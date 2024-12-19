# verilog-prolog-circuitry

In the Computer System Fundamentals course, material covered digital logic circuits and how they work together to form the digital and electronic devices that surround us. Specifically, we covered number systems, basic logic gates, Boolean algebra, combinational logic circuits, sequential logic circuits, finite state machines (FSM), and simple processor datapaths.

# Final Project
Run using Logisim.
Downloadable through https://sourceforge.net/projects/circuit/

## Project Modules
### Main
![Screenshot (19)](https://github.com/user-attachments/assets/7bed1dd3-e6bf-4cf6-bb14-36c814f39f0c)
It includes:
1. Two 7-segments to display the
    1. First operand (8-bit) before pressing the operator
    2. Result after writing second operand ( 9-bit) and pressing the equal button.
2. 8-block calculator
3. 4 buttons : ‘+’ , ‘-‘, ‘*’, ‘/’
4. ‘=’ button
5. 8 input ports for the data

### 8-bit Calculator
![Screenshot (20)](https://github.com/user-attachments/assets/506b911b-f463-47ae-9aa0-4e693f162050)
It includes:
1. Controller sub-circuit
2. Datapath sub-circuit
3. 4-bit Operator input port
4. 8 –bit Data input port
5. Two 4-bit display output ports.

### Controller ( FP Part 1)
![Screenshot (21)](https://github.com/user-attachments/assets/0944fcc6-d55d-4df5-bb55-41761aa2785d)
It is a finite state machine stores ‘1’ when press equal and clears the stored
value when any operator is pressed.
![Screenshot (22)](https://github.com/user-attachments/assets/2df48881-f022-4b2e-a17f-2cc47ad8b273)

### Datapath ( FP Part 2)
![Screenshot (23)](https://github.com/user-attachments/assets/abe93959-39b4-4028-9e7e-969277af3d0e)
It includes:
1. Three register to store the ALUA,ALUB,Operator:
    1. ALUA register (8-bit) enabled when operator is pressed only
    2. ALUB register (8-bit) enabled when equal is pressed only.
    3. Operator register (4-bit) enabled when operator is pressed only.
2. ALU_CIR which is ALUCIR sub-circuit for ALU capable for the four operations ‘+’, ‘-‘, ‘*’, and ‘/’.
3. 8-bit 2x1 MUX to choose which of the ALUA or ALUZ to be transferred to the output display. (MUX selection is the state of the controller), if 0 then transfer ALUA, and if 1 then transfer ALUZ to the display output.
4. S 1-bit input port from the state of the controller sub-ciorcuit
5. Equal 1-bit input port from the user equal button
6. Operator 4-bit input port from the user operator.
7. Input data 8-bit port
8. Output data 8-bit port.
9. Enable for the ALUA and operator registers
![Screenshot (25)](https://github.com/user-attachments/assets/d019a02a-bcd4-4a02-9f30-d953553a2647)
10. Enable for the ALUB register
![Screenshot (24)](https://github.com/user-attachments/assets/d7956c5c-b4ac-4dc7-9864-e238d6efdece)

### ALUCIR
![Screenshot (26)](https://github.com/user-attachments/assets/45d54d7a-32ea-4c20-a669-12195d2a06d0)
It includes:
1. Four arithmetic units of 8-bit binary inputsfor addition, subtraction, multiplication and division.
2. 8-bit 4x1 MUX to select certain output from any of the arithmetic unit based on the selection, where the MUX selection is the output of the encoder circuit of operator input.
3. Operator 4-bit input port from the user operator.
4. Input1 data 8-bit port
5. Input2 data 8-bit port
6. Output data 8-bit port.

### Encoder
![Screenshot (27)](https://github.com/user-attachments/assets/e9d047f8-b5a6-4a33-8328-6c8bc31b92bb)






## Simulation Results
![Screenshot (18)](https://github.com/user-attachments/assets/9dfced0c-520f-4ca4-a804-e7fcde4c21d2)
