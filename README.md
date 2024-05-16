# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:
Use from robomaster import robot

### Step2:
Choose the x,y,z - axis movement distance(meters).

### Step3:
Give ep_chassis.move to move straight.

### Step4:
Give time.sleep() for a break.

### Step5:
Give ep_chassis.drive_speed to have a circular movement.

### Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=0, y=3.05, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=200,g=255,b=205,effect="on")
    ep_chassis.move(x=1.16, y=0, z=15, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")
    ep_chassis.move(x=0, y=0, z=75, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=153,b=102,effect="on")
    ep_chassis.move(x=1.25, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=204,b=255,effect="on")
    ep_chassis.move(x=0, y=0, z=-40, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x=1.68, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=192,g=192,b=192,effect="on")
    ep_chassis.move(x=0, y=0, z=43, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=135,g=151,b=0,effect="on")
    ep_chassis.move(x=1.3, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")
    ep_chassis.move(x=0, y=-2, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")
    ep_chassis.move(x=-0.2, y=.7, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
    ep_chassis.move(x=0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    ep_robot.close()



    
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

https://youtu.be/CdYk-LlmclM?si=rn785d0aA1lbLK3R

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

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
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
