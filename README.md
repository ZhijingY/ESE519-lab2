# ESE519-lab2

The machine I'm using is MacBook Pro, 13-inch, 2018, macOS version is Big Sur 11.7. Processor is 2.3GHz Quad-Core Intel Core i5. 
To complete the setup, I have cloned the pico-examples and pico-sdk from github. 

I have downloaded [Visual Studio Code](https://code.visualstudio.com/download). Visit the website, and downloaded the macOS version.

I used Homebrew to install all the other softwares. If you don't have Homebrew yet, you can folllow the instruction given in the Pico SDK Getting Started Guide. The magic command for installing brew is given as:

```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

After downloading Homebrew, we can follow the Section 9.1.1 in [Pico C SDK Getting Started Guide](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf) to download CMake and arm-none-eabi-gcc GNU Arm Embedded Toolchain by simply typing in the terminal:

```
$ brew install cmake
$ brew tap ArmMbed/homebrew-formulae
$ brew install arm-none-eabi-gcc
```

A serial console is also needed for this lab to view any output from the program running on your board. Screen is a good choice. Simply type "brew install screen" in your terminal. After downloading screen, [here](https://learn.adafruit.com/welcome-to-circuitpython/advanced-serial-console-on-mac-and-linux) is a wonderful guide about how to use it to view the output of your board. Basically to view the output of RP2040 on your terminal, you need to firstly figure out which serial port is assigned to your board. This can be done by typing ```ls /dev/tty.*``` without connecting the RP2040 to your computer. You will see something like this: 

```
$ /dev/tty.Bluetooth-Incoming-Port
```

Then plug RP2040 to your computer, give the ```ls /dev/tty.*``` command again, a new serial port will show up. That will be the port for RP2040 on your computer. Here I give the example: 

```
$ /dev/tty.Bluetooth-Incoming-Port	/dev/tty.usbmodem14201
```

In this case, ```/dev/tty.usbmodem14201``` is the serial port for your RP2040. Typing ```screen /dev/tty.usbmodem14201 115200``` will bring you to the screen mode in which you can monitor the output of your board.

In your terminal, under a directory you consider proper, type in ```mkdir pico``` to create a folder called "pico", and ```cd pico``` to get into the folder. Then in the "pico" directory, use git to clone the required [PICO-SDK](https://github.com/raspberrypi/pico-sdk) and [PICO-EXAMPLES](https://github.com/raspberrypi/pico-examples) files.

If you don't have or never use git, [install it on your computer](https://git-scm.com/download/mac). After installing git onto your computer, clone the files to local "pico" folder by the commands:

```
$ git clone -b master https://github.com/raspberrypi/pico-sdk.git
$ cd pico-sdk
$ git submodule update --init
$ cd ..
$ git clone -b master https://github.com/raspberrypi/pico-examples.git
```

If difficulty is met when cloning the pico files, you can also download the files manually by clicking the green "Code" button and choose "Download ZIP". Put the downloaded "pico-sdk" folder and "pico-examples" folder into the "pico" folder. 
