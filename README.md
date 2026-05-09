# Autonomous Obstacle Avoidance System

## 🎯 Project Overview
[cite_start]This project demonstrates an automated obstacle avoidance system designed for autonomous navigation[cite: 76, 77]. [cite_start]It uses an ultrasonic sensor to monitor the path ahead and triggers an emergency stop via an H-Bridge motor driver if an object is detected within a specific safety threshold[cite: 77, 78].

## 🛠 Hardware Components
* [cite_start]**Microcontroller:** Arduino Uno R3[cite: 80].
* [cite_start]**Motor Driver:** L293D H-Bridge IC[cite: 81].
* [cite_start]**Sensor:** HC-SR04 Ultrasonic Distance Sensor[cite: 82].
* [cite_start]**Actuator:** Mini DC Motor[cite: 83].
* [cite_start]**Power Supply:** 9V Battery (Motor Power) and USB (Logic Power)[cite: 84].

## 🔌 Circuit Connections

### L293D Motor Driver Wiring
| Chip Pin | Connect To | Function |
| :--- | :--- | :--- |
| Pin 1 | Arduino D9 (PWM) | [cite_start]Speed Control (Enable) [cite: 86] |
| Pin 2 | Arduino D8 | [cite_start]Direction 1 [cite: 86] |
| Pin 3 | Motor Terminal 1 | [cite_start]Power to Motor [cite: 86] |
| Pin 4, 5 | Arduino GND | [cite_start]Ground [cite: 86] |
| Pin 6 | Motor Terminal 2 | [cite_start]Power to Motor [cite: 86] |
| Pin 7 | Arduino D7 | [cite_start]Direction 2 [cite: 86] |
| Pin 8 | 9V Battery (+) | [cite_start]Motor Power (VCC2) [cite: 86] |
| Pin 16 | Arduino 5V | [cite_start]Chip Logic (VCC1) [cite: 86] |
| Pin 12, 13 | Arduino GND | [cite_start]Ground [cite: 86] |

### HC-SR04 Ultrasonic Sensor Wiring
| Sensor Pin | Arduino Pin |
| :--- | :--- |
| VCC | [cite_start]5V [cite: 88] |
| Trig | [cite_start]D12 [cite: 88] |
| Echo | [cite_start]D11 [cite: 88] |
| GND | [cite_start]GND [cite: 88] |

## 🔬 Circuit Analysis
* [cite_start]**Motor Control:** The system utilizes Pulse Width Modulation (PWM) on Pin 9 to control rotational speed[cite: 90]. [cite_start]The L293D IC allows low-current Arduino pins to switch high-current motor loads and change direction[cite: 91, 92].
* [cite_start]**Sensing Logic:** The HC-SR04 uses SONAR principles, sending a 40kHz ultrasonic burst to calculate distance[cite: 93, 94]. 
* [cite_start]**Safety Threshold:** If an obstacle is detected within **20cm**, the system executes an emergency stop by cutting power to the motor[cite: 78, 119, 122].

## 🚀 How to Run
1. Wire the components according to the tables above.
2. [cite_start]Ensure the 9V battery is connected to Pin 8 of the L293D to provide sufficient torque for the motor[cite: 84, 86].
3. [cite_start]Upload the provided source code to your Arduino Uno[cite: 96].
4. [cite_start]The motor will run at approximately 80% speed until an object blocks its path[cite: 126, 119].
