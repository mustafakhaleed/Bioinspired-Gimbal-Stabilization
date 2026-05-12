# Bioinspired Stabilizing System: 3-Axis Gimbal Control

This repository hosts the research, design, and implementation of a bioinspired 3-axis gimbal stabilizing system. The project integrates mechanical design (CAD), mathematical modeling (Lagrangian dynamics), and real-time control systems.

## 🚀 Overview
The system uses three **FB5311M digital servo motors** and an **MPU6050 IMU** to maintain precise orientation despite external disturbances. 

### Key Features:
* **3-Axis Control:** Independent stabilization for Yaw, Pitch, and Roll.
* **Bioinspired Design:** Structural optimization for 3D printing and component integration.
* **Dual Control Strategy:** Comparative analysis between Linear Quadratic Regulator (LQR) and Proportional-Integral-Derivative (PID) controllers.

## 📐 Mathematical Foundation
The system dynamics are modeled using the **Euler-Lagrange** method. 

### Lagrangian Mechanics:
The Lagrangian $L$ is defined as the difference between Kinetic Energy ($K$) and Potential Energy ($P$):
$$L = K - P$$

### State-Space Model:
For small-angle approximations, the system is represented as:
$$\dot{X} = AX + BU$$
$$Y = CX + DU$$

## 🕹️ Control Implementation
A significant finding in this project was the transition from **LQR** to **PID**. 
* **LQR:** While theoretically optimal, it struggled with the specific noise and dynamics introduced by the physical placement of the IMU.
* **PID:** Provided a more robust solution. Each axis was fine-tuned ($K_p$, $K_i$, $K_d$) to eliminate steady-state error and minimize overshoot.

## 🛠️ Tools Used
* **Hardware:** Arduino Uno, MPU6050 IMU, FB5311M Servos.
* **Software:** LabVIEW (Simulation & Logic Visualization), Arduino IDE (C++), SolidWorks/CAD (Modeling).
