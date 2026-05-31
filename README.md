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
| A | B | Cin | Sum (S) | Carry-out (Cout) |
| - | - | --- | ------- | ---------------- |
| 0 | 0 | 0   | 0       | 0                |
| 0 | 0 | 1   | 1       | 0                |
| 0 | 1 | 0   | 1       | 0                |
| 0 | 1 | 1   | 0       | 1                |
| 1 | 0 | 0   | 1       | 0                |
| 1 | 0 | 1   | 0       | 1                |
| 1 | 1 | 0   | 0       | 1                |
| 1 | 1 | 1   | 1       | 1                |


| A | B | Bin | Difference (D) | Borrow-out (Bout) |
| - | - | --- | -------------- | ----------------- |
| 0 | 0 | 0   | 0              | 0                 |
| 0 | 0 | 1   | 1              | 1                 |
| 0 | 1 | 0   | 1              | 1                 |
| 0 | 1 | 1   | 0              | 1                 |
| 1 | 0 | 0   | 1              | 0                 |
| 1 | 0 | 1   | 0              | 0                 |
| 1 | 1 | 0   | 0              | 0                 |
| 1 | 1 | 1   | 1              | 1                 |

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:PARAVEZHAA M
RegisterNumber:212225220070
*/

module ex3 (a,b,c, x, y, z, sum, dif, car, bor);

input a,b,c,x,y,z;

output sum,dif,car, bor;

assign sum = a^b^c;

assign car = a&b | a&c | b&c;

assign dif = x^y^z;

assign bor = ~x&z | ~x&y | y&z; 

endmodule


**RTL Schematic**

**Output Timing Waveform**
<img width="1210" height="687" alt="image" src="https://github.com/user-attachments/assets/bc52e88a-6584-470e-9ee9-839f9b7a1002" />

<img width="1223" height="747" alt="image" src="https://github.com/user-attachments/assets/73930b68-3ee8-4e5b-8e64-c20ed76683e2" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



