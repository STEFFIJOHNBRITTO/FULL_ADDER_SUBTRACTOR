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

![full addsub](https://github.com/user-attachments/assets/b62be1cd-674c-42e0-a38d-b9df01d266f1)

![Screenshot 2024-12-02 211726](https://github.com/user-attachments/assets/91e597f3-6072-4ded-ba93-d77704b7090f)


**Procedure**

Full Adder: Inputs: Three inputs: A, B (the two bits to be added), and Cin (the carry-in bit from a
 previous addition). Outputs: Two outputs: Sum (the resulting sum) and Cout (the carry-out bit).
 Logic: Sum = A ^ B ^ Cin (XOR operation). Cout = (A & B) | (A & Cin) | (B & Cin) (carry occurs if at
 least two inputs are 1).
 
 Full Subtractor: Inputs: Three inputs: A, B (the two bits, where A - B is calculated), and Bin (the
 borrow-in from a previous subtraction). Outputs: Two outputs: Diff (the resulting difference) and
 Bout (the borrow out bit). Logic: Diff = A ^ B ^ Bin (XOR operation). Bout = (~A & B) | ((~A | B) &
 Bin) (borrow occurs if A is less than B or needs a borrow). Both circuits follow simple XOR logic for
 the primary result and AND-OR logic to determine carry or borrow conditions
 

**Program:**

 Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
 
 Developed by: STEFFI J
 
 RegisterNumber: 24900405

 ```

 module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow); 
input a,b,cin,bin; output sum,carry,difference,borrow; 
assign sum=a^b^cin; 
assign carry=(a^b)&cin|a&b;
 assign difference=a^b^bin; 
assign borrow=~(a^b)&bin|(~a)&b;

```

**RTL Schematic**

![f addsub](https://github.com/user-attachments/assets/00c15eb3-d991-43b2-be78-6d563f1ca6af)


**Output Timing Waveform**

![f addsub](https://github.com/user-attachments/assets/b8a820ff-5672-41f3-bdb9-bdaccb0d86e1)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



