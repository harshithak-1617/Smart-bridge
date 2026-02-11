# Smart-bridge

Smart Bridge Using Arduino


Abstract

The objective of this project is to monitor flood conditions and automatically lift a bridge when a dangerous water level is detected. The system also provides an alert using a buzzer. A smart bridge is an intelligent structure that senses environmental conditions and reacts automatically to ensure safety. This project demonstrates a simple and cost effective prototype using Arduino servo motors and a soil moisture sensor.

Introduction

Floods cause severe loss of life and property especially in developing countries where advanced monitoring systems are limited. Bridges are an essential part of transportation infrastructure and their failure during floods can lead to catastrophic consequences such as loss of lives damage to public property and disruption of transport and commerce.

This project proposes a smart bridge system that automatically adjusts its height in response to rising water levels. The aim is to improve safety and reduce risks during flood situations by using automation and embedded systems.

Components Used

Arduino Uno with programming cable
Servo motors two units
Soil moisture sensor
Breadboard
Jumper wires
Foam sheet for bridge structure
Adhesive

Working Principle

The soil moisture sensor continuously monitors the presence of water near the bridge. When water is detected the Arduino processes the sensor signal and activates the servo motors. The servo motors lift the bridge automatically and an alert is generated to indicate a flood condition. When the water level decreases the bridge returns to its original position.

Procedure

Step one Construct the bridge using foam sheets and lightweight materials so that it can move vertically.
Step two Install the servo motors and connect them to the Arduino to control the bridge movement.
Step three Connect the soil moisture sensor to the Arduino and place it near the water source.
Step four Write and upload the Arduino program to control the servo motors based on sensor input.
Step five Test the system by simulating flood conditions using water and observe the bridge movement.

Circuit Overview

The soil moisture sensor is connected to the Arduino input pin.
The servo motors are connected to the Arduino output pins.
Power is supplied through the breadboard power rails.

Arduino Code

#include <Servo.h>

Servo tap_servo;
int sensor_pin = 4;
int tap_servo_pin = 5;
int val;

void setup()
{
pinMode(sensor_pin INPUT);
tap_servo.attach(tap_servo_pin);
}

void loop()
{
val = digitalRead(sensor_pin);

if (val == 0)
{
tap_servo.write(0);
}

if (val == 1)
{
tap_servo.write(90);
}
}

Results

Initially the bridge remains in its normal position when no water is detected.
When an increased water level is detected the bridge lifts automatically.
The bridge stays in the raised position until the water level returns to normal.
This ensures safer passage for vehicles and pedestrians during flood conditions.

Conclusion

The Smart Bridge project successfully demonstrates an automatic height adjusting bridge using Arduino servo motors and a soil moisture sensor. The system continuously monitors water levels and adjusts the bridge height to improve safety during floods. This project shows the practical application of embedded systems and automation in smart infrastructure and disaster management.
