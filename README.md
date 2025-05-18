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
FULL ADDER
![Screenshot 2025-05-02 185901](https://github.com/user-attachments/assets/e8df89d4-c05a-44a9-b137-2d2a76fee5e2)
 FULL SUBTRACTOR
![Screenshot 2025-05-02 185952](https://github.com/user-attachments/assets/a902c23c-6d3b-441c-865f-e5e1fda1d22a)



**Procedure**
Open Quartus Software Create a New Project Create a New Design File Compile the Program Generate RTL Schematic Create Nodes for Inputs/Outputs Generate Timing Diagram Simulate Different Input Combinations Save Your Work
**Program:**


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by:Duraiarasan M
RegisterNumber:212224230071

```
Full Adder: 

module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

Full Subtractor:

module fullsub(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule
```
**RTL Schematic**
FULL ADDER
![Screenshot 2025-05-02 185346](https://github.com/user-attachments/assets/eb4c6c8f-86af-42a1-bff9-37d8b4c2e83b)

FULL SUBTRACTOR
![Screenshot 2025-05-02 185424](https://github.com/user-attachments/assets/f184d858-4324-42d1-b4c4-575de4957e1c)



**Output Timing Waveform**
FULL ADDER
![Screenshot 2025-05-02 185555](https://github.com/user-attachments/assets/41da14ec-013e-4500-8c5b-c6626280166c)
FULL SUBTRACTOR
![Screenshot 2025-05-02 185626](https://github.com/user-attachments/assets/8d908443-a9e4-4884-b49b-4982401815fe)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



