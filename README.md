# verilog-prolog-circuitry

In the Computer System Fundamentals course, material covered digital logic circuits and how they work together to form the digital and electronic devices that surround us. Specifically, we covered number systems, basic logic gates, Boolean algebra, combinational logic circuits, sequential logic circuits, finite state machines (FSM), and simple processor datapaths.

# Final Project
Run using Logisim.
Downloadable through https://sourceforge.net/projects/circuit/

## Project Modules
### Main
![Screenshot (19)](https://github.com/user-attachments/assets/7bed1dd3-e6bf-4cf6-bb14-36c814f39f0c)
It includes:
a) Two 7-segments to display the
i. First operand (8-bit) before pressing the operator
ii. Result after writing second operand ( 9-bit) and pressing the equal
button.
b) 8-block calculator
c) 4 buttons : ‘+’ , ‘-‘, ‘*’, ‘/’
d) ‘=’ button
e) 8 input ports for the data

### 8-bit Calculator
![Screenshot (20)](https://github.com/user-attachments/assets/506b911b-f463-47ae-9aa0-4e693f162050)
2- 8-bit Calculator
It includes:
a) Controller sub-circuit
b) Datapath sub-circuit
c) 4-bit Operator input port
d) 8 –bit Data input port
e) Two 4-bit display output ports.

### Controller ( FP Part 1)
![Screenshot (21)](https://github.com/user-attachments/assets/0944fcc6-d55d-4df5-bb55-41761aa2785d)
It is a finite state machine stores ‘1’ when press equal and clears the stored
value when any operator is pressed.
![Screenshot (22)](https://github.com/user-attachments/assets/2df48881-f022-4b2e-a17f-2cc47ad8b273)

### Datapath ( FP Part 2)
![Screenshot (23)](https://github.com/user-attachments/assets/abe93959-39b4-4028-9e7e-969277af3d0e)
4- Datapath ( FP Part 2)
It includes:
a) Three register to store the ALUA,ALUB,Operator:
i. ALUA register (8-bit) enabled when operator is pressed only
ii. ALUB register (8-bit) enabled when equal is pressed only.
iii. Operator register (4-bit) enabled when operator is pressed only.
b) ALU_CIR which is ALUCIR sub-circuit for ALU capable for the four
operations ‘+’, ‘-‘, ‘*’, and ‘/’.
c) 8-bit 2x1 MUX to choose which of the ALUA or ALUZ to be transferred
to the output display. (MUX selection is the state of the controller), if 0
then transfer ALUA, and if 1 then transfer ALUZ to the display output.
d) S 1-bit input port from the state of the controller sub-ciorcuit
e) Equal 1-bit input port from the user equal button
f) Operator 4-bit input port from the user operator.
g) Input data 8-bit port
h) Output data 8-bit port.
i) Enable for the ALUA and operator registers
![Screenshot (25)](https://github.com/user-attachments/assets/d019a02a-bcd4-4a02-9f30-d953553a2647)
j) Enable for the ALUB register
![Screenshot (24)](https://github.com/user-attachments/assets/d7956c5c-b4ac-4dc7-9864-e238d6efdece)

### ALUCIR
![Screenshot (26)](https://github.com/user-attachments/assets/45d54d7a-32ea-4c20-a669-12195d2a06d0)
It includes:
a) Four arithmetic units of 8-bit binary inputsfor addition, subtraction,
multiplication and division.
b) 8-bit 4x1 MUX to select certain output from any of the arithmetic unit
based on the selection, where the MUX selection is the output of the
encoder circuit of operator input.
c) Operator 4-bit input port from the user operator.
d) Input1 data 8-bit port
e) Input2 data 8-bit port
f) Output data 8-bit port.

### Encoder
![Screenshot (27)](https://github.com/user-attachments/assets/e9d047f8-b5a6-4a33-8328-6c8bc31b92bb)






## Simulation Results
![Screenshot (18)](https://github.com/user-attachments/assets/9dfced0c-520f-4ca4-a804-e7fcde4c21d2)
