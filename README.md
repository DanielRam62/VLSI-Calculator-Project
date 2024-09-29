# VLSI Calculator Project

This project involves the design and simulation of a VLSI-based calculator that performs addition and subtraction of 4-bit numbers using SRAM memory. The project was designed using **Cadence** tools and includes detailed simulations for all components, such as the SRAM cells, decoders, adders, and subtractors.

## Project Overview

The VLSI Calculator is capable of adding or subtracting two 4-bit numbers. The input numbers are stored in SRAM cells, and the results of the operations are also stored back in the SRAM. The project consists of several key components:

### Key Components:
1. **SRAM Memory Cell**: A static random-access memory cell designed to store bits of data without needing continuous refresh. The SRAM cells are used to store input numbers and the results of operations.
2. **Decoder**: A 4-to-16 decoder that selects the correct memory row for read and write operations.
3. **Full Adder and Subtractor**: Logic circuits that perform the arithmetic operations.
4. **Multiplexer (MUX)**: Used to select between user input and the calculator’s output for storage in the memory.
5. **D-Flip-Flop**: Stores the values needed for computation to ensure the correct sequence of read and write operations to the memory.

### Project Structure:

- **SRAM Memory**: The SRAM memory consists of 64 memory cells arranged in a 16-row by 4-column matrix. Each row represents a 4-bit number, and the decoder selects which row to read or write based on the user's input.
- **Full Adder and Subtractor**: These logic components perform addition and subtraction of two 4-bit numbers. The results are passed through the MUX and stored in the memory.

### Block Diagram

Below is a high-level block diagram of the system:

+------------------+ +--------------------+ | User Input | ---> | Decoder (4x16) | +------------------+ +--------------------+ | v +-----------------+ +------------------+ | SRAM (16x4) | <----> | Full Adder/Subtr. | +-----------------+ +------------------+ | v +--------------------+ | Output to SRAM | +--------------------+


### Workflow:

1. **User Input**: The user enters two 4-bit numbers for the calculator to process.
2. **Memory Access**: The system accesses the correct memory location to retrieve the input numbers and store the result.
3. **Addition/Subtraction**: The system either adds or subtracts the numbers using a full adder/subtractor circuit.
4. **Result Storage**: The result is sent back to the SRAM memory for storage.

## Key Components Details

### 1. SRAM Memory Cell
The SRAM cells are designed using 6 transistors each. These cells store a single bit of data and can be accessed for both reading and writing operations. The cells are fast but require a constant power supply to maintain the data.

### 2. Decoder
The decoder is a 4-to-16 line decoder that selects one of the 16 rows in the memory matrix for reading or writing. It ensures that only one row is activated at a time for data access.

### 3. Full Adder and Subtractor
The full adder performs binary addition on two 4-bit numbers, while the subtractor uses the two’s complement method to handle binary subtraction. The design ensures that the operations are completed quickly and accurately.

### 4. Multiplexer (MUX)
The 2-to-1 MUX selects between two possible inputs: one from the user and one from the output of the arithmetic unit. The selected value is then sent to the memory for storage.

### 5. D-Flip-Flop
The D-Flip-Flop is used to store intermediate values during calculations. It helps ensure the stability of the system by holding data during transitions between states.

## Simulation Results

All components were designed and simulated using **Cadence** tools. The simulations confirm that the system functions correctly and meets the design specifications.

### Highlights of the Simulation:
- **SRAM Cell**: The SRAM cells were successfully simulated, showing correct read and write operations.
- **Adder/Subtractor**: The arithmetic operations performed as expected, with no errors in addition or subtraction.
- **Full System**: The complete system was simulated, including memory access and result storage, and all operations were performed accurately.

## Files

- `docs/VLSI_Calculator_Project_Summary.pdf`: A comprehensive summary of the project, including design details, block diagrams, and simulation results.

## Conclusion

This project demonstrates the successful design and implementation of a VLSI calculator using SRAM memory. The system is capable of performing addition and subtraction on 4-bit numbers and storing the results in memory. The project showcases a thorough understanding of digital design principles and the use of VLSI techniques to create efficient, scalable circuits.

---

© 2024 Daniel Ram. Licensed under the MIT License.
