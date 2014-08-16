Bash scripts for Android Wear
==================

Do you write apps for Android Wear, do much testing or you just want to take a screenshot? Probably you know it isn't great or fun to do that many times a day - even connecting via Bluetooth to debug mightbe hard as command is long.

###How is it helping?
It connects to your watch and generate scripts for most used actions for that connection (so no need to write each time `adb -s localhost:4444` and action command). You just run script to get the output!

###Script list

**screenshot** - it takes a screenshot of your watch screen and automatically send it to your command line location with random name.

**listPackages** - obtain full list of installed software on your Wear.

**install app.apk** - installs app from selected APK.

**uninstall package_name** - be carefoul with it.


###How to run

You might need to set permissions for a `main.sh` with a command `chmod 777 main.sh`.
To run scripts for a connection via Bluetooth ([all that is in one script] (https://developer.android.com/training/wearables/apps/bt-debugging.html)), your phone in companion app needs to show:
"Host:disconnected, Target:connected"
to connect and generate all scripts for that connection just run `./main.sh`.

EXTRA: You can connect to your watch via USB cable, in such case before running main.sh run `adb devices` copy watch ID and use it like that `./main.sh DEVICE_ADB_ID`.


After that you are ready to run other script (listed in **scripts** section), for example type in command line `./screenshot.sh` to obtain a screenshot!
