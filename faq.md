# <a href="#" id="start"></a>Common Problems and Solutions

## <a href="#" id="one"></a>4.1 do not work suddenly during remote controlling

It may be that the infrared obstacle avoidance module of chassis is activated. Please check whether there is an obstacle around the robot, if so, removing the obstacle, and then wait 5 seconds before try to control remotely again.

## <a href="#" id="two"></a>4.2 Video transferring in a slow speed or delay

Please right-click to close the picture transferring then reopen it. If it does not work, you should not try again until the robot leaves the signal blocked area.

## <a href="#" id="three"></a>4.3 Visual status display "lost" in the picture establishing process, and there are no emerald green points appearing in the black and white screen of picture transferring

There are two situations: 
  a. There is no “tracking” in the visual state after the vision is opened.  
  b. There is a “tracking” in the visual state after it is opened, but It suddenly becomes “lost” in the picture establishing process.

Solutions:  
  a. Try to ensure that the robot moves in a straight line, and moving forward for a while then back for a while, repeating it until the visual status becomes “tracking”.  
  b. Retreat the tolley to nearest position where the visual status appears "tracking" to make the robot vision system relock, in this process, you must keeping the orientation and perspective of the robot unchanged.  c. If both of the two methods are tried several times, it still shows "lost". Please close the vision system and re-open it to start to scan and establish picture from the beginning.


## <a href="#" id="four"></a>4.4 The connection has established and the remote control image transmission is normal, but the client does not display the map and inspection path.

The loading time of the map and inspection path is very long. Please wait for 5 minutes or so. If it still does not appear, please close the client software and reopen it to try again.

## <a href="#" id="five"></a>4.5 The autonomous inspection has been started, the visual status always shows "Lost" and the robot swings in place

It shows that the robot can not identify the current position. There are two possibilities:     a. The current position has not been recorded in the process of scanning and picture establishing.  
  b. The light intensity of current position or distribution of the things has changed a lot. For the first case, please control the robot remotely to the location where the picture establishing has scanned, be sure that the orientation of the robot is the same as picture establishing, and reopen the autonomous inspection again.  For the second case, there is a need to rescan the environment and reestablish the picture, and the inspection path and site are also need to be redrawn.

## <a href="#" id="six"></a>4.6 Cannot close the navigation service

Try to click several times, if it still can not be closed, please close the power switch on the robot chassis manually, and then shut down the trolley host through the client software.

## <a href="#" id="seven"></a>4.7 When planning paths and trajectories, the loaded map shows a lot of messy and blue-colored points or the blue trajectory points of robot are obviously different from the path of remote control when the map is been created

This showed that the establishment of visual map failed. Please rescan and reestablish the map and try again.

## <a href="#" id="eight"></a>4.8 The robot cannot avoid obstacles autonomously

Check the kienct indicator light is normal or not, whether the power cable providing of kienct is connected properly. Turned off the vehicle host, 
then restart to test after reopen it again.

## <a href="#" id="nine"></a>4.9 Client cannot connect to robot

Please log in to the management interface of LAN routing, then check that if both the client PC and the robot host are connected to the network. Refer to Chapter 2 Networking Operations to reset the two networks.
