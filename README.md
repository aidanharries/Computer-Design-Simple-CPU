# Computer Design: Simple CPU

**Final Project for ECE 649**

**Author:** Aidan Harries

## Introduction

This project aims to develop a simple CPU that supports a subset of RISC-V instructions. The CPU is a 32-bit architecture with 32 registers and an ALU with control signals. It supports the R-Type instructions "Add" and "Sub", the I-Type instruction "Addi", the Load instruction "LW", and the Store instruction "SW". Additionally, the design includes a display module that shows a "smile face" on an LED matrix.

## Hardware Design

### CPU Hardware Block Diagram

The CPU hardware design consists of several interconnected modules to perform necessary operations. Key components include:
- **Memory (IMEM and DMEM):** Separate instruction and data memory units.
- **Program Counter (PC):** Tracks the current instruction being executed.
- **Control Logic:** Decodes instructions and generates control signals.
- **Immediate Generator (ImmGen):** Generates immediate values for certain instructions.
- **ALU (Arithmetic and Logic Unit):** Performs arithmetic and logical operations.
- **Branch Comparator:** Compares values in registers to determine branch conditions.
- **I/O Module:** Interfaces with external devices like the LED matrix.
- **Register File:** Contains 32 registers for storing data and addresses.
- **LED Matrix:** Displays the "smile face" image.

## Software/Firmware Description

The CPU design includes assembly language programs to control and test the CPU. Key programs include:

### TestCases

A series of tests to verify the CPU's functionality:
- **Addi:** Initialize registers.
- **Add:** Perform addition.
- **Sub:** Perform subtraction.
- **Sw:** Store word.
- **Lw:** Load word.

### IMEM

A program to display a smiley face on the LED matrix:
- Uses load and store instructions to transfer pixel data from data memory to display memory.

## Testing

### Test the TestCases

1. Run Logisim Evolution.
2. Open `FinalProject.circ`.
3. Load `TestCases` into IMEM memory module.
4. Enable the clock.

### Test the Smiley Face

1. Run Logisim Evolution.
2. Open `FinalProject.circ`.
3. Load `IMEM` and `DMEM` into the corresponding memory modules.
4. Enable the clock.

## Conclusion

This project successfully developed a simple CPU that supports a subset of RISC-V instructions. Despite challenges, particularly with the control logic module, the hardware and software components were successfully implemented and tested. Future improvements could include optimizing the hardware design for performance and adding more instructions to the instruction set.
