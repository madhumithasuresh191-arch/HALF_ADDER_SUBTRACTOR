# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit
## Name: S Madhumitha
## Reg No: 212225040217

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
half adder module exp3 ( input wire a, b,
output wire sum,
output wire carry)
~~~
assign sum   = a ^ b;   
assign carry = a & b;   
endmodule

half subracter

module half_subtractor (
input  wire a, b,         // Inputs
output wire diff, borrow  // Outputs
~~~

~~~
// Logic equations
assign diff   = a ^ b;     // XOR for difference
assign borrow = ~a & b;    // Borrow when a < b
~~~

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: RegisterNumber:212225040217

**RTL Schematic**
half adder
<img width="510" height="252" alt="Screenshot 2026-05-21 113906" src="https://github.com/user-attachments/assets/6f22efc4-d113-45ec-b667-6aef21d83444" />
half subracter 
<img width="572" height="238" alt="Screenshot 2026-05-21 113916" src="https://github.com/user-attachments/assets/1663a9ce-2da4-4fea-a81a-4899ccbc977d" />

**Output/TIMING Waveform**
half adder
<img width="1274" height="551" alt="Screenshot 2026-05-21 113938" src="https://github.com/user-attachments/assets/52df6c32-b764-4265-ba43-d6c8ea2cdcdd" />
half subracter 
<img width="1270" height="614" alt="Screenshot 2026-05-21 114000" src="https://github.com/user-attachments/assets/8f230317-0de4-48fb-bf78-f7774875568e" />

**Result:**
This Program was excecuted successfully.
