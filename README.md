<img width="575" height="313" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/14abc35a-e9d6-4387-bdc1-c4ed730e52a6" /># FULL_ADDER_SUBTRACTOR

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
<img width="360" height="406" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/263e9264-65bb-40db-a5b9-1422b111ec19" />
<img width="546" height="428" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/1455a183-2990-4358-a238-b2c82c2db4d9" />



**Procedure**

Write the detailed procedure here

**Program:**
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic** 
<img width="787" height="475" alt="Screenshot 2025-10-07 194540" src="https://github.com/user-attachments/assets/9b59e74e-d04f-4c80-82df-a9dc14e7ff80" />

<img width="575" height="313" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/8f67f32d-1f05-4d3b-8e47-d2bda023b3ba" />


**Output Timing Waveform**
<img width="1920" height="399" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/d171b2ea-2205-4592-b4d5-563bd98c57d7" />


<img width="1119" height="219" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/47911f6d-d29c-4161-b6ee-1d0073422b2d" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



