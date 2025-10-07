# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Full Adder**

![zz](https://github.com/user-attachments/assets/8e413a7b-cc32-4b8b-9fc2-4dadfb58f17e)

**Full Subtractor**

![z](https://github.com/user-attachments/assets/33900d33-9b87-47ad-86f7-3c47fc547a43)

**Procedure**

Write the detailed procedure here

**Program:**

**FULL ADDER:**

module exp4(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule 

**FULL SUBTRACTOR:**

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

**FULL ADDER:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 183148" src="https://github.com/user-attachments/assets/3625b807-ce23-416d-bb79-d1a5b147553d" />

**FULL SUBTRACTOR:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 184813" src="https://github.com/user-attachments/assets/9e250c73-87ad-4421-9bf4-8910e0fd5315" />

**Output Timing Waveform**

**FULL ADDER:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 183706" src="https://github.com/user-attachments/assets/421227e6-fdaa-4084-91af-ce70fbecd254" />

**FULL SUBTRACTOR:**

<img width="1919" height="1079" alt="Screenshot 2025-10-07 185223" src="https://github.com/user-attachments/assets/823937a7-e054-46a1-b464-30f2a83dfe6c" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

