Drozer Setup

1. To install the package use the command 

   1. `sudo dpkg -i path\to\the\debianfile\drozer.deb`

2. To add the apk to the genymotion emulator device 

   1. `adb install agent.apk`

3. To access the console of drozer from the workstation we need to port forward

   1. First switch on the embedded server from the app.

      ![img](https://www.packtpub.com/graphics/9781785883149/graphics/B05065_01_50.jpg)

   2. Then we need to start port forwarding.

   3. Use the command 

      1. `adb forward tcp:31415 tcp:31415`

And now we are ready with the setup 

To start the console enter

`drozer console connect`