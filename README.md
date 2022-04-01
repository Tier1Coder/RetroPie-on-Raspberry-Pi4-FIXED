# RetroPie-on-Raspberry-Pi4-FIXED
Using Retropie as an app with Raspberry Pi4 (WITHOUT BUGS AND ERRORS)

HARDWARE:
- Raspberry Pi 4 (in this tutorial I will use 4 to explain the exceptions and bugs that are not in previous versions)
- I'm using monitor with touch for better experience
- Micro SD Card [MSDC] (formatted, FAT32)


✔ - commands (you can copy paste it)

LET'S MAKE IT:
1) We will use Raspberry Pi Imager: https://www.raspberrypi.com/software/
2) Connect MSDC to your computer using adapter and launch the RPI Imager. Select the operating system and choose storage, then write it.
OPERATING SYSTEM - You have to pick the legacy one, (Legacy Buster OS) or something similar. It has bugs on Bullseye, so I highly recommend avoid it.
3) Once you have your system you plug your MSDC to your Raspberry Pi and power it. Then you select location: USA, America, so you have all of your locale settings done (everything will be set to en_US.UTF-8). Move on to the next settings, calibrate your screen and then update everything in your terminal:


4) ✔ sudo apt-get update && sudo apt-get upgrade 

5) After that you can check if your locale settings are correct, so:

✔ locale

Everything should be:

LANG=en_US.UTF-8 
LANGUAGE=en_US:en 
LC_CTYPE="en_US.UTF-8" 
LC_NUMERIC="en_US.UTF-8" 
LC_TIME="en_US.UTF-8" 
LC_COLLATE="en_US.UTF-8" 
LC_MESSAGES="en_US.UTF-8" 
LC_PAPER="en_US.UTF-8" 
LC_NAME="en_US.UTF-8" 
LC_ADDRESS="en_US.UTF-8" 
LC_TELEPHONE="en_US.UTF-8" 
LC_MEASUREMENT="en_US.UTF-8" 
LC_IDENTIFICATION="en_US.UTF-8" 
LC_ALL=en_US.UTF-8 

If it is not set up you can use a tool: 

✔ raspi-config

and then reset this. You can also use nano text editor or direct command, for example: ✔ sudo update-locale LC_ALL="en_US.UTF-8"

6) Now we have to install RetroPie.git:
✔ cd 
✔ git clone --depth=1 https://github.com/RetroPie/RetroPie-Setup.git 

7) Now we use the script to install it:

✔ cd RetroPie-Setup 
✔ chmod +x retropie_setup.sh 
✔ sudo ./retropie_setup.sh 

The RetroPie Setup will launch.

8*) The fix.
AD.1: Go to: Manage Packages -> dependancy packages -> mesa-drm -> install from source
AD.2: Go to: Manage Packages -> dependancy packages -> omxiv -> install from source

9) Now do the Basic Install.

10) After installing (should take about 30 mins) you can launch your RetroPie using:
✔ emulationstation
in your terminal.

Here you go. Your RetroPie works as an APP for Raspberry Pi 4 with Raspberry OS (Raspbian) installed.

You can see my photo to see how cool it is ! :)

ARDUINO GAMEPAD WORKS PERFECTLY WITH THIS ! CHECK MY TUTORIAL FOR MORE!
