# Hand Gesture-Controlled 5-DOF Robotic Arm

A **5-DOF robotic arm teleoperation system** that enables real-time control through hand gestures using **Computer Vision, Deep Learning, and Embedded Systems**. The system translates human hand gestures captured through a camera into robotic joint commands, enabling intuitive and contactless human–robot interaction.

## Project Overview

The system combines a vision-processing pipeline with an embedded robotic control system. Hand gestures are detected using **MediaPipe hand landmark tracking** and classified using a **TensorFlow Lite** model. The recognized gestures are converted into corresponding joint commands and transmitted to an **Arduino-based robotic arm controller** through UART communication.

The robotic arm incorporates multiple servo-driven joints and a stepper-motor-based base rotation mechanism, providing coordinated control across five degrees of freedom.

## Key Features

* Real-time **hand gesture recognition**
* Computer Vision-based hand landmark detection using **MediaPipe**
* Deep Learning-based gesture classification using **TensorFlow Lite**
* Real-time teleoperation of a **5-DOF robotic arm**
* Gesture-to-joint command mapping
* **Denavit-Hartenberg (DH) based kinematic modelling**
* Arduino-based embedded motor control
* UART-based communication between vision system and robotic controller
* Servo and stepper motor control
* Multi-frame gesture validation to reduce unintended commands
* Gravity compensation for improved arm stability
* Experimental evaluation of recognition accuracy, latency, and gripper reliability

## System Architecture

```text
Camera
   ↓
Hand Detection – MediaPipe
   ↓
Hand Landmark Extraction
   ↓
Gesture Classification – TensorFlow Lite
   ↓
Gesture-to-Joint Mapping
   ↓
UART Communication
   ↓
Arduino Controller
   ↓
Servo / Stepper Motor Control
   ↓
5-DOF Robotic Arm
```

## Hardware

* Arduino Uno
* NEMA17 Stepper Motor
* A4988 Stepper Driver
* MG996R Servo Motors
* PCA9685 Servo Driver
* 5-DOF Robotic Arm Mechanism
* Camera/Webcam
* External power supply

## Software & Technologies

**Programming & AI**

* Python
* Computer Vision
* MediaPipe
* TensorFlow Lite
* NumPy

**Robotics**

* Denavit-Hartenberg Modelling
* Forward & Inverse Kinematics
* Joint-Space Control
* Gravity Compensation

**Embedded Systems**

* Arduino
* UART Communication
* PWM Servo Control
* Stepper Motor Control

## Performance

The developed system achieved:

* **93.4% overall gesture-classification accuracy**
* **187 ms mean end-to-end response latency**
* **84% reduction in spurious commands** using multi-frame validation compared with single-frame classification
* Gravity compensation reduced shoulder drift from approximately **12°/s to below 0.5°/s**
* **100% gripper timeout reliability over 50 trials**

## Applications

The system demonstrates the potential of gesture-based robotic teleoperation for:

* Human–Robot Interaction
* Assistive Robotics
* Remote Manipulation
* Educational Robotics
* Contactless Robotic Control
* Vision-Based Robotic Systems

## Project Outcome

This project provided hands-on experience in integrating **Computer Vision, Deep Learning, Robotics, Embedded Systems, Kinematic Modelling, and real-time communication** into a complete robotic system. It demonstrates the development of a vision-to-actuation pipeline in which human gestures are processed into real-time commands for physical robotic motion.
