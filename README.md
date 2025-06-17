# CODTECH-TASK-1
8-bit Arithmetic Logic Unit (ALU) Project
Overview
This project implements an 8-bit Arithmetic Logic Unit (ALU) in Verilog. The ALU supports the following operations:

Addition (ADD)
Subtraction (SUB)
Bitwise AND
Bitwise OR
Bitwise NOT

The design includes flags for zero, carry, and overflow detection. A testbench is provided to verify functionality, and a simulation report summarizes the results.
Files Included

alu_design.v: Verilog module for the ALU.
alu_testbench.v: Testbench for simulating the ALU with various test cases.
alu_simulation.vcd: Waveform output file generated during simulation.
simulation_report.md: Markdown file detailing simulation results and test case outcomes.

Features

Inputs: Two 8-bit inputs (A and B) and a 3-bit opcode to select the operation.
Outputs: 8-bit result, zero flag, carry flag, and overflow flag.
Operations:
000: Addition (A + B)
001: Subtraction (A - B)
010: Bitwise AND (A & B)
011: Bitwise OR (A | B)
100: Bitwise NOT (~A)
Other opcodes: Default to zero output



Setup and Simulation
Prerequisites

Verilog simulator (e.g., ModelSim, Vivado Simulator, or Icarus Verilog)
Verilog compiler supporting VCD waveform output

Steps to Simulate

Clone or Download: Obtain the project files.
Compile the Verilog Files:
Compile alu_design.v and alu_testbench.v using your Verilog simulator.
Example command for Icarus Verilog:iverilog -o alu_sim alu_design.v alu_testbench.v




Run the Simulation:
Execute the compiled simulation to generate the VCD file.
Example command for Icarus Verilog:vvp alu_sim




View Waveforms:
Open alu_simulation.vcd in a waveform viewer (e.g., GTKWave) to inspect signals.


Review Results:
Check simulation_report.md for a detailed summary of test cases and outcomes.



Test Cases
The testbench (alu_testbench.v) includes the following test cases:

Addition: 10 + 20
Subtraction: 20 - 10
AND: 10101010 & 11001100
OR: 10101010 | 11001100
NOT: ~10101010
Addition with overflow: 127 + 127
Subtraction with zero result: 10 - 10
Invalid opcode: 101

Simulation Report
The simulation_report.md file confirms that all test cases pass, verifying correct operation of the ALU, including proper flag behavior for zero, carry, and overflow conditions.
Notes

The ALU handles invalid opcodes by outputting zero.
The overflow flag is set for signed arithmetic overflow in addition and subtraction.
The VCD file (alu_simulation.vcd) can be used to visualize signal transitions during simulation.

License
This project is provided as-is for educational purposes.
