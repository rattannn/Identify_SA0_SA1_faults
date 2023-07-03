GOOGLE INDIA GIRL HACKATHON 2023

# Identify_SA0_SA1_faults
Identify SA0 and SA1 fault in the given circuit as the input

Problem Statement:
As discussed in workshops, manufactured chips may have structural faults at certain places/nodes, which must be tested before being delivered to end users.
The task is to design an algorithm and write its code to identify the input vector required to identify the fault at a given node in a given circuit.
In a case, there would only be a single fault in the design.
The algorithm should be efficient, robust and able to identify faults quickly.

Inputs
Available inputs are -
Circuit file (format provided below)
Fault node location
Fault type
SA0 : stuck-at-0, a fault where node is not able to attain value 1, irrespective of inputs
SA1 : stuck-at-1, a fault where node is not able to attain value 0, irrespective of inputs
Outputs
The code should print a vector for inputs to test the fault, and the expected value of output to confirm the fault.
The output should be printed to the following file in run directory - output.txt

Circuit Format
The circuit will have 4 inputs - A, B, C and D. All of which are boolean type (only 0 and 1 are valid inputs)
The circuit’s output will always be Z which is also a boolean.
The circuit will be built using the following operations -
AND ( & ) gate
OR ( | ) gate
NOT ( ~ ) gate
XOR ( ^ ) gate
The circuit would purely be a combinational logic.
All internal nodes in the circuit would be named as : “net_<alphanumeric string>”
Each input ( A / B / C / D ) would be utilized only once in the circuit.
Example Input:
Circuit File:
net_e = A & B
net_f = C | D
net_g = ~ net_f
Z = net_g ^ net_e





Fault: 
FAULT_AT = net_f
FAULT_TYPE = SA0


Example Output:
[A, B, C, D] = [0, 0, 0, 1], Z = 1
