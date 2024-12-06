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

![Screenshot 2024-12-06 200623](https://github.com/user-attachments/assets/e5b3b053-a177-449d-a9e3-7a7a613f0ec2)

![Screenshot 2024-12-06 200630](https://github.com/user-attachments/assets/cc7fbfee-ed4f-4248-8e73-a7d48427f5c7)


**Procedure**

Write the detailed procedure here

**Program:**
```
module fulladder(a, b, cin, sum, carry);
input a, b, cin;
output sum, carry;
assign sum = ( (a ^ b) ^ cin );
assign carry = ( (a & b) | ( cin & (a ^ b) ) );
endmodule


module fullsub(a,b,bin,difference,borrow);
input a,b,bin; output difference,borrow;
assign difference = (a ^ b)^bin;
assign borrow= ( a & b) | ( bin & ((a ^ b )));
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

![Screenshot 2024-12-06 200900](https://github.com/user-attachments/assets/3b2b8a4a-5c3d-4cde-ad37-e0cf5418f774)
![Screenshot 2024-12-06 200928](https://github.com/user-attachments/assets/91ec7cbb-14ff-4242-8b95-77d81d595425)



**Output Timing Waveform**

![Screenshot 2024-12-06 201054](https://github.com/user-attachments/assets/20f89cf5-b306-4cb1-926d-3b6e2a6f5b2e)
![Screenshot 2024-12-06 201110](https://github.com/user-attachments/assets/729c0650-cdbe-4789-ba20-aeea2a2f17aa)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



