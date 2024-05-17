# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure


### Step1:

Define the predefined path
Create a list or array to store the coordinates of the robot's predefined path.
Each coordinate should represent a point along the path that the robot needs to follow.

### Step2:

Initialize the robot's starting position
Set the robot's initial position to the first coordinate in the predefined path.

### Step3:

Move the robot along the path
Loop through each coordinate in the predefined path, starting from the second coordinate.
Calculate the distance and direction from the robot's current position to the next coordinate.
Use appropriate robot control commands to move the robot towards the next coordinate.
Repeat this process for each coordinate in the predefined path.

### Step4:

Check if the robot has reached the end of the path
After completing the loop, compare the robot's final position with the last coordinate in the
predefined path.
If the two positions match or are within a certain threshold, the robot has successfully reached
the end of the path.
If not, modify the path or make other adjustments as needed.

### Step5:
End the program

Once the robot has reached the end of the path, stop the program or execute any additional
tasks required.
Print a message or perform any necessary cleanup steps before terminating the program.
## Program
```python
from robomaster import robot
import time
from robomaster import camera

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0.5, y=0, z=80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")

    ep_chassis.move(x=1.0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=-118, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")
    
    ep_chassis.move(x=-1.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")
    

    ep_chassis.move(x=0, y=1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=84, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()


```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![image](https://github.com/tharunkumaran2006/mobilerobot-openloopcontrol/assets/151625188/f7a5e85c-0a67-48a5-9f7c-9b0693d79890)

![image](https://github.com/tharunkumaran2006/mobilerobot-openloopcontrol/assets/151625188/70ade4a2-c5be-4874-8650-9d8e5d5bbe18)

![robo](https://github.com/tharunkumaran2006/mobilerobot-openloopcontrol/assets/151625188/edeaee46-23b2-4fd2-b83d-55b5fe95f69c)

<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://youtu.be/DI4lqbV5aQU?si=p9tiFasFxMzKM2kh)

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
THARUN V K (212223230231)
Department of Artificial Intelligence and Machine Learning
Saveetha Engineering College
```
