# Summary

This module uses a 3d printed spiral torsion spring (SPS) connected to the shaft of the motor. The angle is measured in this point and in the output of the spring, so torsion, and thus, torque can be calculated. The compliancy, thickness and revolutions of the spiral can be tuned for the application. The compliancy added to the system can be useful for manipulators and legged robots. The torsion sensing can help to prevent damage to the module. All of this should cost less than 15 USD.

<img src="/imgs/SEA.png" width="350">

<img src="/imgs/SEA.png" width="350">

The JGA25-370 is a very common format of DC motor with a 4 mm shaft, there is a vast set of gearbox ratios and nominal voltage, so you can choose an specific one to match your demands. You also need to modify the SPS "arm" to attach its body to something.

# Parts

The CAD files were made with Fusion 360, they can be found [HERE](https://grabcad.com/library/sea-module-1).

- Chasis
- Sensor holder
- SPS and arm
- SPS cover
- 2 Angle sensor CJCMU-03
- JGA25-370 motor (i used a 165 RPM at 6 V)
- 2 M3x8 sink bolts
- 2 M3x25 socket bolts
- 2x3 90° pin header male connector


# Fabrication

I printed all the parts in a standard FDM 3d printer (Ender3) using PLA. Notice that PLA may not be suitable for the application of your SPS. Also, notive that the pins are soldered in opposite directions in the sensors.

IMPORTANT: The angle sensor is made for a 4 mm shaft, BUT, I had to file it a little bit for the shaft to enter.

# Test setup and program

I used an Arduino Nano and a TB6612FNG dual motor driver. The test program uses the serial monitor to receive an angle input to rotate the shaft. I made two classes, one for the SEA and one for the servo (only one sensor). It requires three digital pins, one must provide PWM, and two analog input pins for the angle sensors. 

# Further work

- To characterize the SPS and use it to calculate torque.
- To make a simple robot.