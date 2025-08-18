# Embedded-C
# Difference Between Normal C and Embedded C

## 1. What is the difference between Normal C and Embedded C?

  ---------------------------------------------------------------------------------
  Aspect             Normal C                       Embedded C
  ------------------ ------------------------------ -------------------------------
  **Purpose**        General-purpose programming    Specially used for programming
                     for desktop/laptop             microcontrollers and embedded
                     applications.                  systems.

  **Execution        Runs on operating systems like Runs directly on hardware
  Environment**      Windows, Linux, macOS.         without an OS (bare-metal) or
                                                    with a small RTOS.

  **Compiler**       Compilers generate code for    Compilers generate code for
                     general-purpose CPUs (e.g.,    microcontroller architectures
                     GCC for x86/x64).              (e.g., Keil for ARM, MPLAB for
                                                    PIC).

  **Libraries**      Uses standard libraries like   Uses hardware-specific
                     stdio.h, stdlib.h for          libraries and headers to
                     input/output, file handling,   control peripherals (e.g.,
                     etc.                           GPIO, UART, ADC).

  **Input/Output**   Uses devices like keyboard,    I/O happens through
                     mouse, display, and files for  microcontroller ports, sensors,
                     I/O.                           actuators, and other hardware.

  **Memory           Large memory available;        Very limited RAM/ROM; memory
  Management**       dynamic memory allocation is   must be used efficiently, often
                     common.                        avoiding dynamic allocation.

  **Programming      More abstract and portable     Hardware-dependent; code is
  Style**            across devices.                tightly coupled with the
                                                    microcontroller's registers and
                                                    datasheet.

  **Examples**       Writing a text editor, web     Writing code for LED blinking,
                     application, or calculator     motor control, or sensor data
                     program.                       reading.
  ---------------------------------------------------------------------------------

------------------------------------------------------------------------
