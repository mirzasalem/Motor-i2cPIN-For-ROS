# PID Motor Position Control

Arduino-based PID motor position control using quadrature encoder feedback and L298N motor driver with I2C communication support.

---

## Description

This project implements closed-loop PID control for a DC motor using an incremental encoder.  
The motor position and speed are calculated in real time, and the PID controller adjusts PWM output to achieve the desired setpoint.  
The system works as an I2C slave device and can be controlled by an external master such as ESP32 or Raspberry Pi.

---

## Features

- PID-based motor position control  
- Quadrature encoder feedback  
- L298N motor driver support  
- I2C slave communication  
- Interrupt-based encoder reading  
- Bidirectional motor control  

---

## Hardware

- Arduino Uno / Nano / Mega  
- DC motor with encoder  
- L298N motor driver  
- External power supply  

---

## Pin Configuration

| Signal | Pin |
|------|-----|
| Encoder A | D2 |
| Encoder B | D8 |
| Motor IN1 | D9 |
| Motor IN2 | D10 |
| I2C SDA | A4 |
| I2C SCL | A5 |

---

## Libraries

- PID_v1  
- Wire  
- PinChangeInt  

---

## I2C Details

- Slave address: `0x08`  
- Receives: motor setpoint  
- Sends: wheel position (degrees)  

---

## Usage

1. Upload the code to Arduino  
2. Connect motor and encoder  
3. Send position setpoint via I2C  
4. Motor moves to desired position  

---

## Notes

- Do not power motor directly from Arduino  
- Tune PID gains according to your motor  
- Common ground is required  

---

## Author

Mirza Salem

This arduino code is for Jetson nano i2c pin supported which takes 3,5 and 27,28pins.
