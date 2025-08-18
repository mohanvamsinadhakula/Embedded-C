# Embedded-C
# Difference Between Normal C and Embedded C

## 1. What is the difference between Normal C and Embedded C?

| Aspect                | Normal C                                                                  | Embedded C                                                                    |
|-----------------------|---------------------------------------------------------------------------|----------------------------------------------------------------------------   |
| **Purpose**           | General-purpose programming for desktop/laptop applications.              | Specially used for programming microcontrollers and embedded systems.         |
| **Execution Environment** | Runs on operating systems like Windows, Linux, macOS.                 | Runs directly on hardware without an OS (bare-metal) or with a small RTOS.    |
| **Compiler**          | Compilers generate code for general-purpose CPUs (e.g., GCC for x86/x64). | Compilers generate code for microcontroller architectures (e.g., Keil for ARM, MPLAB for PIC). |
| **Libraries**         | Uses standard libraries like stdio.h, stdlib.h for input/output, file handling, etc. | Uses hardware-specific libraries and headers to control peripherals (e.g., GPIO, UART, ADC). |
| **Input/Output**      | Uses devices like keyboard, mouse, display, and files for I/O.            | I/O happens through microcontroller ports, sensors, actuators, and other hardware. |
| **Memory Management** | Large memory available; dynamic memory allocation is common.              | Very limited RAM/ROM; memory must be used efficiently, often avoiding dynamic allocation. |
| **Programming Style** | More abstract and portable across devices.                                | Hardware-dependent; code is tightly coupled with the microcontroller’s registers and datasheet. |
| **Examples**          | Writing a text editor, web application, or calculator program.            | Writing code for LED blinking, motor control, or sensor data reading. |

------------------------------------------------------------------------
