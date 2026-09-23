# Ultrasonic Distance Tracker with Servo Motor

## Description
This project automatically detects the distance of an object using an ultrasonic sensor and reacts by moving a servo motor. It is built using an Arduino Uno microcontroller and is ideal for projects like automated gates, smart dustbins, or simple radar tracking systems.

## Problem Statement
Measuring the exact proximity of approaching objects manually or with physical contact switches can be inefficient or impractical. This setup solves that problem by creating a touchless, automated system that continuously measures distance and triggers mechanical movement based on how close an object gets.

## Components Required
* **Arduino Uno Rev3** (Microcontroller board)
* **HC-SR04 Ultrasonic Distance Sensor** (Measures proximity)
* **SG90 Micro Servo Motor** (Handles physical movement)
* **Solderless Breadboard** (For connecting the parts together)
* **Jumper Wires** (Male-to-Male and Male-to-Female connection lines)

## Principle
The project works on the principle of **Sonar (Sound Navigation and Ranging)**. The ultrasonic sensor sends out high-frequency sound waves that bounce off nearby objects. By calculating the time it takes for the echo to return, the Arduino determines the exact distance of the target object.

## Working
1. **Triggering:** The Arduino instructs the ultrasonic sensor to emit a sound wave burst.
2. **Listening:** The sensor waits for the wave to hit an object and bounce back, measuring the travel time.
3. **Calculating:** The Arduino converts this travel time into centimeters using the speed of sound.
4. **Acting:** If the calculated distance falls within a specific range (for example, closer than 20cm), the Arduino signals the servo motor to rotate to a new angle (like opening a door). If nothing is close, the motor returns to its default position.

## Project Image
Below is the physical circuit assembly of the system:

![Arduino Distance Sensor Project](image_7_5YN5.png)

## Notes for Improvement
* **Power Supply:** Use an external power source for the servo motor instead of pulling power directly from the Arduino board to prevent sudden system resets.
* **Component Upgrade:** Swap the SG90 micro servo for a high-torque metal gear servo (like the MG996R) if you need to lift or push heavier physical mechanisms.
* **Alert Mechanism:** Add a small buzzer or a status LED to give immediate visual or audio feedback whenever an object enters the detection zone.

