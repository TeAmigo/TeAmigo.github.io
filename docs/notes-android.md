
# Table of Contents

1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-09 Sat 09:23&gt; </span></span> - Check out Kotlin. It's being pushed by Google and I'm not in love with java. Or C++. Python maybe, but it doesn't work here. A simpler more block headed language seems to work for me.](#orgda8b6cd)
2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-04 Mon 08:04&gt; </span></span> - Develop a ScrabbleScorer app.](#orgc44e8b8)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-04 Mon 08:04&gt; </span></span> - Discovered /disk2/androidprojects/09Keyboard1 - This is a working hex keyboard example. The only working example I found! Copied project to /disk2/androidprojects/ScrabbleScorer4.](#org3a1e150)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 14:06&gt; </span></span> - Draw a horizontal or vertical line - use an xml shape file and an ImageView to display it. These and other shapes are from a Polish developer's blog, see This url.](#orga33fa4a)
        2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:36&gt; </span></span> - The XML Keyboard description file.](#orgbc5d820)
        3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:36&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-04 Mon 08:29&gt; </span></span> - Need to trim down the key board to a 4 by 3: [(1,2,3),(4,5,6),(7,8,9)(clr-all,0,clear-one)]. This is done in  -](#org9ac4151)
            1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:31&gt; </span></span> - Changed clr-all to a minus sign. Only 1 or 2 digits, no need for more than clear-one twice used.](#org3c6c626)
        4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-06 Wed 20:09&gt; </span></span> - All effort has been at understanding the layout, views, and Shapes. Trying to get the horizontal and vertical lines to work, and the interaction of the ImageView, a real tangle.](#orga13d27d)
        5.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-07 Thu 17:10&gt; </span></span> - I restarted the project in ScrabbleScorer5, using Constraintlayout.](#orgf043b01)
        6.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-07 Thu 17:08&gt; </span></span> - TextView.setText("txt") is what you need for the activeValue TextView.](#org7cd5ecc)
        7.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-09 Sat 09:21&gt; </span></span> - General observation - you may have to do a lot more in code than xml to place the layout objects so they look good on different screens, and there is the issue of the android level that is supported. Many of the coolest newest features are not available on older rigs.](#orgac976c6)
3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 12:25&gt; </span></span> - Downloaded SDK docs - file:///home/rick/Android/Sdk/docs/reference/packages.html - There are other specific areas of documentation in that dir - ~/Android/Sdk/docs/ . Because the search doesn't seem to work, file:///home/rick/Android/Sdk/docs/reference/classes.html is easier to find class defs.](#orgbd2f81c)
4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-01 Fri 08:40&gt; </span></span> - Google Developer Training - goes through a whole lot of examples.](#orga5ef084)
5.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:38&gt; </span></span> - resources, files in the res directory of the project is an xml description of a View, or other resource. A layout resource defines the architecture for the UI in an Activity or a component of a UI. Local doc from the top ,  Web doc ,](#org866cb50)
6.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-02 Sat 22:47&gt; </span></span> - https://constraintlayout.com/basics/guidelines.html](#org6489308)
7.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-01 Fri 09:03&gt; </span></span> - Google is generally a big pain in the ass. They change things constantly, what worked yesterday may not work today. A very tangled mess. Do I want to devote much time to this?](#orgd3bb38f)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-01 Fri 18:25&gt; </span></span> - This layout stuff is rediculous. See](#org10b8948)
8.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 12:50&gt; </span></span> - The local documentation has been downloaded. Getting AndroidStudio to use it evidently requires some tweaking. StackOverflow article suggests changing a config file, ~/.AndroidStudio3.3/config/options/jdk.table.xml . The entry for javadocPath.](#org209a765)
9.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 13:54&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 11:27&gt; </span></span> - Finish the intro sample program https://developer.android.com/training/basics/firstapp/building-ui . In ~/AndroidStudioProjects/MyApplication/ is where it is.  -](#org0d334c3)
10. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-29 Tue 14:37&gt; </span></span> - There are a whole bunch of examples at https://github.com/googlesamples . Lots of them downloaded to *disk2/androidprojects* .](#orga90483b)
11. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:47&gt; </span></span> - Android Application Fundamentals - websource](#org876665f)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:50&gt; </span></span> - The Android operating system is a multi-user Linux system in which each app is a different user. By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps. By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.](#org2541a8a)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:48&gt; </span></span> - App components - There are four different types of app components:](#orgab84e37)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Activity - the entry point for interacting with the user. It represents a single screen with a user interface.](#org65fd666)
        2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Service - does not provide a user interface, runs in the background to perform long-running operations or to perform work for remote processes](#org06a5a4a)
        3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Broadcast receivers](#orgb61cbde)
        4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Content providers](#org76f2e06)
12. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-25 Wed 16:02&gt; </span></span> - Tracking and recording points of interest are my biggest uses at least in the US. trying OSM Tracker. OsmAnd would be great If I can ever get it going again.](#org64183cc)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-27 Fri 15:36&gt; </span></span> - I bought it for the phone. So have the + version.](#org3030794)
13. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-25 Wed 16:04&gt; </span></span> - Navigation - Even Mexico is pretty easy if you can get Google. If not, back to Osmand, which isn't even installing on my phone and has had other difficulties. Try the APK, see if that works. -](#orgee76481)
14. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-06 Fri 18:08&gt; </span></span> - My Osmand on RCA10 decided it had to start all over again when I took away all its Favourites. WTF? Trying to get it to put itself in a certain place is a nightmare, because the naming conventions on adroid are SO fucked up. Had to connect to internet and download world file, and AZ, then putting them in /osmand. (/storage/sdcard0/osmand to osmand).](#org88d2d0d)
15. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-09-09 Sat 13:56&gt; </span></span> - Installed Android Studio on XPS13, /home/rick/Android/Sdk is where the sdk is, /home/rick/share/android-studio/bin/studio.sh is where executable studio is. Projects are in ~/share/AndroidProjects.](#org2a261b6)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-09-09 Sat 14:46&gt; </span></span> - To get the emulator to run, had to link a different ~/Android/Sdk/emulator/lib64/libstdc++. Then the emulator worked. Thanks to https://stackoverflow.com/questions/42831999/android-studio-2-3-ubuntu-16-10-emulator-do-not-start](#org94dfa89)
16. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-06-16 Fri 13:25&gt; </span></span> - RCA11 - currently running Android 5, but don't expect updates from the RCA types.](#orgc67c1a8)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-06-16 Fri 13:28&gt; </span></span> - I was trying to find the mysteriously specified "file system" locations. Look like a directory tree but evidently a huge bunch of partitions. So, I used termux, a comd line interface tool, to do cd, ls, pwd, etc to locate mysterious locations.](#org87e7833)
17. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-06-16 Fri 13:26&gt; </span></span> - RCA10" - system is too old to mess with. Osmand~ upgrade to 2.63 doesn't run on it. Fine for many things though.](#orgdd93fc6)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-05-30 Tue 11:16&gt; </span></span> - The RCA10 is running Android 4.2.2](#org9dc190c)
18. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-24 Thu 15:18&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-13 Sun 17:16&gt; </span></span> - Android Studio - androidstudio - /share/scripts/androidstudio /share/android-studio/bin $ ./studio.sh - This is the Adroid Studio downloaded from http://developer.android.com/sdk/index.html - :androidstudio: -](#orgfbcf278)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-26 Sat 15:30&gt; </span></span> - Code folding, like hiding, showing imports, function definitions, etc. C&#x2013; and C-+ do the job.](#orgb7e8e95)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-24 Thu 15:19&gt; </span></span> - The android skd is at /home/rick/Android/Sdk](#org143a28f)
    3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 14:04&gt; </span></span> - Added this line to ~/.gradle/gradle.properties: org.gradle.jvmargs=-Xmx1536M . This is to up the memory to enable fast run.](#org042f300)
    4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 14:05&gt; </span></span> - Views - can get quick documentation, full screen, etc.](#org142fee1):views:
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 14:08&gt; </span></span> - Get out of full screen mode - move the mouse up to the top of the screen, the menu will appear. Click the double arrows on the right corner.](#orgf1f9ff2)
    5.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 13:36&gt; </span></span> - The version of the compileSDKVersion and the buildToolsVersion is found in the app/build.gradle. Not the top level build.gradle](#org3e02377)
    6.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 14:24&gt; </span></span> - Way too complicated, way too controlling, and generally a big pain in the ass. Google sucks. It truly is a big bag of shit, but it's the only game in town right now. Sort of like windows before linux distros really got going.](#org5af7964)
    7.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-27 Mon 18:48&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-27 Mon 11:50&gt; </span></span> - curl -O studio did it. https://dl.google.com/android/repository/build-tools\_r25.0.2-linux.zip if the sudio can't do it. -](#org729704b)
    8.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-26 Sat 11:07&gt; </span></span> - /dev/kvm keeps coming up and I keep resetting it so I have permissions. BUT, from the web, this advice:](#orga71f974)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-26 Sat 11:08&gt; </span></span> - you need to first sudo apt install qemu-kvm. To check the ownership of /dev/kvm use ls -al /dev/kvm The user was root, the group kvm. To check which users are in the kvm group, use grep kvm /etc/group. To add yourself to the kvm group, you could use sudo adduser rick kvm](#org3bc8846)
    9.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:39&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 10:48&gt; </span></span> - How to set up gradle to avoid going to the net for its zip file. In other words, point to the local gradles installed already. Note that the below allowed AndroidStudio to create the whole project, then shut it down to make the changes listed below. - Tested this with /share/AndroidProjects/OneMoreTime on my 10" tablet, which is Android 4.2, the earliest I have.](#org587d0b1)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:23&gt; </span></span> - Just put the relevant gradle zip in the wrapper directory and set the wrapper properties to point to it. Here's an example:](#orgfa3673f)
            1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:25&gt; </span></span> - the gradle zip is in the wrapper directory: /share/AndroidProjects/OneMoreTime/gradle/wrapper/gradle-2.14.1-all.zip](#orgb7ac861)
            2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:26&gt; </span></span> - The  gradle-wrapper.properties file has been changed to point to the local copy: distributionUrl=gradle-2.14.1-all.zip](#org70a7bcd)
        2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-26 Sun 16:46&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 10:50&gt; </span></span> - Key was to change values in the build.gradle scripts in root directory and app directory. And the value for distributionUrl in gradle-wrapper.properties. Actually using Gradle 3.4.1. Using the app ~/AndroidStudioProjects/MyFirstApp/ to proble this whole issue. Note the file ~/AndroidStudioProjects/MyFirstApp/gradle/wrapper/gradle-wrapper.properties has entries that have to do with the "avoid download" issue. running -](#orgdd99c57)
            1.  [~/AndroidStudioProjects/MyFirstApp $ ./gradlew tasks](#org115a1cd)
            2.  [and changing exec to echo, lets me see things as they exist when gradlew is run. Running it in the current state causes it to execute](#org90e4e0f)
            3.  [Downloading https://services.gradle.org/distributions/gradle-2.14.1-all.zip](#orga6c897a)
            4.  [](#orga0d8e0d)
    10. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-24 Fri 18:10&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 13:16&gt; </span></span> - Where is the maven like file storage area where library etc. jar files and other artifacte files stored? Seems that they are stored in *share/android-studio/gradle/m2repository* maven is a whole nother ball of wax.](#org033f653):repository:
    11. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-24 Fri 18:10&gt; </span></span> - what is a classpath dependency in gradle?](#orge0e2ea7)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-26 Sun 14:45&gt; </span></span> - It is used to install the Android Plugin for Gradle stuff, which extends the vanilla Gradle. As of today, it should be set to 2.2.3. According to table at https://developer.android.com/studio/releases/gradle-plugin.html the plugin should be at 2.3+ for gradle 3.3+. The table at that site lists the versions of the plugin to use with various versions of Gradle.](#org3259c02)
    12. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 13:53&gt; </span></span> - Use the local gradle rather than the "default gradle wrapper" - Tools/Settings/Build,Execution,Deployment and set to use local gradle distribution.](#org3132a9f)
    13. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 13:18&gt; </span></span> - ~/share/EBooks/Android/AndroidStudioDevelopmentEssentialsAndroid6 - http://localhost/Meet%20Android%20Studio%20%7c%20Android%20Studio.html](#org94b0515)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-06 Mon 18:17&gt; </span></span> - Book rcmd v1.5, using 2.2.3. May need to download older version?](#org79c5a5e)
        2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-06 Mon 18:20&gt; </span></span> - Tools/Android/SDK Manager is how it's invoked.](#org5d7a8ff)
        3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-06 Mon 18:15&gt; </span></span> - Downloaded sample code in /share/zips/AndroidStudioBook.zip](#orgcf3409e)
    14. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-26 Sun 12:42&gt; </span></span> - Set font sizes and other stuff: File/Settings/Editor/Colors&Fonts, for Keys, File/Settings/Keymap. Also Appearance may have more to do with Studio elements.](#orga61e167)
    15. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-25 Sat 10:47&gt; </span></span> - Am using it to build tutorial at developer.android.com, see below](#orgac3cd50)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-26 Sun 12:12&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 16:02&gt; </span></span> - I downloaded the Android Documentation via andriod sdk (just type android at $). It only was under Android 7.0 (API 24) in the stand alone sdk manager, it was listed also in Studio from Tools/Android/SDK Manager, which has a very different interface from the stand alone. In the Studio its listed under SDK Tools tab. The documentation downloaded has this course in it, so  using local copy at file:///share/android-sdk-linux/docs/training/basics/firstapp/index.html which is a tutorial to create 1st app. -](#org8f74270)
            1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-26 Sun 12:28&gt; </span></span> - There is a menu on the local copy which allows you to go to any page in the tutorial.](#orgf649caf)
19. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:22&gt; </span></span> - The android development environment](#org8f41443):SDK:
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:23&gt; </span></span> - Android SDK (*share/android-sdk-linux*)](#orgc7a925e)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:24&gt; </span></span> - android - at command line, brings up the Android SDK manager.This lets you install the various android development pieces.](#org588a8df)
        1.  [android help - this gives more info on use of android command.](#orgef380c8)
        2.  [android avd - android virtual device manager - create virtual android devices.](#orgb062520)
    3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-25 Sat 10:51&gt; </span></span> - Installing Sources for Android 22 (sources;android-22) and Android SDK Platform 22 (platforms;android-22) from AndroidStudio, for the ZTE Avis Model Z828 which is Android 5.1.1 Lollipop](#org0710a18)
20. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:20&gt; </span></span> - Get a OsmAnd built.](#orgbbd8fc5):OsmAnd:
21. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 17:00&gt; </span></span> - how to do a android system backup?](#orgbc81c08)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-06 Wed 17:15&gt; </span></span> - to backup:](#orgaf272cf)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 17:00&gt; </span></span> - http://trendblog.net/android-guide-make-nandroid-backup-android-phone/ http://www.techrepublic.com/article/how-to-create-a-full-backup-of-your-android-device-without-root/ http://www.makeuseof.com/tag/what-is-a-nandroid-backup-and-how-exactly-does-it-work/ https://tektab.com/2015/10/31/android-bootloaderfastboot-mode-and-recovery-mode-explained/](#orgddeb056)
22. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 14:48&gt; </span></span> - adb - debugger](#org3953222):adb:debugger:
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-04-07 Fri 17:18&gt; </span></span> - Get a successful adb connection to the RCA11. Setup the ~/.android/adb<sub>usb.ini</sub> with the full idVendor which is 0x1914. Don't leave out the 0x. I have both the RCA10 andRCA11 in there now. This is only necessary with unrecognized devices. The ZTE Avis phone doesn't seem to need an entry.](#org0b7a914)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-07 Sat 10:33&gt; </span></span> - For the RCA10 idVendor is 0x2207](#org21e8c91)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 16:11&gt; </span></span> - Cool little script to capture screen of android device.](#org5055674)
    3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 14:49&gt; </span></span> - https://developer.android.com/studio/command-line/adb.html](#org859a2a6)
    4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 15:16&gt; </span></span> - create the capacity on the android device to use adb, go into Settings/About Phone/ and tap Build Number 7 times. This will make you a developer and create a Developers Options item in the Settings screen.](#orgd31e4a5)
    5.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:47&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-29 Tue 19:04&gt; </span></span> - I'm up to finding the adb<sub>usb.ini</sub> after following http://ryancuda.blogspot.com/2013/12/how-to-get-working-adb-drivers-for.html "How to get working ADB drivers for unrecognized Android devices". Using this first to set up RCA RCT6103W46 10"  Tablet.](#orgeb558f2)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:47&gt; </span></span> - Using the site above, followed these steps.](#org5ffe661)
            1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:48&gt; </span></span> - Turned on developer options on 10" RCA by repeatedly tapping build number in Settings - System - About tablet. Then the Developer menu appears under System in Settings app. Checked "USB Debugging".](#org19ef288)
            2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:53&gt; </span></span> - Executed lsusb -vv and found the relevant device. This output a lot of info, See file /share/notes/lsusb112916. The number needed is called "idVendor"in the output of lsusb -vv, in the article he refers to it as device ID.](#org4f902a2)
            3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 15:52&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:58&gt; </span></span> - Execute "android update adb"; only if you don't already have an ~/.android/adb<sub>usb.ini</sub>. "android update adb" creates a new ~/.android/adb<sub>usb.ini</sub>, losing the contents of it. Edit that file adding the idVendor from step 2 at the end of the file. -](#orgd4a0f78)
                1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 15:04&gt;</span></span>Note that I downloaded the whole android sdk from https://developer.android.com/studio/index.html#downloads. I also downloaded the Android Studio from there, but haven't played with it](#orgee2e989)
            4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 15:04&gt; </span></span> - Run "adb kill-server" then "adb devices". This worked, the last command returned the serial number of my device, thus adb sees it.](#org1d0c0e7)
23. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-02 Mon 12:03&gt; </span></span> - RCA RCT6103W46 10"  Tablet with wireless keyboard](#org0ecf7a1)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 17:02&gt; </span></span> - Rooting https://www.google.com/search?num=100&newwindow=1&client=ubuntu&hs=Rsy&channel=fs&q=rca+rct6103w46+10%22+root&oq=rca+rct6103w46+10%22+root&gs\_l=serp.3..33i160k1.1965803.1968030.0.1969068.4.4.0.0.0.0.277.277.2-1.1.0&#x2026;.0&#x2026;1.1.64.serp..3.1.276.0zwuD4u3AC4](#org49b5c6a)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-08-31 Wed 15:25&gt; </span></span> - Get into recovery mode - hold power-on and volume-down buttons until dogs appear. Then keep holding the volume down button. After the android icon appears, use volume-up and volume down to move through menu, power-on to select. https://youtu.be/N-6yvjgR06Y ,](#orgdacfdf5)
    3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-08-31 Wed 12:06&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-02 Mon 12:05&gt; </span></span> - Fix the broken glass. Seems the underneath is fine, bought the little tools, watch 2 videos -/Video/RCA Tablet Glass DigitizerTouchscreen Replacement - Disassembly (Low).mp4 and other one. Got the glass in and is working well.](#orgdaf633a)
        1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-02 Mon 12:24&gt; </span></span> - Turn it off with a broken screen - press and hold the power button as usual, with keyboard attached, now your in a selectin mode where you can use the arrow keys to move, and enter to select.](#org6a59141)
        2.  [/Video/RCA Tablet Glass DigitizerTouchscreen Replacement - Disassembly (Low).mp4](#org0adc379)
        3.  [/Video/RCA Tablet Glass DigitizerTouchscreen Replacement - Reassembly (Low).webm](#orgd24b873)
24. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-08-31 Wed 12:08&gt; </span></span> - ZTE Avid Plus phone, T-mobile account, $95/mo for 14Gb hotspot or tethered, and unlimited data on phone itself. Used it to download over 30Gb of stuff in less than a month.](#org50104ed)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 15:20&gt; </span></span> - send and receive files using adb. What I'm interested in now is the /storage/sdcard1/Flud directory on the sdcard1. used adb shell and poked around the directories until I found it. Then use e.g. adb push uks.mp4 /storage/sdcard1/Flud (in dir where uks.mp4 exists). This is much slower than Nautilus.](#org9187590)
25. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-01-31 Sun 18:21&gt; </span></span> - The 11" RCA with Android 5. Gps doesn't work. When connecting with USB cable to laptop, pull down the "whats going on" menu, ad check connected to a media device. Touch that and you get a couple of options.](#org86c5395)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-02-01 Mon 14:21&gt; </span></span> - Get files onto or off it, use a USB drive then esFileExplorer.](#org7bed649)
26. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-01-19 Tue 14:09&gt; </span></span> - HUAWEI-H881C android phone - got it from Carole, JE using for mp3 playing, put a microSD card in it, you have to take off the back to get to it. Manual is downloaded to  /share/EBooks/MANUALS/HUAWEI-H881C-UserGuideEN.pdf](#org4544f3e)
27. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 12:11&gt; </span></span> - I busted my irulu xPro1 10" , no os, so am trying to get it back.](#org3b84ad9)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 14:57&gt; </span></span> - http://androidforums.com/threads/rca-pro-10-tablet.875260/ and http://forum.xda-developers.com/android/general/firmware-rca-viking-pro-rct6303w87dk-t3325158](#orgd58be20)
    2.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 12:12&gt; </span></span> - Downloaded adb and fastboot on Ubuntu via apt-get, poking around many sites,](#org5c9b9b1)
    3.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 12:13&gt; </span></span> - Can I use fastboot? See http://android.wonderhowto.com/how-to/know-your-android-tools-what-is-fastboot-do-you-use-it-0155640/](#org5e97292)
    4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 14:33&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 14:51&gt; </span></span> - The following allowed me to download 360wangpan<sub>setup.exe</sub> in zips, but its all in Chinese!](#org4ab6da9)
        1.  [Wrote Hello, I did something and I only can boot into recovery mode or fastboot. Is there an image of the ROM that I can download and install? My S/N is X1047JG1503031E1519. Thank you for any help, Rick Charon at https://www.irulu.com/tablet/p-irulu-expro-x1-pro-series-android-4.4-high-speed-octa-core-tablet-16gb-rom-10-points-capacitive-ips-touch-screen-bluetooth-4.2\_1023431.html  -](#orga21ef95)
    5.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 14:34&gt; </span></span> - Looking at installing Ubuntu Touch, following https://developer.ubuntu.com/en/start/ubuntu-for-devices/installing-ubuntu-for-devices/](#org6c78a7d)
    6.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 14:48&gt; </span></span> - Get adb connected = on device, go into the install via adb screen, msg is to send package you want to apply, and from laptop, adb devices shows it there.](#org706b0e7)
    7.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 16:38&gt; </span></span> - tried adb sideload with zip for nexus, aborted.](#org945af6b)
    8.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-16 Mon 14:08&gt; </span></span> - Most hopeful solution yet, but looked and not even sure which is the CPU! http://www.blogtechtips.com/2015/01/01/find-chinese-tablet-firmware-flash-file-using-board-id/](#org7895711)
    9.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-18 Wed 17:37&gt;</span></span>https://code.google.com/p/android-roms/wiki/Install\_Custom\_ROM - Is this possible.](#org4968675)
    10. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-18 Wed 17:40&gt; </span></span> - Instructions: How to use “adb sideload” in Linux &#x2013;  https://code.google.com/p/android-roms/wiki/Install\_Custom\_ROM](#orgb8d143c)
28. [REDO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-13 Sun 17:11&gt; </span></span> - I was installing the android source from https://source.android.com/source/downloading.html, decided to hold off,](#orgf8f62ae)
29. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-12 Sat 16:44&gt; </span></span> - Set up debugging mode:](#orgbf69903)
    1.  [.   Open up your device’s “Settings”. This can be done by pressing the Menu button while on your home screen and tapping “System settings”](#org6a1e7d9)
    2.  [.  Now scroll to the bottom and tap “About phone” or “About tablet”.  At the “About” screen, scroll to the bottom and tap on “Build number” seven times.  Make sure you tap seven times. If you see a “Not need, you are already a developer!” message pop up, then you know you have done it correctly.](#org9cbebb3)
    3.  [. Done! By tapping on “Build number” seven times, you have unlocked USB debugging mode on Android 4.2 and higher. You can now enable/disable it whenever you desire by going to “Settings” -> “Developer Options” -> “Debugging” ->” USB debugging”.](#orgc97c97d)
30. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-11 Fri 19:03&gt; </span></span> - Get into it, the programming and control. Learn it. Following https://source.android.com/source/initializing.html , have installed the openjdk by](#orgb7dd277):dev:
    1.  [sudo update-alternatives &#x2013;config java](#org724cd81)
    2.  [sudo update-alternatives &#x2013;config javac](#org08d083c)
    3.  [Think I did what was suggested in https://source.android.com/source/initializing.html, on to https://source.android.com/source/downloading.html](#orge6f9283)
    4.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-12 Sat 16:24&gt; </span></span> - following along, set up repo in ~/bin/repo. This is a python script "Repo is a tool that makes it easier to work with Git in the context of Android." (from https://source.android.com/source/downloading.html](#org381ca5c)
31. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-01 Tue 08:14&gt; </span></span> - get the bu353 GPS USB dongle to work: After system start up run PL2303 app. Allow it to take over the GPS function. Then you're ready to go, run Map.Me or other.](#org1c848a7)
32. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-07 Wed 10:25&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-12-15 Mon 17:10&gt; </span></span> - Get a decent mp3 player setup. Creating and using playlists is important. For doing Spanish going down the road. - WE NOW HAVE ANDROID BLUETOOTH. Game over.](#orge1acf9b)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-12-15 Mon 18:51&gt; </span></span> - One of the biggest PITA is the tag listing. I use files, and want file names. Found 2 apps that play directories directly, trying them.](#orgf66be9b)
33. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-10-02 Thu 22:54&gt; </span></span> - Dropbox on RCA Android device from Xubuntu, Choose export to save a file to the android disk. Favorite doesn't do it.](#org5129b20)
34. [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-10-02 Thu 22:55&gt; </span></span> The MTP protocol, -](#org8724d9c)
    1.  [- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-08 Thu 11:22&gt; </span></span> With the ZTE Avis Plus Z828 phone plugged in and MTP connection chosen on the phone, mount point is *run/user/1000/gvfs* , in that directory there is a file called mtp:gooble-gooble. that's the android file system.](#orga8be452)

Android Notes


<a id="orgda8b6cd"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-09 Sat 09:23&gt; </span></span> - Check out Kotlin. It's being pushed by Google and I'm not in love with java. Or C++. Python maybe, but it doesn't work here. A simpler more block headed language seems to work for me.


<a id="orgc44e8b8"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-04 Mon 08:04&gt; </span></span> - Develop a ScrabbleScorer app.


<a id="org3a1e150"></a>

## PROCESS - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-04 Mon 08:04&gt; </span></span> - Discovered /disk2/androidprojects/09Keyboard1 - This is a working hex keyboard example. The only working example I found! Copied project to /disk2/androidprojects/ScrabbleScorer4.


<a id="orga33fa4a"></a>

### HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 14:06&gt; </span></span> - Draw a horizontal or vertical line - use an xml shape file and an ImageView to display it. These and other shapes are from a Polish developer's blog, see [This url.](https://android-dev-examples.blogspot.com/2014/08/android-shape-line.html?showComment=1549405736938#c7392760593496643228)


<a id="orgbc5d820"></a>

### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:36&gt; </span></span> - [The XML Keyboard description file.](file:///disk2/androidprojects/ScrabbleScorer4/app/src/main/res/xml/hexkbd.xml)


<a id="org9ac4151"></a>

### FIXED  - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:36&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-04 Mon 08:29&gt; </span></span> - Need to trim down the key board to a 4 by 3: [(1,2,3),(4,5,6),(7,8,9)(clr-all,0,clear-one)]. This is done in  -


<a id="org3c6c626"></a>

#### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:31&gt; </span></span> - Changed clr-all to a minus sign. Only 1 or 2 digits, no need for more than clear-one twice used.


<a id="orga13d27d"></a>

### UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-06 Wed 20:09&gt; </span></span> - All effort has been at understanding the layout, views, and Shapes. Trying to get the horizontal and vertical lines to work, and the interaction of the ImageView, a real tangle.


<a id="orgf043b01"></a>

### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-07 Thu 17:10&gt; </span></span> - I restarted the project in ScrabbleScorer5, using Constraintlayout.


<a id="org7cd5ecc"></a>

### UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-07 Thu 17:08&gt; </span></span> - TextView.setText("txt") is what you need for the activeValue TextView.


<a id="orgac976c6"></a>

### UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-09 Sat 09:21&gt; </span></span> - General observation - you may have to do a lot more in code than xml to place the layout objects so they look good on different screens, and there is the issue of the android level that is supported. Many of the coolest newest features are not available on older rigs.


<a id="orgbd2f81c"></a>

# REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 12:25&gt; </span></span> - Downloaded SDK docs - <file:///home/rick/Android/Sdk/docs/reference/packages.html> - There are other specific areas of documentation in that dir - ~/Android/Sdk/docs/ . Because the search doesn't seem to work, <file:///home/rick/Android/Sdk/docs/reference/classes.html> is easier to find class defs.


<a id="orga5ef084"></a>

# REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-01 Fri 08:40&gt; </span></span> - [Google Developer Training](https://google-developer-training.github.io/android-developer-fundamentals-course-concepts-v2/) - goes through a whole lot of examples.


<a id="org866cb50"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-05 Tue 09:38&gt; </span></span> - resources, files in the res directory of the project is an xml description of a View, or other resource. A layout resource defines the architecture for the UI in an Activity or a component of a UI. [Local doc from the top](file:///home/rick/Android/Sdk/docs/guide/topics/resources/overview.html) ,  [Web doc](https://developer.android.com/guide/topics/resources/layout-resource) ,


<a id="org6489308"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-02 Sat 22:47&gt; </span></span> - <https://constraintlayout.com/basics/guidelines.html>


<a id="orgd3bb38f"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-01 Fri 09:03&gt; </span></span> - Google is generally a big pain in the ass. They change things constantly, what worked yesterday may not work today. A very tangled mess. Do I want to devote much time to this?


<a id="org10b8948"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-01 Fri 18:25&gt; </span></span> - This layout stuff is rediculous. See


<a id="org209a765"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 12:50&gt; </span></span> - The local documentation has been downloaded. Getting AndroidStudio to use it evidently requires some tweaking. [StackOverflow](https://stackoverflow.com/questions/42893969/how-to-use-android-sdk-documentation-offline/43005110#43005110) article suggests changing a config file, ~/.AndroidStudio3.3/config/options/jdk.table.xml . The entry for javadocPath.


<a id="org0d334c3"></a>

# FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 13:54&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-31 Thu 11:27&gt; </span></span> - Finish the intro sample program <https://developer.android.com/training/basics/firstapp/building-ui> . In ~/AndroidStudioProjects/MyApplication/ is where it is.  -


<a id="orga90483b"></a>

# CHECK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-29 Tue 14:37&gt; </span></span> - There are a whole bunch of examples at <https://github.com/googlesamples> . Lots of them downloaded to *disk2/androidprojects* .


<a id="org876665f"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:47&gt; </span></span> - Android Application Fundamentals - [websource](https://developer.android.com/guide/components/fundamentals)


<a id="org2541a8a"></a>

## NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:50&gt; </span></span> - The Android operating system is a multi-user Linux system in which each app is a different user. By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps. By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.


<a id="orgab84e37"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:48&gt; </span></span> - App components - There are four different types of app components:


<a id="org65fd666"></a>

### 1 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Activity - the entry point for interacting with the user. It represents a single screen with a user interface.


<a id="org06a5a4a"></a>

### 2 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Service - does not provide a user interface, runs in the background to perform long-running operations or to perform work for remote processes


<a id="orgb61cbde"></a>

### 3 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Broadcast receivers


<a id="org76f2e06"></a>

### 3 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-28 Mon 15:53&gt; </span></span> - Content providers


<a id="org64183cc"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-25 Wed 16:02&gt; </span></span> - Tracking and recording points of interest are my biggest uses at least in the US. trying OSM Tracker. OsmAnd would be great If I can ever get it going again.


<a id="org3030794"></a>

## UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-27 Fri 15:36&gt; </span></span> - I bought it for the phone. So have the + version.


<a id="orgee76481"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-25 Wed 16:04&gt; </span></span> - Navigation - Even Mexico is pretty easy if you can get Google. If not, back to Osmand, which isn't even installing on my phone and has had other difficulties. Try the APK, see if that works. -


<a id="org88d2d0d"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-06 Fri 18:08&gt; </span></span> - My Osmand on RCA10 decided it had to start all over again when I took away all its Favourites. WTF? Trying to get it to put itself in a certain place is a nightmare, because the naming conventions on adroid are SO fucked up. Had to connect to internet and download world file, and AZ, then putting them in /osmand. (/storage/sdcard0/osmand to osmand).


<a id="org2a261b6"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-09-09 Sat 13:56&gt; </span></span> - Installed Android Studio on XPS13, /home/rick/Android/Sdk is where the sdk is, /home/rick/share/android-studio/bin/studio.sh is where executable studio is. Projects are in ~/share/AndroidProjects.


<a id="org94dfa89"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-09-09 Sat 14:46&gt; </span></span> - To get the emulator to run, had to link a different ~/Android/Sdk/emulator/lib64/libstdc++. Then the emulator worked. Thanks to <https://stackoverflow.com/questions/42831999/android-studio-2-3-ubuntu-16-10-emulator-do-not-start>


<a id="orgc67c1a8"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-06-16 Fri 13:25&gt; </span></span> - RCA11 - currently running Android 5, but don't expect updates from the RCA types.


<a id="org87e7833"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-06-16 Fri 13:28&gt; </span></span> - I was trying to find the mysteriously specified "file system" locations. Look like a directory tree but evidently a huge bunch of partitions. So, I used termux, a comd line interface tool, to do cd, ls, pwd, etc to locate mysterious locations.


<a id="orgdd93fc6"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-06-16 Fri 13:26&gt; </span></span> - RCA10" - system is too old to mess with. Osmand~ upgrade to 2.63 doesn't run on it. Fine for many things though.


<a id="org9dc190c"></a>

## NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-05-30 Tue 11:16&gt; </span></span> - The RCA10 is running Android 4.2.2


<a id="orgfbcf278"></a>

# UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-24 Thu 15:18&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-13 Sun 17:16&gt; </span></span> - Android Studio - androidstudio - /share/scripts/androidstudio /share/android-studio/bin $ ./studio.sh - This is the Adroid Studio downloaded from <http://developer.android.com/sdk/index.html> - :androidstudio: -


<a id="orgb7e8e95"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-26 Sat 15:30&gt; </span></span> - Code folding, like hiding, showing imports, function definitions, etc. C&#x2013; and C-+ do the job.


<a id="org143a28f"></a>

## ENTRY - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-24 Thu 15:19&gt; </span></span> - The android skd is at /home/rick/Android/Sdk


<a id="org042f300"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 14:04&gt; </span></span> - Added this line to ~/.gradle/gradle.properties: org.gradle.jvmargs=-Xmx1536M . This is to up the memory to enable fast run.


<a id="org142fee1"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 14:05&gt; </span></span> - Views - can get quick documentation, full screen, etc.     :views:


<a id="orgf1f9ff2"></a>

### HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 14:08&gt; </span></span> - Get out of full screen mode - move the mouse up to the top of the screen, the menu will appear. Click the double arrows on the right corner.


<a id="org3e02377"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-29 Wed 13:36&gt; </span></span> - The version of the compileSDKVersion and the buildToolsVersion is found in the app/build.gradle. Not the top level build.gradle


<a id="org5af7964"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 14:24&gt; </span></span> - Way too complicated, way too controlling, and generally a big pain in the ass. Google sucks. It truly is a big bag of shit, but it's the only game in town right now. Sort of like windows before linux distros really got going.


<a id="org729704b"></a>

## FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-27 Mon 18:48&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-27 Mon 11:50&gt; </span></span> - curl -O studio did it. <https://dl.google.com/android/repository/build-tools_r25.0.2-linux.zip> if the sudio can't do it. -


<a id="orga71f974"></a>

## ENTRY - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-26 Sat 11:07&gt; </span></span> - /dev/kvm keeps coming up and I keep resetting it so I have permissions. BUT, from the web, this advice:


<a id="org3bc8846"></a>

### ENTRY - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-01-26 Sat 11:08&gt; </span></span> - you need to first sudo apt install qemu-kvm. To check the ownership of /dev/kvm use ls -al /dev/kvm The user was root, the group kvm. To check which users are in the kvm group, use grep kvm /etc/group. To add yourself to the kvm group, you could use sudo adduser rick kvm


<a id="org587d0b1"></a>

## FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:39&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 10:48&gt; </span></span> - How to set up gradle to avoid going to the net for its zip file. In other words, point to the local gradles installed already. Note that the below allowed AndroidStudio to create the whole project, then shut it down to make the changes listed below. - Tested this with /share/AndroidProjects/OneMoreTime on my 10" tablet, which is Android 4.2, the earliest I have.


<a id="orgfa3673f"></a>

### FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:23&gt; </span></span> - Just put the relevant gradle zip in the wrapper directory and set the wrapper properties to point to it. Here's an example:


<a id="orgb7ac861"></a>

#### 1 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:25&gt; </span></span> - the gradle zip is in the wrapper directory: /share/AndroidProjects/OneMoreTime/gradle/wrapper/gradle-2.14.1-all.zip


<a id="org70a7bcd"></a>

#### 2 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 18:26&gt; </span></span> - The  gradle-wrapper.properties file has been changed to point to the local copy: distributionUrl=gradle-2.14.1-all.zip


<a id="orgdd99c57"></a>

### FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-26 Sun 16:46&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-25 Sat 10:50&gt; </span></span> - Key was to change values in the build.gradle scripts in root directory and app directory. And the value for distributionUrl in gradle-wrapper.properties. Actually using Gradle 3.4.1. Using the app ~/AndroidStudioProjects/MyFirstApp/ to proble this whole issue. Note the file ~/AndroidStudioProjects/MyFirstApp/gradle/wrapper/gradle-wrapper.properties has entries that have to do with the "avoid download" issue. running -


<a id="org115a1cd"></a>

#### ~/AndroidStudioProjects/MyFirstApp $ ./gradlew tasks


<a id="org90e4e0f"></a>

#### and changing exec to echo, lets me see things as they exist when gradlew is run. Running it in the current state causes it to execute


<a id="orga6c897a"></a>

#### Downloading <https://services.gradle.org/distributions/gradle-2.14.1-all.zip>


<a id="orga0d8e0d"></a>

#### 


<a id="org033f653"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-24 Fri 18:10&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 13:16&gt; </span></span> - Where is the maven like file storage area where library etc. jar files and other artifacte files stored? Seems that they are stored in *share/android-studio/gradle/m2repository* maven is a whole nother ball of wax.     :repository:


<a id="orge0e2ea7"></a>

## QUESTION - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-24 Fri 18:10&gt; </span></span> - what is a classpath dependency in gradle?


<a id="org3259c02"></a>

### UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-26 Sun 14:45&gt; </span></span> - It is used to install the Android Plugin for Gradle stuff, which extends the vanilla Gradle. As of today, it should be set to 2.2.3. According to table at <https://developer.android.com/studio/releases/gradle-plugin.html> the plugin should be at 2.3+ for gradle 3.3+. The table at that site lists the versions of the plugin to use with various versions of Gradle.


<a id="org3132a9f"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 13:53&gt; </span></span> - Use the local gradle rather than the "default gradle wrapper" - Tools/Settings/Build,Execution,Deployment and set to use local gradle distribution.


<a id="org94b0515"></a>

## REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 13:18&gt; </span></span> - ~/share/EBooks/Android/AndroidStudioDevelopmentEssentialsAndroid6 - <http://localhost/Meet%20Android%20Studio%20%7c%20Android%20Studio.html>


<a id="org79c5a5e"></a>

### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-06 Mon 18:17&gt; </span></span> - Book rcmd v1.5, using 2.2.3. May need to download older version?


<a id="org5d7a8ff"></a>

### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-06 Mon 18:20&gt; </span></span> - Tools/Android/SDK Manager is how it's invoked.


<a id="orgcf3409e"></a>

### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-06 Mon 18:15&gt; </span></span> - Downloaded sample code in /share/zips/AndroidStudioBook.zip


<a id="orga61e167"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-26 Sun 12:42&gt; </span></span> - Set font sizes and other stuff: File/Settings/Editor/Colors&Fonts, for Keys, File/Settings/Keymap. Also Appearance may have more to do with Studio elements.


<a id="orgac3cd50"></a>

## UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-25 Sat 10:47&gt; </span></span> - Am using it to build tutorial at developer.android.com, see below


<a id="org8f74270"></a>

### UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-26 Sun 12:12&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 16:02&gt; </span></span> - I downloaded the Android Documentation via andriod sdk (just type android at $). It only was under Android 7.0 (API 24) in the stand alone sdk manager, it was listed also in Studio from Tools/Android/SDK Manager, which has a very different interface from the stand alone. In the Studio its listed under SDK Tools tab. The documentation downloaded has this course in it, so  using local copy at <file:///share/android-sdk-linux/docs/training/basics/firstapp/index.html> which is a tutorial to create 1st app. -


<a id="orgf649caf"></a>

#### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-26 Sun 12:28&gt; </span></span> - There is a menu on the local copy which allows you to go to any page in the tutorial.


<a id="org8f41443"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:22&gt; </span></span> - The android development environment     :SDK:


<a id="orgc7a925e"></a>

## NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:23&gt; </span></span> - Android SDK (*share/android-sdk-linux*)


<a id="org588a8df"></a>

## COMMANDS - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:24&gt; </span></span> - android - at command line, brings up the Android SDK manager.This lets you install the various android development pieces.


<a id="orgef380c8"></a>

### android help - this gives more info on use of android command.


<a id="orgb062520"></a>

### android avd - android virtual device manager - create virtual android devices.


<a id="org0710a18"></a>

## UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-25 Sat 10:51&gt; </span></span> - Installing Sources for Android 22 (sources;android-22) and Android SDK Platform 22 (platforms;android-22) from AndroidStudio, for the ZTE Avis Model Z828 which is Android 5.1.1 Lollipop


<a id="orgbbd8fc5"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-02-24 Fri 15:20&gt; </span></span> - Get a OsmAnd built.     :OsmAnd:


<a id="orgbc81c08"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 17:00&gt; </span></span> - how to do a android system backup?


<a id="orgaf272cf"></a>

## CHECK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2019-02-06 Wed 17:15&gt; </span></span> - to backup:

    adb backup -apk -shared -all -f ~/rca11backup.ab # the RCA11 has very restrictive policies. Probably have to root it to bck it up.
    adb restore rca11backup.ab # never got to this because of the RCA bullshit.


<a id="orgddeb056"></a>

## REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 17:00&gt; </span></span> - <http://trendblog.net/android-guide-make-nandroid-backup-android-phone/> <http://www.techrepublic.com/article/how-to-create-a-full-backup-of-your-android-device-without-root/> <http://www.makeuseof.com/tag/what-is-a-nandroid-backup-and-how-exactly-does-it-work/> <https://tektab.com/2015/10/31/android-bootloaderfastboot-mode-and-recovery-mode-explained/>


<a id="org3953222"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 14:48&gt; </span></span> - adb - debugger     :adb:debugger:


<a id="org0b7a914"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-04-07 Fri 17:18&gt; </span></span> - Get a successful adb connection to the RCA11. Setup the ~/.android/adb<sub>usb.ini</sub> with the full idVendor which is 0x1914. Don't leave out the 0x. I have both the RCA10 andRCA11 in there now. This is only necessary with unrecognized devices. The ZTE Avis phone doesn't seem to need an entry.

    adb shell   #and you're in the root dir of device.


<a id="org21e8c91"></a>

### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2018-04-07 Sat 10:33&gt; </span></span> - For the RCA10 idVendor is 0x2207


<a id="org5055674"></a>

## CHECK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 16:11&gt; </span></span> - Cool little script to capture screen of android device.

$ adb shell screencap /sdcard/screen.png
$ adb pull /sdcard/screen.png 


<a id="org859a2a6"></a>

## REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 14:49&gt; </span></span> - <https://developer.android.com/studio/command-line/adb.html>


<a id="orgd31e4a5"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 15:16&gt; </span></span> - create the capacity on the android device to use adb, go into Settings/About Phone/ and tap Build Number 7 times. This will make you a developer and create a Developers Options item in the Settings screen.


<a id="orgeb558f2"></a>

## FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:47&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-29 Tue 19:04&gt; </span></span> - I'm up to finding the adb<sub>usb.ini</sub> after following <http://ryancuda.blogspot.com/2013/12/how-to-get-working-adb-drivers-for.html> "How to get working ADB drivers for unrecognized Android devices". Using this first to set up RCA RCT6103W46 10"  Tablet.


<a id="org5ffe661"></a>

### ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:47&gt; </span></span> - Using the site above, followed these steps.


<a id="org19ef288"></a>

#### 1 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:48&gt; </span></span> - Turned on developer options on 10" RCA by repeatedly tapping build number in Settings - System - About tablet. Then the Developer menu appears under System in Settings app. Checked "USB Debugging".


<a id="org4f902a2"></a>

#### 2 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:53&gt; </span></span> - Executed lsusb -vv and found the relevant device. This output a lot of info, See file /share/notes/lsusb112916. The number needed is called "idVendor"in the output of lsusb -vv, in the article he refers to it as device ID.


<a id="orgd4a0f78"></a>

#### UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2017-03-23 Thu 15:52&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 14:58&gt; </span></span> - Execute "android update adb"; only if you don't already have an ~/.android/adb<sub>usb.ini</sub>. "android update adb" creates a new ~/.android/adb<sub>usb.ini</sub>, losing the contents of it. Edit that file adding the idVendor from step 2 at the end of the file. -


<a id="orgee2e989"></a>

##### NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 15:04&gt;</span></span>Note that I downloaded the whole android sdk from <https://developer.android.com/studio/index.html#downloads>. I also downloaded the Android Studio from there, but haven't played with it


<a id="org1d0c0e7"></a>

#### 4 - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-11-30 Wed 15:04&gt; </span></span> - Run "adb kill-server" then "adb devices". This worked, the last command returned the serial number of my device, thus adb sees it.


<a id="org0ecf7a1"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-02 Mon 12:03&gt; </span></span> - RCA RCT6103W46 10"  Tablet with wireless keyboard


<a id="org49b5c6a"></a>

## REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 17:02&gt; </span></span> - Rooting <https://www.google.com/search?num=100&newwindow=1&client=ubuntu&hs=Rsy&channel=fs&q=rca+rct6103w46+10%22+root&oq=rca+rct6103w46+10%22+root&gs_l=serp.3..33i160k1.1965803.1968030.0.1969068.4.4.0.0.0.0.277.277.2-1.1.0....0...1.1.64.serp..3.1.276.0zwuD4u3AC4>


<a id="orgdacfdf5"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-08-31 Wed 15:25&gt; </span></span> - Get into recovery mode - hold power-on and volume-down buttons until dogs appear. Then keep holding the volume down button. After the android icon appears, use volume-up and volume down to move through menu, power-on to select. <https://youtu.be/N-6yvjgR06Y> ,


<a id="orgdaf633a"></a>

## FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-08-31 Wed 12:06&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-02 Mon 12:05&gt; </span></span> - Fix the broken glass. Seems the underneath is fine, bought the little tools, watch 2 videos -/Video/RCA Tablet Glass DigitizerTouchscreen Replacement - Disassembly (Low).mp4 and other one. Got the glass in and is working well.


<a id="org6a59141"></a>

### HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-02 Mon 12:24&gt; </span></span> - Turn it off with a broken screen - press and hold the power button as usual, with keyboard attached, now your in a selectin mode where you can use the arrow keys to move, and enter to select.


<a id="org0adc379"></a>

### /Video/RCA Tablet Glass DigitizerTouchscreen Replacement - Disassembly (Low).mp4


<a id="orgd24b873"></a>

### /Video/RCA Tablet Glass DigitizerTouchscreen Replacement - Reassembly (Low).webm


<a id="org50104ed"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-08-31 Wed 12:08&gt; </span></span> - ZTE Avid Plus phone, T-mobile account, $95/mo for 14Gb hotspot or tethered, and unlimited data on phone itself. Used it to download over 30Gb of stuff in less than a month.


<a id="org9187590"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 15:20&gt; </span></span> - send and receive files using adb. What I'm interested in now is the /storage/sdcard1/Flud directory on the sdcard1. used adb shell and poked around the directories until I found it. Then use e.g. adb push uks.mp4 /storage/sdcard1/Flud (in dir where uks.mp4 exists). This is much slower than Nautilus.


<a id="org86c5395"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-01-31 Sun 18:21&gt; </span></span> - The 11" RCA with Android 5. Gps doesn't work. When connecting with USB cable to laptop, pull down the "whats going on" menu, ad check connected to a media device. Touch that and you get a couple of options.


<a id="org7bed649"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-02-01 Mon 14:21&gt; </span></span> - Get files onto or off it, use a USB drive then esFileExplorer.


<a id="org4544f3e"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-01-19 Tue 14:09&gt; </span></span> - HUAWEI-H881C android phone - got it from Carole, JE using for mp3 playing, put a microSD card in it, you have to take off the back to get to it. Manual is downloaded to  /share/EBooks/MANUALS/HUAWEI-H881C-UserGuideEN.pdf


<a id="org3b84ad9"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 12:11&gt; </span></span> - I busted my irulu xPro1 10" , no os, so am trying to get it back.


<a id="orgd58be20"></a>

## REFERENCES - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-13 Tue 14:57&gt; </span></span> - <http://androidforums.com/threads/rca-pro-10-tablet.875260/> and <http://forum.xda-developers.com/android/general/firmware-rca-viking-pro-rct6303w87dk-t3325158>


<a id="org5c9b9b1"></a>

## ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 12:12&gt; </span></span> - Downloaded adb and fastboot on Ubuntu via apt-get, poking around many sites,


<a id="org5e97292"></a>

## QUESTION - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 12:13&gt; </span></span> - Can I use fastboot? See <http://android.wonderhowto.com/how-to/know-your-android-tools-what-is-fastboot-do-you-use-it-0155640/>


<a id="org4ab6da9"></a>

## DID NOT WORK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 14:33&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-12 Thu 14:51&gt; </span></span> - The following allowed me to download 360wangpan<sub>setup.exe</sub> in zips, but its all in Chinese!


<a id="orga21ef95"></a>

### Wrote Hello, I did something and I only can boot into recovery mode or fastboot. Is there an image of the ROM that I can download and install? My S/N is X1047JG1503031E1519. Thank you for any help, Rick Charon at <https://www.irulu.com/tablet/p-irulu-expro-x1-pro-series-android-4.4-high-speed-octa-core-tablet-16gb-rom-10-points-capacitive-ips-touch-screen-bluetooth-4.2_1023431.html>  -


<a id="org6c78a7d"></a>

## CANCELED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 14:34&gt; </span></span> - Looking at installing Ubuntu Touch, following <https://developer.ubuntu.com/en/start/ubuntu-for-devices/installing-ubuntu-for-devices/>


<a id="org706b0e7"></a>

## HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 14:48&gt; </span></span> - Get adb connected = on device, go into the install via adb screen, msg is to send package you want to apply, and from laptop, adb devices shows it there.


<a id="org945af6b"></a>

## QUESTION - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-13 Fri 16:38&gt; </span></span> - tried adb sideload with zip for nexus, aborted.


<a id="org7895711"></a>

## CHECK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-16 Mon 14:08&gt; </span></span> - Most hopeful solution yet, but looked and not even sure which is the CPU! <http://www.blogtechtips.com/2015/01/01/find-chinese-tablet-firmware-flash-file-using-board-id/>

<http://www.blogtechtips.com/2014/08/13/tablet-stuck-on-android-screen-fix/> is also interesting.


<a id="org4968675"></a>

## CHECK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-18 Wed 17:37&gt;</span></span><https://code.google.com/p/android-roms/wiki/Install_Custom_ROM> - Is this possible.


<a id="orgb8d143c"></a>

## CHECK - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-11-18 Wed 17:40&gt; </span></span> - Instructions: How to use “adb sideload” in Linux &#x2013;  <https://code.google.com/p/android-roms/wiki/Install_Custom_ROM>


<a id="orgf8f62ae"></a>

# REDO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-13 Sun 17:11&gt; </span></span> - I was installing the android source from <https://source.android.com/source/downloading.html>, decided to hold off,


<a id="orgbf69903"></a>

# HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-12 Sat 16:44&gt; </span></span> - Set up debugging mode:


<a id="org6a1e7d9"></a>

## 1 .   Open up your device’s “Settings”. This can be done by pressing the Menu button while on your home screen and tapping “System settings”


<a id="org9cbebb3"></a>

## 2 .  Now scroll to the bottom and tap “About phone” or “About tablet”.  At the “About” screen, scroll to the bottom and tap on “Build number” seven times.  Make sure you tap seven times. If you see a “Not need, you are already a developer!” message pop up, then you know you have done it correctly.


<a id="orgc97c97d"></a>

## 3 . Done! By tapping on “Build number” seven times, you have unlocked USB debugging mode on Android 4.2 and higher. You can now enable/disable it whenever you desire by going to “Settings” -> “Developer Options” -> “Debugging” ->” USB debugging”.


<a id="orgb7dd277"></a>

# TODO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-11 Fri 19:03&gt; </span></span> - Get into it, the programming and control. Learn it. Following <https://source.android.com/source/initializing.html> , have installed the openjdk by     :dev:


<a id="org724cd81"></a>

## sudo update-alternatives &#x2013;config java


<a id="org08d083c"></a>

## sudo update-alternatives &#x2013;config javac


<a id="orge6f9283"></a>

## Think I did what was suggested in <https://source.android.com/source/initializing.html>, on to <https://source.android.com/source/downloading.html>


<a id="org381ca5c"></a>

## UPDATE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-12 Sat 16:24&gt; </span></span> - following along, set up repo in ~/bin/repo. This is a python script "Repo is a tool that makes it easier to work with Git in the context of Android." (from <https://source.android.com/source/downloading.html>


<a id="org1c848a7"></a>

# HOWTO - <span class="timestamp-wrapper"><span class="timestamp">&lt;2015-09-01 Tue 08:14&gt; </span></span> - get the bu353 GPS USB dongle to work: After system start up run PL2303 app. Allow it to take over the GPS function. Then you're ready to go, run Map.Me or other.


<a id="orge1acf9b"></a>

# FINISHED - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-07 Wed 10:25&gt;</span></span>- <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-12-15 Mon 17:10&gt; </span></span> - Get a decent mp3 player setup. Creating and using playlists is important. For doing Spanish going down the road. - WE NOW HAVE ANDROID BLUETOOTH. Game over.


<a id="orgf66be9b"></a>

## NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-12-15 Mon 18:51&gt; </span></span> - One of the biggest PITA is the tag listing. I use files, and want file names. Found 2 apps that play directories directly, trying them.


<a id="org5129b20"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-10-02 Thu 22:54&gt; </span></span> - Dropbox on RCA Android device from Xubuntu, Choose export to save a file to the android disk. Favorite doesn't do it.


<a id="org8724d9c"></a>

# ABOUT - <span class="timestamp-wrapper"><span class="timestamp">&lt;2014-10-02 Thu 22:55&gt; </span></span> The MTP protocol, -


<a id="orga8be452"></a>

## NOTE - <span class="timestamp-wrapper"><span class="timestamp">&lt;2016-09-08 Thu 11:22&gt; </span></span> With the ZTE Avis Plus Z828 phone plugged in and MTP connection chosen on the phone, mount point is *run/user/1000/gvfs* , in that directory there is a file called mtp:gooble-gooble. that's the android file system.

