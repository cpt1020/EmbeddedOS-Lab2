# Analysis and Implementation of Embedded Operating Systems Lab 2

嵌入式作業系統分析與實作 Analysis and Implementation of Embedded Operating Systems [CSIE7618] @ NCKU 2022 Spring

## Development Environment

- Development Board
    - STM32F407G-DISC1
- Real-Time Operating System (RTOS)
    - [FreeRTOS v10.2.1](https://github.com/FreeRTOS/FreeRTOS/tree/V10.2.1)
- IDE
    - STM32CubeIDE

## Report

https://hackmd.io/@cpt/embeddedOS_lab2

## Requirement

- Create four tasks
    - `Red_LED_App`, `Green_LED_App`, `Delay_App`, `TaskMonitor_App`
- `TaskMonitor_App` will call `Taskmonitor()` periodicity
- `TaskMonitor()`
    - Traverse `ReadyTaskList`, `DelayedTaskList`, `OverflowDelayedTaskList`
    - Print TCB information by UART
        - Task Name, Priority(Base/actual), Stack Pointer, TopOfStack Pointer, Task State
