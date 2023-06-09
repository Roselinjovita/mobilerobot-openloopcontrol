# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Use from robomaster import robot.

Step2:

Choose the x,y,z - axis movement distance(meters).

Step3:

Give ep_chassis.move to move straight.

Step4:

Give time.sleep() for a break.

Step5:

Give ep_chassis.drive_speed to have a circular movement.

## Program

''
Developed by:  S.ROSELIN MARY JOVITA

Register number: 212222230122
''
```python
from robomaster import robot
import time
from robomaster import camera


if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera
          
    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed()
 
    ep_chassis.move(x=0, y=0, z=55, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=148,g=87,b=235,effect="on")  
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed() 

    
    x = speed in x direction( meter/second) [-3.5,3.5]
    y = speed in y direction( meter/second) [-3.5,3.5]
    z = rotation about z axis ( degree/second)[-300,300]
    
    ep_led.set_led(comp="all",r=137,g=235,b=147,effect="on")  
    ep_chassis.drive_speed(x=0.4,y=0,z=-20)
    time.sleep(12)
    ep_led.set_led(comp="all",r=255,g=49,b=49,effect="on") 
    ep_chassis.move(x=2.95, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=255,b=0,effect="on") 
    
    
    ep_chassis.move(x=0.2, y=0, z=90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=48,g=213,b=200,effect="on") 
    ep_chassis.move(x=0.5, y=0, z=0, xy_speed=1).wait_for_completed()

    ep_chassis.drive_speed(x=0.2,y=0,z=-20.5)
    time.sleep(4)
    
    ep_chassis.move(x=2.2, y=0, z=0, xy_speed=1).wait_for_completed()

    
    
    

    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    



    
    ep_robot.close()

```
## MobileRobot Movement Image:

![robo](./img/robomaster.png)





Insert image here

![mobile robots](https://github.com/Roselinjovita/mobilerobot-openloopcontrol/assets/119104296/3e1a7cc8-f708-42cc-bc9e-a6ccd0a27a7f)



![mobile robo](https://github.com/Roselinjovita/mobilerobot-openloopcontrol/assets/119104296/4c2b1bce-4b21-4da0-ab50-2e4266273db7)



## MobileRobot Movement Video:

https://youtu.be/05wOwljVUqI



## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.



```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
