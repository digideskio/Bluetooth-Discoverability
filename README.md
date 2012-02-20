Bluetooth Always Discoverable
=============================================================

This app will provide a support for leave the bluetooth discoverability of Android phones prior to 2.3.3.

This application works only with *rooted* phones. You need the write permission for the /system/app folder.

The application start a service (even at a system startup time) that, will maintain discoverable the bluetooth adapter.
Using reflection the app will use methods *setDiscoverableTimeout* and *setScanMode* from BluetoothAdapter class, using reflection, and resetting the timer each 100 seconds.


Get started
-------------------------------------------------------------

1. Get the source

    git clone git://github.com/markov00/Bluetooth-Discoverability.git
    

1. Compile and create an *signed* apk with your preferred IDE

1. Mount the /system/app folder with write permission

    mount -o remount,rw -t yaffs2 /dev/block/mtdblock3 /system

1. Push the apk on your sdcard

    adb push BTActive.apk /sdcard/

1. Move the apk inside /system/app folder on your rooted phone.

    cat /sdcard/BTActive.apk > /system/app/BTActive.apk


Tested on
-------------------------------------------------------------
Rooted LG P500 with Android 2.2
Rooted Nexus S with Android 2.3.6 (it has also by default the always discoverability option but I try it only for test purposes)

