ALLSKY CAMERA REPO OVERVIEW

This repository contains CAD files for creating your own mount for an outdoor sky camera using a ZWO planetary camera, intended for use with the INDI-Allsky software.

FILE INDEX:
CAD Files\Allsky Camera (Assembly) v9.step
	STEP file for the whole assembly to visualize assembly
CAD Files\Allsky Camera Base v10.step
	STEP file for the main housing, if it needs to be modified 	for the user
CAD Files\dome seal v1.step
	STEP file for the rubber gasket to seal the dome
Fabrication Files\Allsky Camera Base v10.stl
	STL file of the main housing, ready for 3D printing
Fabrication Files\dome seal v1.dxf
	DXF files of the rubber gasket for laser cutting or 	stenciling
Photos
	Folder of various photos of the system

BILL OF MATERIALS
1x Allsky Camera Base (3D printed from file, ASA plastic recommended)
1x Dome Seal (Laser cut from 1.5mm rubber, or cut with a knife)
4x 4-40 1/2" Screw (McMaster-Carr 91772A110 or similar)
4x 4-40 Nut (McMaster-Carr 91841A005 or similar)
1x 1/4-20 1/2" Screw (McMaster-Carr 91772A537 or similar)
1x ZWO ASI662MC Planetary Camera (Or similar camera with a 62mm diameter, and a 1/4-20 screw in the bottom)
1x ZWO 170° 2.5mm CS Lens (The ASI662MC does come with a 150° 2.1mm lens, but this one is better)
1x Raspberry Pi 4B 4GB (Or better)
1x MicroSD card 128GB (Or better)
1x Acrylic Dome (Amazon https://www.amazon.com/dp/B07L6GLTNP)
1x Rubber Sheet (McMaster-Carr 85785K23 or similar)
4x Generic Wood Screws with Washers

PI Setup
- Download Raspberry Pi OS (64-bit Trixie) from here (https://www.raspberrypi.com/software/operating-systems/). The Lite version can be used for headless operation
- Install the Raspberry Pi Imager from here (https://www.raspberrypi.com/software/)
- Connect the MicroSD card to your PC, and flash the card with the OS using the Raspberry Pi Imager
- Install the MicroSD card in your PI, connect the PI to a monitor, mouse and keyboard, ethernet (Optional, can use WiFi instead), and apply power
- Follow the OS installation instructions
- Install git> sudo apt-get install git
- Clone the INDI-Allsky repo> git clone https://github.com/aaronwmorris/indi-allsky.git
- Navigate to the directory> cd indi-allsky/misc/
- Manually build the application from source and follow the on screen instructions (This takes awhile)> ./build_indi.sh
- Naviagate to the top folder> cd ../
- Install the application, and follow the on screen instructions (Enabling autostart on boot is recommended)> ./setup.sh
- If nothing failed, it should be running the hosted website you can navigate to for viewing the camera and configuring the system. You can check your PI's IP address with> ifconfig

ASSEMBLY
- Print the Allsky Camera Base
- Cut the rubber gasket from the sheet
- Connect the camera to its USB cable, and feed the cable through the hole in the bottom/side of the base, seat the camera in it's pocket (The cable will be a bit of a tight squeeze)
- Using the 1/4-20 screw, thread it into the center hole on the bottom of the base, screwing into the camera to secure it
- Remove the 2.1mm lens that shipped with the camera, and install the 2.5mm lens
- Using the wood screws and washers, mount this to the side of your house/shed or other mounting method
- Once the PI is setup and running, rotate the lens until focus is achieved
- Using the 4-40 screws, insert them into the 4 holes around the edge of the dome from the bottom
- Slide the gasket onto the 4 screws protruding from the bottom
- Slide the dome over the gasket onto the 4 screws protruding from the bottom
- Secure the 4 screws with their nuts