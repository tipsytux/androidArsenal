# Installing and Configuring FRIDA

First we need to understand that this installation requires two steps:

1. Installing the server on the rooted android device
2. Installing the client on the Linux machine

### Step 1: Installing the server 

1. Considering the emulator device to be Genymotion
2. For any other download the respective frida-server from the given website
3. [Website](https://github.com/frida/frida/releases)
4. move the server to the android device using the command 
   1. `adb root`
   2.  `adb push frida-server /data/local/tmp/ `
   3. `adb shell "chmod 755 /data/local/tmp/frida-server"`
   4. `adb shell "./data/local/tmp/frida-server &"`
5. Thus we are done setting up the server.
6. Lets us set up the client now.

### Step 2: Installing the client

1. **Pre-requisites**:
   1. Python 
      1. To install python, the command is `sudo apt-get install python`
   2. Python-pip
      1. To install pip, the command is `sudo apt-get install python-pip`
2. **Downloading FRIDA with pip**
   1. `sudo pip install frida`

### Step3: Testing 

1. **Port Forwarding** 
   1. `adb forward tcp:27042 tcp:27042`
   2. `adb forward tcp:27043 tcp:27043`
2. **Testing** 
   1. `frida-ps -R`

## Some Important Links:

[https://github.com/frida/frida](https://github.com/frida/frida)

[http://www.frida.re/docs/android/](http://www.frida.re/docs/android/)