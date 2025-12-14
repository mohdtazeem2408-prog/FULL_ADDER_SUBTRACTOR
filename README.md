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

Truthtable

<img width="694" height="460" alt="Screenshot 2025-12-14 084519" src="https://github.com/user-attachments/assets/3ef9171a-f004-49db-ac43-5af69abb41f9" />



<img width="807" height="621" alt="Screenshot 2025-12-14 084535" src="https://github.com/user-attachments/assets/c4f830b1-5f10-4fed-a0ec-c90952f6af47" />



Procedure
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.



Write the detailed procedure here

Program:

```
module full_adder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule

```
```
module full_subtractor(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
assign diff=(a^b^c);
assign borrow=(~a&c)|(~a&b)|(b&c);
endmodule

```


RTL Schematic

FULL ADDER

<img width="1037" height="572" alt="Screenshot 2025-12-14 084137" src="https://github.com/user-attachments/assets/60ff158f-e8a7-4a4a-a76e-0c3cab69b8d2" />

FULL SUBTRACTOR


<img width="1036" height="522" alt="Screenshot 2025-12-14 084206" src="https://github.com/user-attachments/assets/8fef7a92-a630-44d7-a2ff-34fd8b0710d0" />


Output Timing Waveform


FULL ADDER

<img width="1034" height="324" alt="Screenshot 2025-12-14 084227" src="https://github.com/user-attachments/assets/56a30a34-d3dc-4450-a050-0a9d10a76e85" />


FULL SUBTRACTOR

<img width="1035" height="295" alt="Screenshot 2025-12-14 084244" src="https://github.com/user-attachments/assets/94f6a389-5a57-4f21-aaab-ad8371cd5d0b" />


Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



