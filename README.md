# Everybot 2023

Always follow the resources provided by OCS Robotics WPILIB 

https://sites.google.com/view/ocs-robotics/resources

## SET UP DRIVING TOOL 
1. FRC Game Tools provides components that help FIRST Robotics Competition (FRC) participants manage and communicate with robots.
	FRC Game Tools is a software bundle that includes the FRC Driver Station and FRC Utilities. These components are required for FRC teams to 		configure and control robots and communicate with the field. The bundle also includes optional LabVIEW APIs for FRC teams using the LabVIEW 		programming language. FRC Game Tools is a required installation for all FRC participants.

## Steps 
<b> First set up the driving program to control the Robot. </b>
- FRC Game Tools
<b> Liink </b> 
(https://www.ni.com/en-us/support/downloads/drivers/download.frc-game-tools.html#369633)

- click next and install everything in the download package 

- exit the login page that pops up 
<img width="340" alt="Screen Shot 2023-02-21 at 9 07 18 PM" src="https://user-images.githubusercontent.com/123269897/220511193-0f1272e0-81ca-4e8c-9663-840bc913e64b.png">

## REBOOT COMPUTER AFTER COMPLETE INSTALL

<img width="340" alt="Screen Shot 2023-02-21 at 9 07 18 PM" src="https://user-images.githubusercontent.com/123269897/220512445-4eaa6f3a-3707-4c4e-9206-aa52be0dc080.png">

### after reboot 
Launch FRC Driver Station 

![Screen Shot 2023-02-21 at 9 18 11 PM](https://user-images.githubusercontent.com/123269897/220512639-2fd5f31d-d8b0-41f5-a10d-daa26ff5c84d.png)

### Add the WPILIB FRAMEWORK that is used in FRC for the robot must have the library in labview(VS Code)
<img width="340" alt="Screen Shot 2023-02-21 at 9 21 32 PM" src="https://user-images.githubusercontent.com/123269897/220513365-66a6962b-ab61-431e-9b0d-8fcfe1301200.png">

## Last Framework to Install 

(https://store.ctr-electronics.com/software/)

<p> It provides a variety of functionality to support all Phoenix CAN Bus devices. The feature set includes:

	Update device firmware (including PDP/PCM). Change CAN IDs

	Configure direction and offsets

	Self-test Snapshot devices

	Change configuration settings

	Factory default configuration settings

	Test motors

	Check plots

	Temperature Calibrate Pigeon-IMU
Confirm proper CAN bus wiring without writing any software.
Now you can drive your motors and collect data without writing any software.
	
	
	
# FQA IF ERRORS OCCUR
(https://docs.wpilib.org/en/stable/docs/yearly-overview/known-issues.html)	
	
### Prior To Departing For The Competition
Dedicate a laptop to be used solely as a driver station. Many teams do. A dedicated machine allows you manage the configuration for one goal – being ready to compete at the field. Dedicated means no other software except the FRC-provided Driver Station software and associated Dashboard installed or running.

Use a business-class laptop for your driver station. Why? They’re much more durable than the $300 Black Friday special at Best Buy. They’ll survive being banged around at the competition. Business-class laptops have higher quality device drivers, and the drivers are maintained for a longer period than consumer laptops. This makes your investment last longer. Lenovo ThinkPad T series and Dell Latitude are two popular business-class brands you’ll commonly see at competitions. There are thousands for sale every day on eBay. The laptop provided in recent rookie kits is a good entry level machine. Teams often graduate from it to bigger displays as they do more with vision and dashboards.

Consider used laptops rather than new. The FRC® Driver Station and dashboard software uses very few system resources, so you don’t need to buy a new laptop – instead, buy a cheap 4-5 year old used one. You might even get one donated by a used computer store in your area.

<b> Laptop recommended features </b>
	- RAM – 4GB of RAM

	-A display size of 13” or greater, with minimum resolution of 1440x1050.

	-Ports

	-A built-in Ethernet port is highly preferred. Ensure that it’s a full-sized port. The hinged Ethernet ports don’t hold up to repeated use.

	-Use an Ethernet port saver to make your Ethernet connection. This extends the life of the port on the laptop. This is particularly important if 	 you have a consumer-grade laptop with a hinged Ethernet port.

	-If the Ethernet port on your laptop is dodgy, either replace the laptop (recommended) or buy a USB Ethernet dongle from a reputable brand. Many 	 teams find that USB Ethernet is less reliable than built-in Ethernet, primarily due to cheap hardware and bad drivers. The dongles given to 		rookies in the KOP have a reputation for working well.

	-2 USB ports minimum

	-A keyboard. It’s hard to quickly do troubleshooting on touch-only computers at the field.

	-A solid-state disk (SSD). If the laptop has a rotating disk, spend $50 and replace it with a SSD.

	-Updated to the current release of Windows 10 or 11. Being the most common OS now seen at competitions, bugs are more likely to be found and 		fixed for Windows 10 and 11 than on older Windows versions.

	-Install all Windows updates a week before the competition. This allows you time to ensure the updates will not interfere with driver station 		functions. To do so, open the Windows Update settings page and see that you’re up-to-date. Install pending updates if not. Reboot and check 		again to make sure you’re up to date.

	-Change “Active Hours” for Windows Updates to prevent updates from installing during competition hours. Navigate to Start -> Settings -> Update & 	Security -> Windows Update, then select Change active hours. If you’re traveling to a competition, take time zone differences into account. This 	will help ensure your driver station does not reboot or fail due to update installing on the field.

	-Remove any 3rd party antivirus or antimalware software. Instead, use Windows Defender on Windows 10 or 11. Since you’re only connecting to the i	nternet for Windows and FRC software updating, the risk is low. Only install software on your driver station that’s needed for driving. Your 		goal here is to eliminate variables that might interfere with proper operation. Remove any unneeded preinstalled software (“bloatware”) that 		came with the machine. Don’t use the laptop as your Steam machine for gaming back at the hotel the night before the event. Many teams go as far 	as having a separate programming laptop.

	-Avoid managed Windows 10 or 11 installations from the school’s IT department. These deployments are built for the school environment and often 		come with unwanted software that interferes with your robot’s operation.

	-Laptop battery / power

	-Turn off Put the computer to sleep in your power plan for both battery and powered operation.

	-Turn off USB Selective Suspend:

	- Right click on the battery/charging icon in the tray, then select Power Options.

	- Edit the plan settings of your power plan.

	- Click the Change advanced power settings link.

	- Scroll down in the advanced settings and disable the USB selective suspend setting for both Battery and Plugged in.

	- Ensure the laptop battery can hold a charge for at least an hour after making the changes above. This allows plenty of time for the robot and 		drive team to go through the queue and reach the alliance station without mains power.

	- Bring a trusted USB and Ethernet cable for use connecting to the roboRIO.

	- Add retention/strain relief to prevent your joystick/gamepad controllers from falling on the floor and/or yanking on the USB ports. This helps 		prevent issues with intermittent controller connections.

	- The Windows user account you use to drive must be a member of the Administrator group.

## At The Competition
Turn off Windows firewall using these instructions.

Turn off the Wi-Fi adapter, either using the dedicated hardware Wi-Fi switch or by disabling it in the Adapter Settings control panel.

Charge the driver station when it’s in the pit.

Remove login passwords or ensure everyone on the drive team knows the password. You’d be surprised at how often drivers arrive at the field without knowing the password for the laptop.

Ensure your LabView code is deployed permanently and set to “run as startup”, using the instructions in the LabView Tutorial. If you must deploy code every time you turn the robot on, you’re doing it wrong.

Limit web browsing to FRC related web sites. This minimizes the chance of getting malware during the competition.

Don’t plan on using internet access to do software updates. There likely won’t be any in the venue, and hotel Wi-Fi varies widely in quality. If you do need updates, contact a Control System Advisor in the pit.

## Before Each Match
Make sure the laptop is on and logged in prior to the end of the match before yours.

Close programs that aren’t needed during the match – e.g., Visual Studio Code or LabView – when you are competing.

Bring your laptop charger to the field. Power is provided for you in each player station.

Fasten your laptop with hook-and-loop tape to the player station shelf. You never know when your alliance partner will have an autonomous programming issue and blast the wall.

Ensure joysticks and controllers are assigned to the correct USB ports.

In the USB tab in the FRC Driver Station software, drag and drop to assign joysticks as needed.

Use the rescan button (F1) if joysticks / controllers do not appear green

Use the rescan button (F1) during competition if joystick or controllers become unplugged and then are plugged back in or otherwise turn gray during competition.

## TO RUN THE CODE CONNECT YOUR ROBO RIO RADIO 
## Programming Radio 
	https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-3/radio-programming.html#prerequisites
	# Prerequisites
The FRC Radio Configuration Utility requires administrator privileges to configure the network settings on your machine. The program should request the necessary privileges automatically (may require a password if run from a non-administrator account), but if you are having trouble, try running it from an administrator account.

Download the latest FRC Radio Configuration Utility Installer from the following links:

FRC Radio Configuration 23.0.2

FRC Radio Configuration 23.0.2 Israel Version

Before you begin using the software:

Disable all other network adapters

Plug directly from your computer into the wireless bridge ethernet port closest to the power jack. Make sure no other devices are connected to your computer via ethernet. If powering the radio via PoE, plug an Ethernet cable from the PC into the socket side of the PoE adapter (where the roboRIO would plug in). If you experience issues configuring through the PoE adapter, you may try connecting the PC to the alternate port on the radio.	
