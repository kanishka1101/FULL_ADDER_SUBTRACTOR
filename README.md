# FULL_ADDER_SUBTRACTOR

Name: Kanishka G

Reference number : 25011903

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
<img width="792" height="418" alt="Screenshot 2025-11-23 130405" src="https://github.com/user-attachments/assets/b0d59b70-d013-4ddd-a449-8620c620be79" />
<img width="797" height="425" alt="Screenshot 2025-11-23 130515" src="https://github.com/user-attachments/assets/73fdd664-2b37-441f-8494-737e6ac742e8" />



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
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule

**RTL Schematic**
![ex3](https://github.com/user-attachments/assets/39f0abca-f90a-4819-b15f-a68fe5fb414b)
![ex4](https://github.com/user-attachments/assets/16f9c1d8-380b-429f-bbff-01a0c2982db8)



**Output Timing Waveform**
![waveform3](https://github.com/user-attachments/assets/d485ed46-7837-4920-b6b7-faee3c98e4e9)
![waveform3 2](https://github.com/user-attachments/assets/c74cb55a-7fbc-4b19-8f12-4fa22066f9cf)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



