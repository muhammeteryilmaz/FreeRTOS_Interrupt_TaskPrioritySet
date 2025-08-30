# FreeRTOS_Interrupt_Task

## Description
This project demonstrates FreeRTOS task prioritization with multiple LEDs controlled by different tasks. Each task toggles a specific LED (PB0, PB7, PB14) at different frequencies (750ms, 500ms, 250ms). A button interrupt on PC13 suspends or resumes the lowest-priority task.

## FreeRTOS Features
- Task management (`xTaskCreate`)
- Interrupt management (`xTaskResumeFromISR`)
- Task suspension/resumption (`vTaskSuspend`, `vTaskResume`)

## Hardware
- **Microcontroller**: STM32F446ZET6
- **Button**: PC13 (connected to GND, no pull-up required)
- **LEDs**: Onboard LEDs on PB0, PB7, PB14 (with integrated resistors)

## Setup
1. Open the project in STM32CubeIDE.
2. Ensure FreeRTOS and HAL libraries are included.

## Outputs
- **LEDs**: PB0 (750ms), PB7 (500ms), PB14 (250ms) toggle at different rates; PB0 toggles only when button is pressed

## Test Results
- The button interrupt successfully suspended/resumed the lowest-priority task, and LEDs toggled as expected based on task priorities.
