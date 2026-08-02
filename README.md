# STM32 FreeRTOS Counting Semaphore LED Control

 Project Overview ->

This project demonstrates LED control using Counting Semaphore with FreeRTOS on STM32 microcontroller.

The main objective of this project is to understand RTOS task synchronization and how multiple tasks can access shared resources using semaphore mechanisms.

 Features

* Implemented multiple FreeRTOS tasks
* Used semaphore for task synchronization
* Controlled STM32 onboard LEDs using GPIO
* UART used for task execution monitoring
* Real-time task scheduling using FreeRTOS kernel

 Hardware Used

* STM32F407 Discovery Board
* USB to UART (for debugging)

Software Tools->

* STM32CubeIDE
* STM32 HAL Library
* FreeRTOS
* C Programming

 Concepts Implemented->

* FreeRTOS Tasks
* Semaphore Acquire and Release
* Task Synchronization
* GPIO Programming
* UART Communication

 Working Principle->

Four different FreeRTOS tasks are created for controlling four LEDs.

Each task tries to acquire the semaphore before accessing the hardware resource. After completing the LED toggle operation, the task releases the semaphore, allowing another task to execute.

UART messages are transmitted to monitor which task acquired and released the semaphore.

 Task Details->

| Task   | LED Control | Function                  |
| ------ | ----------- | ------------------------- |
| Task 1 | Green LED   | LED Toggle with Semaphore |
| Task 2 | Orange LED  | LED Toggle with Semaphore |
| Task 3 | Red LED     | LED Toggle with Semaphore |
| Task 4 | Blue LED    | LED Toggle with Semaphore |

 Output

* LEDs toggle according to task execution.
* UART displays semaphore acquire and release messages.


