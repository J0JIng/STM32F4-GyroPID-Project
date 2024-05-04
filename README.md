# GyroPID - IMU + PID
Sensor Interface and Design Using STM32F4 for SC2104

## Overview
This project involves implementing PID control on a STM32 microcontroller board along with an Inertial Measurement Unit (IMU) sensor. The goal is to achieve stabilization of a platform based on the IMU readings.

## Hardware Requirements
- STM32 development board (specifically designed for version D)
- Inertial Measurement Unit (IMU) MPU-6050
- Servo motors
- OLED display
- Push button for user input

## Software Requirements
- STM32CubeIDE for development
- Standard Peripheral Library (SPL) for STM32

## Setup and Configuration
1. Ensure all hardware components are connected to the STM32 development board as per the IOC.
2. Configure the STM32CubeIDE project with the appropriate pin mappings and peripherals as specified in the provided code.
3. Flash the compiled firmware onto the STM32 board.
4. Ensure proper initialization of the IMU sensor and servo motors.

## Functionality
- The main program initializes the IMU sensor, OLED display, and other peripherals.
- Upon startup, the program displays initialization messages on the OLED display and initializes the IMU sensor.
- The program then enters a loop where it continuously reads data from the IMU sensor, computes roll and pitch angles, and applies PID control to adjust servo motors.
- User input from a push button is used to start and stop the control loop.
- During operation, the program continuously updates the OLED display with relevant information such as sensor readings, target angles, and servo motor PWM values.
- Serial communication is used to transmit roll and pitch angles, as well as target angles, for monitoring purposes. Use 'SerialPlot' to view. 

## Control Algorithms
- The program implements PID control algorithms for both roll and pitch angles.
- PID parameters (proportional, integral, derivative gains) can be adjusted for fine-tuning the control loop.

## Notes
- Ensure proper calibration of the IMU sensor for accurate readings.
- Adjust PID parameters based on the specific requirements and characteristics of the platform being stabilized.
