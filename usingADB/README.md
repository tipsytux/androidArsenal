# ADB Cheat Sheet

1. `adb devices`
   1. Prints the list of all the devices attached.
2. `adb shell`
   1. This command will give us a shell, when only one device is connected.
3. `adb -e shell`
   1. The command to get a shell for the emulator when a real device and an emulator are connected.
4. `adb -d shell`
   1. The command to get a shell for the real device when a real device and an emulator are connected.
5. `adb -s [name of the device]`
   1. The command to get a shell for a specific target when multiple devices/emulators are connected.
6. `pm list packages`
   1. The command is used to list down all the packages that have been installed.
7. `adb push [file on local machine][location on the device]`
   1. The command is used to copy a file from the local machine to the device.
   2. The location on the device that is externally writable is ***/data/local/tmp/*** 
8. `adb pull [file on the device]`
   1. The command is used to download a particular file from the device to the current working directory.
9. `adb install [filename.apk]`
   1. The command is used to install an apk named filename.apk (that is present in the current working directory) on the device.
10. `adb kill-server`
    1. The command kills the adb daemon and restarts the server for us.