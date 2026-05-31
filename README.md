# 8-Bit Computer from Scratch (NAND Logic)

![Project Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Architecture](https://img.shields.io/badge/Architecture-8--Bit-blue)

## Overview
This project is a fully functional 8-bit computer built entirely from the ground up using fundamental NAND gates in a digital logic sim (By Sebastian Lague). Inspired by Ben Eater's Playlist. It features a custom architecture with a centralized bus, control logic, and an ALU capable of basic arithmetic operations. 

The goal of this project is to understand the lowest levels of computing—bridging the gap between raw logic gates and a machine capable of executing programmed instructions.

## Architecture & Components
The current architecture is built around an 8-bit data bus and includes the following core components:

* **Registers (A & B):** 8-bit general-purpose registers used for temporary data storage and ALU operations.
* **Arithmetic Logic Unit (ALU):** Currently supports 8-bit Addition and Subtraction.
* **Random Access Memory (RAM):** 16-byte addressable memory for storing instructions and data.
* **Memory Address Register (MAR):** Stores the memory address currently being accessed in RAM.
* **Program Counter (PC):** Keeps track of the current instruction's memory address and increments automatically.
* **Instruction Register (IR):** Holds the current instruction being executed.
* **Instruction Decoder:** The "brain" of the CPU that decodes the opcode and sends the correct control signals to right components.
* **Output Register:** Latches data from the bus to display the final output register(to a 3-Digit 7 Segment Display).

## Instruction Set Architecture (ISA)
The CPU currently supports a minimal, custom instruction set. 

| Mnemonic | Opcode | Description | Operation |
| :--- | :--- | :--- | :--- |
| **LDA** | `0001`  | Load to A | Loads data from the specified RAM address into Register A. |
| **ADD** | `0010`  | Add | Adds the value in RAM to Register A and stores the result in Register A. |
| **SUB** | `0011`  | Subtract | Subtracts the value in RAM from Register A. |
| **OUT** | `1111`  | Output | Moves the contents of Register A to the Output Register. |


## Future Roadmap
This is an evolving project. Here are the planned upgrades and features I want to implement next:

### Hardware & Architecture Expansions
- [ ] **Expand Instruction Set:** Implement `JNZ` (Conditional Jump), `JMP` (Unconditional Jump), and other logical and bitwise operations.
- [ ] **Conditional Logic:** Add a flags register (Zero, Carry) to support conditional jumps (e.g., `JNC`, `JNZ`), allowing for loops.
- [ ] **Memory Upgrade:** Expand the RAM addressing space beyond 16 bytes.

### Software & Tooling
- [ ] **Custom Assembler:** Write an assembler script in Python to automatically compile human-readable assembly mnemonics into the binary machine code required by the simulator. 

## Screenshots & Media
**Watch the 7+3 Calculation:**

https://github.com/user-attachments/assets/c996f1ae-ae27-4580-ad70-1a622eedb653

**Architecture Overview:**
![Computer Architecture](https://github.com/user-attachments/assets/44c7d35e-8795-45d2-a9ec-9f7ee2aded24)
