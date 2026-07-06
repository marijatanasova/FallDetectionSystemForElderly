# Fall Detection System For Elderly

## Overview
A fall detection system for elderly people implemented in C, on STM32F103RB microcontroller using the MPU6050 accelerometer sensor. The system monitors acceleration data in real time and triggers a buzzer alert when a fall is detected.

## Hardware
- STM32F103RB microcontroller
- MPU6050 accelerometer (I2C)
- Active buzzer (alert output)

## How it works
The MPU6050 continuously measures acceleration on X, Y, Z axes. Total acceleration is calculated as √(x² + y² + z²). A fall is detected when a sudden acceleration spike occurs followed by a period of stillness, indicating the person has fallen and is no longer moving.

## Implementation
- I2C communication at register level, without HAL libraries
- MPU6050 register reading via I2C1 on STM32
- Fall detection algorithm based on total acceleration thresholds

## Status

Implemented:
- I2C peripheral initialization (register level, no HAL)
- I2C read function implemented

In progress:
- Accelerometer data reading and conversion
- Fall detection algorithm
- Buzzer alert
