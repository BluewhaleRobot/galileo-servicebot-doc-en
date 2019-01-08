# <a href="#" id="start"></a>Chapter 3, Navigation

## <a href="#" id="intro"></a>3.1 System introduction

The vehicle host computer is equipped with a visual navigation system. The robot trolley can move and inspect autonomously with the system, When encountering obstacles, the trolley will also autonomously dodges and bypass.

Navigation system workflow::

(1) In the mode of remote control image transmission, the operator controls the device remotely to surround the motion area for twice to establish a visual map that the robot can understand.

(2) Draw the inspection trajectory of robot and set the target point manually on the visual navigation map created in step 1 using the control software.

(3)Start the inspection after the path and target point are set. Selecting the target point, then the robot will move utonomously to the target point along the trajectory planned in step 2.

## <a href="#" id="create"></a>3.2 The creation of map

Opening the remote control image transmission according to the operation in Chapter 2, set the speed of chassis movement as about 20%. Click the button“ Start Drawing” on the main interface and wait 10 seconds.

![nav-1](/images/nav-1.png)

Open the visual system output image.

![nav-2](/images/nav-2.png)
![nav-3](/images/nav-3.png)

Telerobot moves straight forward until the vision system initializes successfully.

![nav-4](/images/nav-4.png)

Now starting of the vision system has been finished, the telerobot begins to moving in the movement area. Try to avoid pure rotation in the process of remote control (just pressing the key turn left or right wil cause the lost of vision system for targets easily). Please press the key forward and turn left or right simultaneously so as to turn the robot along the large radius trajectory.

During remote control, please make sure that the visual indication status in the main interface is `"Tracking"`. Once it becomes red `"lost"`, please retreat the telerobot to the normal state of previous period. You must use the back button to finish the retreating process, at the same time, keep the orientation and perspective of the robot unchanged.

Please do not operate the robot temporarily if `"Closed loop optimization"` appears in the Visual indication status during remote control. When the path that the robot walks forms a circle, the robot will automatically optimize the map established previously, which will greatly improve the quality of the map. Therefore, in order to establish a more accurate map, you can remotely control the robot to walk multiplely along closed paths in the process of establishing a map. Importantly, the quality of the map will greatly influence the effect of navigation later.

When the robot has browsed the entire motion area, stop moving, click the button "Save Map" on the main interface, and wait for the save dialog to pop up. Enter the name of map in the dialog and click  "OK ". Wait for the map to finish loading.

![nav_5](/images/nav-5.png)

After the map is loaded, you can see the approximate effect of the map which you just established. If you feel more satisfied, you can click the button " Finish Map ". Then the section about establishment of map is finished.

The demo video of this section:

[The process of Visual map creation.](https://www.bwbot.org/s/H3B6xC)

`In case of emergency, please press the red switch manually on the trolley to stop it.`

## <a href="#" id="draw"></a>3.3 The drawing of inspection trajectory and site

`Warning: Because planning trajectory need to download and render the visual map,  the client exchange large amounts of data with the trolley host, the whole process takes a long time. So for the execution of the following steps, please waiting for the update of the client software interface patiently.`

Open the control software, click the button "Unconnected" to connect with the chassis, click on the button" draw navigation map" to open the editing interface of inspection path on the main interface.

![nav-6](/images/nav-6.png)

After loading, the software interface is similar to the figure below.

![nav-8](/images/nav-8.png)

### <a href="#" id="draw-path"></a>3.3.a Drawing the inspection trajectory

The inspection trajectory is the path you want the robot to walk on. After clicking the button "Start Navigation" on the main interface, the robot will move according to the path you have drawn. Here, we will introduce how to use the path drawing tool.

  - ![nav-9](/images/nav-9.png) 1. Basic operation

    Basic operations contain pan and zoom. Panning of the map is achieved by draging the map with the left mouse button. Zoom of the map is achieved by scrolling he mouse forward and backward. This is very useful for drawing paths. For more detailed requirements about movement, you can enlarge it before drawing.
  - ![nav-10](/images/nav-10.png) 2. Pencil tool

    Click the pencil icon in the left toolbar. This is a straight line tool. Click on any point with left mouse botton on the graph, then move the mouse, there will appear a red straight line. Move the mouse to the end position you want and click the left mouse button, a straight line is drawn. If you click the left button once again, then click right mouse button to cancel this drawing.
  - ![nav-11](/images/nav-11.png) 3. Eraser tool

    Click the Eraser tool on the left toolbar, then click the left mouse button and drag to erase the points drawn previously.
  - ![nav-12](/images/nav-12.png) 4. Curve tool

    Click the curve tool on the left toolbar, click the left mouse button at the beginning of the curve, and then click it in the middle of the curvea and the endpoint of the curve respectively. Such a curve is drawn.
  - ![nav-13](/images/nav-13.png) 5. Remove tool

    If you want to delete the points you drawn previously in a wide range, you can use this removal tool. Click on the delete tool on the left toolbar, and then put left mouse click on the starting point of the deletion, at this moment,  you can see a rectangle always moves with the mouse. Click the left mouse button again to delete the area selected by rectangle. Right click to cancel the selection.

You can draw the inspection trajectory of the robot with those tools. It should be noted that you draw the line (blue dot) along the original trajectory as much as possible to ensure that the path is smooth during the movement. You can see the terrain roughly from the green point on the map, and then draw the points allowed by the range of motion based on this information. For service robot, mode trajectory is connected.

![nav-14](/images/nav-14.png)

### <a href="#" id="draw-station"></a>3.3.b Set target point

With respect to the application scenarios of service robot, the robot needs to move back and forth between several fixed positions. For example, from the kitchen to the first table, then back to the kitchen to the second table and so on. The following work is to mark the location of each target point on the route map drawn above. We can send the corresponding target point to the robot, and then let the robot go to the target point automatically.

Click on ![nav-15](/images/nav-15.png) to activate the inspection site insertion tool, and click on the inspection trajectory in order to insert inspection sites. Inspection  sites can be deleted by erasing and deleting tools.

![nav-16](/images/nav-16.png)

Enter the corresponding target point number in the currently selected navigation point below, and the corresponding target point will be displayed in green in the figure. We can know the serial number of each target point in this way.

![nav-100](/images/nav-100.png)

![nav-20](/images/nav-20.png)

### <a href="#" id="save-path"></a>3.3.c Save the trajectory and upload

Click the button "Save Path" on the interface, enter the file name, and click "Save".

![nav-17](/images/nav-17.png)

![nav-18](/images/nav-18.png)

The full demo video about this sector:

[Draw the planning path and target point](https://www.bwbot.org/s/pY3uAg)

## <a href="#" id="open-close"></a>3.4 Openning and closing of autonomous inspection

Open the control terminal software and click the button "Not Connected" to connect with the chassis. Waiting for the map download to complete, the client loads a few sections drawn navigation map and path site automatically.

![nav-19](/images/nav-19.png)

![nav-21](/images/nav-21.png)

![nav-22](/images/nav-22.png)

`Control the robot remotelyled to the position where it can be tracked. Of course, the robot must be in the inspection path and its facing orientation should be the same as the map you have created.`

Click the button "Start navigation" to start the automatic inspection, wait 30 seconds or so for the robot to start to move autonomously, and the blue blocks that indicate the location of the robot in the interface begin to be updated synchronously.

![nav-23](/images/nav-23.png)

![nav-23-1](/images/nav-23-1.png)

![nav-23-2](/images/nav-23-2.png)

If you want to stop the inspection, click on the button "Stop Service".

If the robot suddenly stops moving during the autonomous inspection process, and the visual status becomes “lost”, which means that the vision system loses the targets. The reasons for that may be the following: (1) The initial movement direction of the robot is opposite to the movement direction when the map is established; (2) the light intensity or the environment has changed tremendously. For reason (1), please restart the robot after turn it around. For reason (2), you need to re-esablish the map and planning path.

The full demo video of this section:

[Openning and closing of autonomous inspection](https://www.bwbot.org/s/fBYkCv)

`In case of emergency, please press the red switch manually on the trolley to stop it.`


## <a href="#" id="open-close"></a>3.5 Map Management and Updates

In the map management control panel，we provide map management functions which include map deletion, update and save as.

![nav-24](/images/nav-24.png)

### 3.5.1 Update map

In actual use, the environment may change a lot, which results in the map established previously can no longer be tracked. In this moment, you can use the function of updating map. First select the map to be updated in the left menu , then click the button “Update Map”.

![nav-25](/images/nav-25.png)

![nav-26](/images/nav-26.png)

The robot may not be able to trace after turning on the updating function. At this time, you can remotely control the robot to a place where environment changes a little , then the robot can track the environment. The subsequent operation is the same as the process of establishing a map. When the map updating is completed, please click the button“Save As “firstly. Then you need to enter the name of the new map and wait for the save to complete. If you feel that the new map is of good quality, you can click the button “End Update” to end the map update process. The newly updated map can be seen in the map drop-down menu. After that, you can use the new map to navigate.

![nav-27](/images/nav-27.png)


### 3.5.2 Delete map

Select the name of map in the first drop-down menu. Click the button “delete “  on the right to delete the map.

[Robot map management](https://www.bwbot.org/s/TPuSCo)
