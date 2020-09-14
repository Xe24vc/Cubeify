This is still an early work in progress so expect bugs. Please only use this on a clean Ubuntu 20.04 Focal Fossa install.
I'm not responsible for any lost data or hardware damage that may result.

# Cubeify
A Linux environment tailored to running Dolphin-Emu as a front end using the GC Bios (Must be legally accquired).
Specifically designed for use on a DeskMini A300/X300 with a Ryzen5 3400g.

![alt text](https://github.com/Xe24vc/Cubeify/blob/master/Examples/Bios.png)

Notice:
There is no copyrighted content included in this repo or any of the associated repos.
The bios file (IPL.bin) which is required to use Cubeify and any roms must be dumped yourself legally.
Do not ask for any copyrighted material.

Cubeify can be built on Ubuntu 20.04 LTS Focal Fossa using the provided scripts and following the directions below.

1) Clone or download this repo and copy the "Cubeify" folder to /home/"Your Username"/Documents.

2) Open a terminal and navigate to Cubeify, then make the first script executable ("chmod a+x ./00_Setup_Pt1.sh").

3) Execute the script ("./00_Setup_Pt1.sh") and go grab a coffee as this can take awhile.

4) When it finishes reboot your machine and navigate back to Cubeify. Then execute the script ("00_Setup_Pt2.sh").
   During this process you should notice the top bar, desktop icons, and several other things are hidden.
   Don't worry you can configure these settings as you wish in Gnome-Extensions & Gnome-Tweak-Tools.
   
5) When it finishes again, start Dolphin by typing "dolphin-emu" in terminal. At this point you can configure Dolphin how you like.
   You will need to copy a legally acquired IPL.bin to the proper location for your region (Google this if you don't know how).

6) Once you are done setting up Dolphin, you can execute the script ("01_Startup.sh").
   This will auto start Dolphin any time it is not already running.
   To stop the loop at any time press [/] is the terminal window.
   Doing so will let you close Dolphin without it restarting.
   
Notes:
You can hide Ubuntu's Dock with [Alt+9] or show it with [Ctrl+9].

To load games on the GC Bios use (A+B+DPad_Down) on the controller or change the "Change Disc" hotkey in Dolphin.
When the file browser is up you can navigate it using the DPads and select a file using the start button.

If you are using this on a DeskMini A300 there is an option to max all of the clock speeds on the 3400G.
Setting OC=1 in 01_Startup.sh will result in all cores running at 4.1GHz with Core Performance Boost enabled.
Or 3.7GHz with Core Performance Boost disabled. Change this setting in UEFI Bios.

It also sets the minimum clock speed for the Vega GFX at 1.2GHz to prevent slow downs in Paper Mario.
