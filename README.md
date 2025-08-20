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
### 3. What is a Character Set? Explain in Detail

A **character set** is a collection of characters, where each character is mapped to a unique integer code (called a **code point**).  
In C programming, characters are stored and processed internally as integers, most commonly using the **ASCII (American Standard Code for Information Interchange)** standard.  

This mapping enables the computer to:
- Represent textual data in memory.
- Process characters as numeric values.
- Store, transmit, and display text consistently across systems.

Every character is associated with a unique integer value called its **ASCII value**.

---

### Types of Character Sets in C

Character sets can be broadly divided into two categories:

#### 1. Printable Characters
These characters are visible on the output screen and include:

- **Alphabets**  
  - Uppercase: `A [65] – Z [90]`  
  - Lowercase: `a [97] – z [122]`

- **Numeric Digits**  
  - `0 [48] – 9 [57]`

- **Special Symbols**  
  Characters other than alphabets and digits fall under this category.  
  Examples:  ! @ # $ % ^ & * ( ) - _ + = [ ] { } | \ ; : ' " , . / < > ?

---

#### 2. Non-Printable Characters
These characters are not directly visible but control formatting, spacing, or cursor movement. They are primarily represented using **escape sequences**.

- **Backslash Characters / Escape Sequences**  
- Formed by `\` followed by an alphabet, digit, or symbol.  
- Treated as **a single character** (not two).  
- Frequently used inside functions like `printf()`.  
- Exception: `\0` is not used inside `printf()`; it is reserved for **string termination**.

---

### Common Escape Sequences in C

| Escape Sequence | ASCII Value (Decimal) | ASCII Name (from Table) | Purpose |
|-----------------|------------------------|--------------------------|---------|
| `\a` | 7  | BEL (Bell)            | Produces an alert (beep sound) |
| `\b` | 8  | BS (Backspace)        | Moves cursor one position back |
| `\f` | 12 | FF (Form Feed)        | Advances to next page (historically used in printers) |
| `\n` | 10 | LF (Line Feed)        | Moves cursor to the beginning of the next line |
| `\r` | 13 | CR (Carriage Return)  | Moves cursor to the beginning of the current line |
| `\t` | 9  | HT (Horizontal Tab)   | Inserts a horizontal tab space |
| `\v` | 11 | VT (Vertical Tab)     | Moves cursor down one vertical tab (rarely used today) |
| `\0` | 0  | NUL (Null Character)  | Terminates strings in C |
---

### Key Notes for Embedded Systems Engineers
- Escape sequences are crucial in **console I/O** and debugging outputs.  
- The **`\0` null character** is fundamental in handling C-strings, as it marks the **end of string buffers**.  
- While characters like `\v` and `\f` exist, they are rarely used in modern embedded systems.  
- Octal (`\ooo`) and Hex (`\xhh`) escape forms are particularly useful when dealing with **non-printable control characters** in protocols or hardware communication.  


