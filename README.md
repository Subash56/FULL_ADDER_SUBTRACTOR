### NAME:SUBASH B
### REG NO:24900843
## EXP NO:4 IMPLEMENTATION OF FULL ADDER AND FULL SUBTRACTOR CIRCUIT
## AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENTS REQUIRED:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime


## FULL ADDER

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

## FULL SUBTRACTOR

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
## TRUTH TABLE:
FULL ADDER:
![image](https://github.com/user-attachments/assets/73ac5923-56de-4d43-8bd1-8eb52b8910ca)

FULL SUBTRACTOR:
![image](https://github.com/user-attachments/assets/27a83ca4-29c5-46f1-bebe-2ec13a4a0516)

## PROCEDURE:

 1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram
## PROGRAM:
~~~
module Fulladder(a,b,c,sum,carry,diff,borrow);
input a,b,c;
output sum,carry,diff,borrow;
assign sum= (a^b^c);
assign carry= ((a^b)&c)|(a&b);
assign diff= (a^b^c);
assign borrow= ((~a&b)|(c&(~(a^b))));
endmodule
~~~

## RTL OUTPUT DIAGRAM:

![fulladder artial](https://github.com/user-attachments/assets/c70bbd25-cd85-4c9c-8dac-db37bfa00b7b)

## OUTPUT TIMING WAVEFORM
![fulladder waveform](https://github.com/user-attachments/assets/f20cdced-e121-4a31-951b-1eb1ccad197d)

## RESULT:
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



