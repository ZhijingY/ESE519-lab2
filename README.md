# ESE519-lab2

The machine I'm using is MacBook Pro, 13-inch, 2018, macOS version is Big Sur 11.7. Processor is 2.3GHz Quad-Core Intel Core i5. 
To complete the setup, I have cloned the pico-examples and pico-sdk from github. 

I have downloaded [Visual Studio Code](https://code.visualstudio.com/download). Visit the website, and downloaded the macOS version.

I used Homebrew to install all the other softwares. If you don't have Homebrew yet, you can folllow the instruction given in the Pico C SDK Getting Started Guide:

picture

After downloading Homebrew, we can follow the Section 9.1.1 in [Pico C SDK Getting Started Guide](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf) to download CMake and arm-none-eabi-gcc GNU Arm Embedded Toolchain by simply type in the "brew install ..." command in the terminal. 

A serial console is also needed for this lab to view any output from the program running on your board. Screen is a good choice. Simply type "brew install screen" in your terminal. After downloading screen, [here](https://learn.adafruit.com/welcome-to-circuitpython/advanced-serial-console-on-mac-and-linux) is a wonderful guide about how to use it to view the output of your board. Basically to view the output of RP2040 on your terminal, you need to firstly figure out which serial port is assigned to your board. This can be done by typing "ls /dev/tty.*" without 
