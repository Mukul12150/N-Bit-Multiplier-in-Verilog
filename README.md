# N-Bit-Multiplier-in-Verilog

### Overview
This project implements an N-bit multiplier using Verilog. The design can multiply two N-bit unsigned numbers to produce a 2N-bit result. This README provides an overview of the project structure, design details, and instructions for simulation and synthesis.

### Features
Parameterizable Bit Width: The design allows for easy adjustment of the bit width (N) of the multiplier.
Modular Design: The multiplier is implemented using a hierarchical and modular approach for better readability and maintenance.
Testbench Included: A testbench is provided to simulate and verify the functionality of the multiplier.

### Project Structure
``*N-bit-Multiplier/*                                                                                                                  
├── src/                                                                                                                          
│   ├── verilog code.v      # Top-level module for the N-bit multiplier                                                                  
│   └── partial_product.v # Module for partial product generation                                                                 
├── tb/                                                                       
│   └── Testbench.v   # Testbench for the N-bit multiplier                                                                                          
├── README.md             # Project documentation                                                 
└── Makefile              # Makefile for running simulations and synthesis ``                                                                 



### Design Details
**Multiplier Module (multiplier.v)**
The top-level module multiplier.v implements the N-bit multiplier. The module takes two N-bit inputs and produces a 2N-bit output.

**Ports**
input [N-1:0] a - First N-bit input operand
input [N-1:0] b - Second N-bit input operand
output [2*N-1:0] product - 2N-bit product of the multiplication
Partial Product Module (partial_product.v)
The partial_product.v module is used to generate partial products, which are then summed to produce the final product.

**Ports**
input [N-1:0] a - Input operand
input b - Single bit of the second operand
output [2*N-1:0] partial_product - Partial product generated
*Testbench*
The testbench tb_multiplier.v is used to verify the functionality of the N-bit multiplier. It applies various test vectors to the multiplier module and checks the correctness of the output.

### Simulation and Synthesis
Prerequisites
Verilog simulator (e.g., ModelSim, Icarus Verilog)
Synthesis tool (e.g., Xilinx Vivado, Synopsys Design Compiler)
Running Simulation
To run the simulation, navigate to the project directory and execute the following command:


This will compile the Verilog files and run the testbench, displaying the simulation results.


