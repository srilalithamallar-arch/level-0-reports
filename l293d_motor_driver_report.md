# L293D Motor Driver -- Essential Overview

## 1. Introduction

The **L293D** is a widely used integrated circuit (IC) designed for
driving inductive loads such as DC motors, stepper motors, relays, and
solenoids. It acts as an interface between low‑power control electronics
(like microcontrollers) and high‑power devices such as motors.

Microcontrollers typically cannot supply enough current to drive motors
directly. The L293D solves this problem by providing a higher current
output stage controlled by low‑power logic signals.

------------------------------------------------------------------------

## 2. Key Features

-   **Dual H‑Bridge motor driver**
-   Can control **2 DC motors** independently
-   **Operating voltage (logic):** 4.5 V -- 7 V
-   **Motor supply voltage:** Up to 36 V
-   **Output current:** 600 mA per channel
-   **Peak output current:** 1.2 A (non‑continuous)
-   **Built‑in flyback diodes** for inductive protection
-   Compatible with **TTL and CMOS logic**
-   Available in **16‑pin DIP package**

------------------------------------------------------------------------

## 3. What is an H‑Bridge?

An **H‑bridge** is an electronic circuit that allows current to flow
through a motor in either direction. This enables a motor to rotate
**clockwise or counterclockwise**.

The L293D contains **two H‑bridges**, allowing control of: - Two DC
motors - One stepper motor

By switching the input logic signals, the direction of the motor can be
reversed.

------------------------------------------------------------------------

## 4. Pin Configuration

The L293D has **16 pins**. The most important ones are:

  Pin     Name       Function
  ------- ---------- ------------------------
  1       Enable 1   Enables motor driver 1
  2       Input 1    Logic input
  3       Output 1   Motor terminal
  4,5     GND        Ground
  6       Output 2   Motor terminal
  7       Input 2    Logic input
  8       Vcc2       Motor power supply
  9       Enable 2   Enables second driver
  10      Input 3    Logic input
  11      Output 3   Motor terminal
  12,13   GND        Ground
  14      Output 4   Motor terminal
  15      Input 4    Logic input
  16      Vcc1       Logic power supply

------------------------------------------------------------------------

## 5. Working Principle

The L293D works by receiving **low‑current digital signals** from a
microcontroller and using them to control **higher‑current outputs**
that power motors.

Typical operation:

1.  Microcontroller sends logic signals to input pins.
2.  L293D interprets these signals.
3.  Internal H‑bridge switches determine the direction of current.
4.  Current flows through the motor accordingly.

------------------------------------------------------------------------

## 6. Motor Direction Control

For one motor:

  Input 1   Input 2   Motor Action
  --------- --------- ---------------------------
  0         0         Stop
  1         0         Rotate one direction
  0         1         Rotate opposite direction
  1         1         Stop (brake)

The **Enable pin must be HIGH** for the motor to operate.

------------------------------------------------------------------------

## 7. Applications

The L293D is commonly used in:

-   Robotics
-   Line follower robots
-   Remote controlled vehicles
-   Conveyor systems
-   Automated machinery
-   Stepper motor control systems

Because of its simplicity and reliability, it is widely used in
**Arduino and embedded system projects**.

------------------------------------------------------------------------

## 8. Advantages

-   Easy interface with microcontrollers
-   Built‑in protection diodes
-   Can control motor direction
-   Simple circuit design
-   Low cost and widely available

------------------------------------------------------------------------

## 9. Limitations

-   Limited current capability (600 mA)
-   Inefficient compared to modern MOSFET drivers
-   Generates heat under heavy loads
-   Not suitable for high‑power motors

For higher efficiency applications, modern drivers such as MOSFET‑based
drivers are preferred.

------------------------------------------------------------------------

## 10. Basic Connection with a Microcontroller

Typical setup:

-   **Vcc1** → Microcontroller 5 V
-   **Vcc2** → Motor supply (6--12 V typical)
-   **GND** → Common ground
-   **Input pins** → Microcontroller digital pins
-   **Enable pin** → PWM pin (for speed control)

Motor speed can be controlled using **PWM signals** applied to the
enable pin.

------------------------------------------------------------------------

## 11. Conclusion

The L293D motor driver is a simple and effective IC used to control DC
and stepper motors from low‑power digital systems. While it is somewhat
outdated compared to modern motor drivers, it remains a popular
component in education, robotics, and embedded system prototyping due to
its simplicity, availability, and ease of use.
