# <a href="#" id="start"></a>Chapter 2, Remote Control Image Transmission

## <a href="#" id="config"></a>2.1 Configuration of robotic vehicle computer network

Place the battery flat on the empty area in front of the host (the battery is blocked by the camera bracket), connect the chassis power wire according to the prompt of line mark, install the wifi antenna of host computer, insert the u turn string module into the computer usb port, and plug in the camera and kinect. Press the chassis red switch and the host computer switch simultaneously, use the hdmi we give to vga plug,  connect the monitor, keyboard and mouse to the robot host and then boot, enter the user password and access to the host ubuntu system. System password is xiaoqiang.

![remote-1](/images/remote-1.png)

Click on the location shown below to select the wireless network which you want to access to.

![remote-2](/images/remote-2.png)

When there are many wifi hotspots around the use environment, 5G networks is recommended. This is because 5G network has less electromagnetic interference, more stable transmission and more effective coverage. If the network coverage of a route is too small, multiple 5G routing wireless bridges can be connected into the same wireless network. The robot access to the large-scale network can expand the ranger of remote control image transmission.

## <a href="#" id="network"></a>2.2 Control terminal PC accesses the working network

The control terminal PC needs to be on the same wireless network as the trolley host. Please refer to Chapter 1 for the installation of control software.

![remote-3](/images/remote-3.jpg)

## <a href="#" id="control"></a>2.3 Operation of control terminal software 

After opening control software, the initial interface is shown in the figure below. Put mouse pointer in any area, the corresponding function prompt will appear. Please try to understand the entire interface as you want.

![remote-4](/images/remote-4.png)

### <a href="#" id="open"></a>2.3.a The opening of remote control image transmission

First of all, make sure that the onboard computer and the chassis are powered on. The power button is on the left side of the host. Led lights in the front of the kinect will blink after the host computer is turned on. The chassis switch is next to the digital tube. The digital tube will display the battery voltage after the chassis is powered on. Please charge the battery When its voltage is lower than 9.8V.

`Click` the button `"Not Connected"` on the main interface to establish the communication link between the remote control and the chassis. It will pop up the following warning on the firewall when in the first operation. Please select "Allow access".

![remote-5](/images/remote-5.png)

After the connection is successful, the main interface becomes as shown in the figure below. Now you can start the remote control chassis movement.

![remote-6](/images/remote-6.png)

Chassis motion control `supports keyboard` manipulation. The operation style is similar to the game Need for Speed.

`Right-click` in the picture transferring area to open the menu, as is shown in the figure below.

![remote-7](/images/remote-7.png)

Select `"Original Image"` , now you can see the first view of the robot and picture transferring has already been opened.

![remote-8](/images/remote-8.png)

Select `"Close"` in the right-click menu to end the picture transferring.

### <a href="#" id="close"></a>2.2.b The closing of remote control video transmission

Close the software directly. If you need to turn off the power of the device, please click the button “Shutdown” on the main interface to turn off the vehicle host firstly, then turn off the switch next to the digital tube of trolley chassis. Ensure that the host computer is turned off (kienct stops blinking) , unplug the wire between battery and trolley chassis.

Demonstration video of this chapter:

[Operation of Remote control video transmission](https://www.bwbot.org/s/sYYkyd)

`Please manually press the red switch on the trolley plate to stop the car in case of emergency.`