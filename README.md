# Z390-Hackintosh-Joost
This is my Hackintosh build using a Z390 Designare, i7, RX 6800 XT, 32GB RAM and Fenvi T919.

![alt test](/Pictures/Z390info1.png)
![alt test](Pictures/RX6800XT-hackintosh2.jpg)
![alt test](Pictures/RX6800XT-hackintosh1.jpg)
![alt test](Pictures/22090947.png)

# PC specifications:
- OS's installed: MacOS Monterey dualbooted with Windows 10 Pro
- PC Case: Fractal Design Define R6 USB-C TG
- Processor: Intel Core i7 9700K, 9th Gen (Code name: Coffee Lake)
- Motherboard: Gigabyte Z390 Designare
- Sound card (onboard): ALC 1220-VB audio controller
- SSD storage: Crucial Crucial MX500, 1TB 
- Graphic card: RX 6800 XT 16GB (previously I used the Sapphire Nitro+ Radeon RX 570 4GD5)
- Fenvi T919 for WiFi/Bluetooth, AirDrop, Apple Watch Unlock, etc.
- Power Supply: Be quiet! Dark Power PRO 11 850W
- Memory (RAM): Corsair Vengeance LPX (2x 16GB, total 32GB)
- Display: iiyama G-Master GB3466WQSU-B1 UltraWideScreen, 34 inch.
- Cooling system: Cooler Master ML360R RGB 
- Stably overclocked the CPU to 5GHz, 1.370 Volt. According: https://www.youtube.com/watch?v=6Sk4ISqmL88
  - Temperature IDLE (Still doing basic things ie. Music on, using Safari etc.): 30 degrees Celcius
  - Stress tested: 50-60 degrees Celcius:
  
 ![alt test](/Pictures/Temp.png)

# Notes:
- I'm not responsible for any harm done to your PC :-) Use my experiences and EFI at your own risk.
- Everything I did went according @CaseySJ his outstanding guides on:
https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/

# Create your USB stick with your pre-made as follows:
https://github.com/joostiphone/MacOS-USB-Installer

 ![alt test](/Pictures/USB-Stick-Logo-MacOS-small.png)

# BIOS Settings (from tonymacx86.com):
https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/
PS: make sure you AVOID BIOS version F9j. A modified F9i version (with the security fixes from Fgj) can be found here:
https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-3038#post-2239464

# Monterey on OpenCore
Monterey with OpenCore is working very well. A small how-to here: 

PRECAUSION:
- I'm using OpenCore. You can download the latest build from here which you can use during the EFI creation as per below (or use mine...):
-  https://github.com/acidanthera/OpenCorePkg/releases
- Also great info from: https://dortania.github.io/OpenCore-Install-Guide/extras/big-sur/#backstory

- USB preparation and installation of Monterey according this video:
https://www.youtube.com/watch?v=x6fZcFIT82c
- Create your EFI:
https://www.youtube.com/watch?v=XyDJMNMFi6I&t=58s
- When the EFI is done, add your SSDT's and DTSD's to the EFI partition using OpenCoreConfigurator to mount the EFI
- After that, create your own Serial Number using OpenCoreConfigurator

# Serial number:
You need to make your own serial number, so that your iCloud etc. will work without using someone else his serial number. In OC GEN-X or in OpenCore Configurator you can generate a new one if you don't have one yet, or if you need a new one.

# Updating Hackintosh (MacOS)
https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/
- Make sure you're using the latest stable release of OpenCore and that it works (you can use my efi as per below, or you can update OpenCore yourself)
- In general; watch others do first to see if they succeed
- Make sure first to install the latest Kext files
- Install latest OpenCore; but first make sure that this works according other users. Latest OpenCore build:
https://github.com/acidanthera/OpenCorePkg/releases

# Kexts:
Make sure (!) you are using the latest kexts: 

- AppleALC.kext
https://github.com/acidanthera/applealc/releases
- IntelMausi.kext
https://github.com/acidanthera/IntelMausi/releases
- SMCProcessor.kext
It's part of the VirtualSMC zip as per below kext
- USBInjectAll.kext
https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/
- Lilu.kext
https://github.com/acidanthera/Lilu/releases
- WhateverGreen.kext
https://github.com/acidanthera/WhateverGreen/releases
- VirtualSMC.kext
https://github.com/acidanthera/VirtualSMC/releases

For convenvience purposes, use either OpenCore Configurator or Hackintool to mount EFI and update the Kexts. I always provide the latest Kexts in my EFI as per below.

# Update your OpenCore EFI (small how-to)
![alt test](Pictures/OpenCoreUpdate.png)

 # Option 1: Update using HackinDROM 
 Download the app here:
 https://hackindrom.zapto.org 
 
 and watch a how-to here:
 https://www.youtube.com/watch?v=xRuerrG-lAU&t=50s

 # Option 2: Manually
 https://github.com/joostiphone/Update-OpenCore-to-latest-version


# Latest Changes in uploaded Monterey and Big Sur EFI (without a Serial Number):
Please note that I only use the latest Stable released versions of MacOS and OpenCore (so no beta's, nighly builds or latest commitments).

(Item 0 is the oldest):

0. Installed my system succesfully using OpenCore v0.6.0
1. Tweaked it
2. Updated to Beta 3
2b. 30-7-2020 15h42 OC060 BigSurB3 NoSN.zip
3. Updated OpenCore from scratch to OpenCore v0.6.0 commitment 0e81540 via: https://github.com/williambj1/OpenCore-Factory/releases
3a. 2-8-2020 11h09 OC060 new BigSurB3 NoSN.zip
4. Updated to Beta 4
5. Updated to Public Beta (which I guess is the same as b4). 
6. 13-Oct-2020: Updated to latest Public Beta (20A5384c) and latest final OpenCore Build (v0.6.2). This is now my main system due to its stability :-)
7. 2-Nov-2020: Updated to latest Public Beta (20B5012d), 11.0.1. and OpenCore to v0.6.3.
8. 19-Dec-2020: Updated OpenCore to v0.6.4.
9. 25-Dec-2020: Update to MacOS 11.1 (20C69)
10. 12-Jan-2021: Updated OpenCore to v0.6.5.
11. 4-Feb-2021: Updated to MacOS 11.2 (20D64), using OpenCore v0.6.5.
12. 5-Feb-2021: Updated OpenCore to v0.6.6.
13. 11-Feb-2021: Updated to MacOS 11.2.1 (20D74), using OpenCore v0.6.6.
14. 22-Feb-2021: Small tweaks in EFI. Added Background.ICNS in Resources/Images folder (you can delete this if required). Also, OpenShell has been hidden now.
15. 28-Feb-2021: Updated to MacOS 11.2.2 (20D80), using OpenCore v0.6.6.
16. 9-March-2021: Updated OpenCore to v0.6.7 and to MacOS MacOS 11.2.3 (20D91).
17. 6-April-2021: Updated OpenCore to v0.6.8.
18. 28-April-2021: Updated to MacOS 11.3 (20E232), using OpenCore v0.6.8.
19. 9-May-2021: Updated to MacOS 11.3.1 (20E241), using OpenCore v0.6.9.
20. I'm now using HackinDROM to update the OpenCore EFI. Find a how-to video here on how to use HackinDROM and how to update OpenCore: https://www.youtube.com/watch?v=xRuerrG-lAU
21. 12-6-2021: Updated to MacOS 11.4 (20F71), and updated to OpenCore v0.7.0.
22. 11-7-2021: Updated to MacOS Monterey 12.0 beta (21A5268h), and updated to OpenCore v0.7.1.
23. (next update will include support for Monterey Beta 8 using OpenCore v0.7.4.). 
24. 11-10-2021: Updated to MacOS Monterey Beta 10, and updated to OpenCore v0.7.4 (plus a fix for Windows black-screen). And I changed the OpenCore Boot screen visual-wise as per my likings.
25. 8-11-2021: Updated to MacOS 12.0.1 (21A559), and updated to OpenCore 0.7.5.
26. 5-12-2021: Updated OpenCore to v0.7.6.
27. 23-12-2021: Updated to Mac OS 12.1 (21C52)

# Download my latest BEFI here (zip file):
![alt test](Pictures/Apple-icon.png)

Download here, supports Monterey or Big Sur. The EFI is without my serial number, so you need to enter your own using OpenCore Configurator:

Big Sur OpenCore:
https://mega.nz/folder/l9xGHQQC#63JkmaR5IT3ONQ4G1RmfLQ

Monterey OpenCore:
https://mega.nz/folder/k8hwSIzB#K1b4jyXhH0XtVsxhJr9mSw

![alt test](Pictures/2021-10-17_09-23-07.png)


# Confirmed working:
CPU, RAM, Fans, Cooling etc. ✔
Audio ✔
Ethernet ✔
Graphics ✔
HDMI ✔
Sleep/wake Function ✔
Power Management ✔
App Store ✔
iMessage ✔
iCloud ✔
FaceTime ✔
USB with 2.0, 3.0, 3.1 and USB Type-C Ports ✔
Bootloader ✔
HDMI Audio ✔
Volume Hotkeys ✔
WiFi (Fenvi) ✔
Bluetooth (Fenvi) ✔
AirDrop (Fenvi) ✔
HandOff ✔ 
Side Car ✔ As you can see here using my regular display and iPad Pro:

![alt test](Pictures/sidecar.png)

# Optional: Overclocking Z390 Designare, i7-9700K to 5Ghz 
Some basic settings, but you can still look at the attached BIOS screenshots for further details:
- CPU Base Clock: 100Mhz
- Extreme Memory Profile (XMP): Profile 1
- CPU Vcore: 1.370V (instead of standard 1.200V). This is pretty high and cause degration of your CPU, just be aware...
- Active Turbo Ratios: Enabled, and set every core on 50 (50 times 100Mhz CPU Base Clock = 5000Mhz).
- C-States Control: Enable (disable all options there)

![alt test](Pictures/cinebench.png)

BIOS Overclock Settings (BIOS Screenshots)
https://mega.nz/file/NxxG2AbI#AvhLcGAFm98mz7CnLYa2zVFylmE6mv70xCRrGh2bJQ4

# Credits:
https://github.com/joostiphone/Credits/blob/main/README.md

# Resources
- https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/
- https://www.tonymacx86.com/threads/success-working-intel-wifi-drivers-for-7265ac-on-catalina.292207/post-2131153
- https://hackintosh.gitbook.io 
- https://dortania.github.io/OpenCore-Install-Guide/extras/big-sur/#backstory
- https://github.com/acidanthera/OpenCorePkg/releases
- https://github.com/williambj1/OpenCore-Factory/releases
- https://mackie100projects.altervista.org/download-opencore-configurator/
- https://github.com/Pavo-IM/OC-Gen-X
- https://github.com/Pavo-IM/ocbuilder
