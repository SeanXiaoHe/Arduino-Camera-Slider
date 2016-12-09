#Arduino Camera Slider
---
##Synopsis
The goal of this project is creating a camera slider controlled by a joystick. The slider basically built by combining the Arduino Uno, the EasyDriver Stepper Motor Driver and the Collision sensor switch module. This project is an good example of control the direction and speed of a stepper motor with Analog Joystick, Easy Driver and limit Switches.

---
##Repository Contents

* Code: *Code for this project*

* IMG: *Images including schematic, my build example and photos of parts*

* Previous Version: *This folder contains the code and schematic for the previous design which built without the Collision sensor switch modules*

* README.md: *Full information about this project*

---
##Schematic
![alt tag](https://github.com/SeanXiaoHe/CS207/blob/master/IMG/SCHEMATIC.png?raw=true)

              
---
##Connection

![alt tag](https://github.com/SeanXiaoHe/CS207/blob/master/IMG/design.jpg)


Here are the connections:

Pin 9 is connected to Steps pin on Easy Driver

Pin 8 is connected to Direction pin

Pin 10 is connected to MS1 pin

Pin 11 is connected to MS2 pin

Pin 12 is connected to SLEEP pin

Pin A0 connected to joystick X-axis

Pin 4 is connected to the joystick Key or switch pin
 
Pint 2 and 3 are connected to the OUT pin of the Limit Switches
 
The Ground and Voltage pins of the Easy Driver are connected to a 1 Amp 12V power supply.
We are also using a small breadboard to split the Ground and Voltage connections of the various devices

---

##User Manual for the Arduino Slider

The slider in this project has to be connected to an external 12V power supply. It also cannot use the external power port on the Arduino; the user has to plug in a different power port to the Easy Driver.

The user can use the joystick to control the rotation direction of the motor which is also the direction of the camera base in this case. The camera base would move to the left when the user moves the joystick to the left, vice versa.

The user can also change the speed by clicking the joystick. The speed of the motor starts from slow to fast by each clicking. The user can alter the speed of each level as well as adding more levels through the if *(!digitalRead(Joy_switch))* part of the code in the loop. By adding a case, the user can add one more level for the speed switch function. When we change the variable *step_speed*, we can modify the speed for each level, from 10 as the slowest to 1 as the fastest speed.

![alt tag](https://github.com/SeanXiaoHe/CS207/blob/master/IMG/Capture.PNG)

The collision switch limits the movement of the motor. When the user moves the joystick, if the collision switch on pin 2 is activated, the motor can only move in a counter-clockwise direction, which means the camera base can only move in the left direction. If the collision switch on pin 3 is activated, the camera base can only go in the right direction.


---

##Parts

* 12V Power Supply 1Amp
* Collision sensor switch module
* EasyDriver Stepper Motor Driver
* GT2 Aluminum Timing Pulley – 20 teeth
* GT2 Belt Clip 2pcs
* GT2 Idler Pulley
* GT2 Timing Belt
* Joystick module with Switch
* Jumper Wires male to female 20pcs
* Nema 17 Stepper Motor
* Small Alligator Clips Test Lead – 10pcs
* Arduino Uno

---

##Credit

"Control the direction and speed of a Stepper motor with Analog Joystick, Easy Driver and limit Switches" from

https://brainy-bits.com/tutorials/stepper-motor-with-joystick-and-limit-switches/

