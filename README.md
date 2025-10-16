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

<img width="399" height="343" alt="image" src="https://github.com/user-attachments/assets/fc3ab060-87b6-4807-b341-762eca0d8496" />

<img width="455" height="475" alt="image" src="https://github.com/user-attachments/assets/c5c1bbd6-15b2-4302-9b90-edc856e701ce" />

**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.

**Program:**


Developed by:PAARKAVI A
RegisterNumber:25012275

i)
module e3(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)
module DE3 (x,y,z,dif,bor);

input x,y,z;

output dif,bor;

assign dif = x^y^z;

assign bor = ~x&z | ~x&y | y&z;

endmodule

**RTL Schematic**
<img width="1920" height="1080" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/88481980-c1f2-4301-afe1-8ed6fc8b3d34" />
<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/a8703f68-36e8-40c4-a83d-3dc10f9255a1" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/f649e8df-f0d1-4b9e-82b7-bd4a83654a2c" />
<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/fb1e975b-5907-42c1-9969-bcfcc75d71a0" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



