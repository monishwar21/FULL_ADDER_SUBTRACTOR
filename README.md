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
1) TRUTH TABLE FOR FULL ADDER
 
<img width="606" height="330" alt="FULLADD" src="https://github.com/user-attachments/assets/c63a6088-2b2a-42fb-938b-c23e13010cf9" />


2)TRUTH TABLE FOR SUBTRACTOR

<img width="606" height="330" alt="full subtractor" src="https://github.com/user-attachments/assets/f84de514-16a5-4682-9dea-96b6d778805b" />


**Procedure**

1)Type the program in Quartus software.

2)Compile and run the program.

3)Generate the RTL schematic and save the logic diagram.

4)Create nodes for inputs and outputs to generate the timing diagram.

5)For different input combinations generate the timing diagram.


**Program:**

PROGRAM FOR FULLADDER:

    module fa(a,b,cin,sum,carry);

    input a,b,cin;

    output sum,carry;

    assign sum=( (a ^ b)^cin);

    assign carry= ( (a & b)| ( cin &(a ^ b )));

    endmodule

PROGRAM FOR FULLSUBTRACTOR:

    module fs(a,b,bin,difference,borrow);

    input a,b,bin;

    output difference,borrow;

    assign difference= ( (a ^ b)^bin);

    assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

    endmodule


 Developed by:MONISHWAR K  RegisterNumber:25014914

**RTL Schematic**
1)FULLADDER

<img width="939" height="481" alt="Screenshot 2025-12-09 215433" src="https://github.com/user-attachments/assets/295e08a5-ae25-454c-aea0-6bc073146dec" />

2)FULLSUBTRACTOR

<img width="936" height="485" alt="Screenshot 2025-12-09 215446" src="https://github.com/user-attachments/assets/e25982c3-9c91-473c-aeec-68469912f9c3" />


**Output Timing Waveform**

1)FULL ADDER

<img width="932" height="483" alt="Screenshot 2025-12-09 215552" src="https://github.com/user-attachments/assets/687eb879-a8e5-40f6-a7f2-847011ec8812" />

2)FULL SUBTRACTOR

<img width="930" height="477" alt="Screenshot 2025-12-09 215605" src="https://github.com/user-attachments/assets/2d03524e-a6a6-41f7-a5ef-d9b8579162f1" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



