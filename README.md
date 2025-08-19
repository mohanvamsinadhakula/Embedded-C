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
# 2. What are the Basic Elements of C Language

The C programming language is built upon several fundamental elements. These elements form the foundation for writing and understanding C programs.

1. **Character Set**  
   - The collection of valid characters (letters, digits, special symbols, and whitespace) used to construct C programs.

2. **Identifiers**  
   - Names assigned to variables, functions, arrays, or other user-defined elements.  
   - Must begin with a letter or underscore and can consist of letters, digits, and underscores.

3. **Keywords**  
   - Predefined, reserved words provided by the C compiler.  
   - Each keyword has a special meaning and cannot be used as identifiers (e.g., `int`, `while`, `return`).

4. **Data Types**  
   - Specify the type of data a variable can hold.  
   - Examples: `int`, `float`, `double`, `char`.

5. **Constants**  
   - Fixed values that do not change during program execution.  
   - Can be numeric constants (`10`, `3.14`) or character/string constants (`'A'`, `"Hello"`).

6. **Variables**  
   - Named memory locations used to store data that can be modified during program execution.  
   - Declared using data types (e.g., `int x; float salary;`).

7. **Expressions**  
   - Combinations of variables, constants, operators, and functions that evaluate to a single value.  
   - Example: `a + b * 5`.

8. **Statements**  
   - Instructions that tell the compiler to perform specific actions.  
   - Types include:
     - **Declaration statements** (`int x;`)
     - **Assignment statements** (`x = 10;`)
     - **Control statements** (`if`, `while`, `for`)
     - **Function calls**

-----
