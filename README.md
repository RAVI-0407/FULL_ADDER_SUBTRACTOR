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

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: RAVIPRASATH K

RegisterNumber: 212224230225 */

  **Full-Adder**
```
 module Fulladder(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule
```

  **Full-Subtractor**
  ```
 module Fullsubtractor(diff,borrow,a,b,c);
 input a,b,c;
 output diff,borrow;
 xor(diff,a,b,c);
 assign borrow= (~a)&c | (~a)&b | (b&c);
 endmodule
```

**RTL Schematic**

**Full-Adder** 

![image](https://github.com/user-attachments/assets/4f9cecae-173b-4c62-92a1-68f1cb59bae1)

**Full-Subtractor**

![image](https://github.com/user-attachments/assets/19b24c94-141f-4256-94ee-42819526245c)

**Output Timing Waveform**

**Full-Adder**

![image](https://github.com/user-attachments/assets/ee8230c8-f5d9-46c1-aa98-cd96daff77e9)

**Full-Subtractor**

![image](https://github.com/user-attachments/assets/b5bb1f96-d5f2-41bb-8e53-136b11d20393)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



