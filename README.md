# PD-Controller-for-Line-follower-Robot

We have 5 IR sensor, we planned to each sensor has its own error signal as following:

•	Edge Left Sensor (error=+2).

•	Left Sensor (error=+1).

•	Middle Sensor (error=0).

•	Right Sensor (error=-1).

•	Edge Right Sensor (error=-2).


   Control Signal=K_P×e[N]+K_D×(e[N]-e[N-1]) ……. (1)

Speed is the reference point where is 70 of 255 voltage level.

 Left Motor = Speed - Control Signal
 
 Right Motor = Speed + Control Signal.

Test the logic:
assume the robot sense the Left edge Sensor, the error= +2, and the previous error was 0:

 Control Signal=15×2+2×(2-0) =34
 
 Left Motor = 70 - 34=36
 
 Right Motor = 70 + 34=104
 
And that what we want to decrease the left motor, at the same time increase the right motor.


References:
[1] https://www.instructables.com/id/Line-Follower-Robot-PID-Control-Android-Setup/
[2] https://howtomechatronics.com/tutorials/arduino/arduino-dc-motor-control-tutorial-l298n-pwm-h-bridge/
[3] http://www.circuitbasics.com/arduino-ir-remote-receiver-tutorial/
[4] https://en.wikipedia.org/wiki/PID_controller


Demo of Project:
https://www.youtube.com/watch?v=hbJG722K6jE

