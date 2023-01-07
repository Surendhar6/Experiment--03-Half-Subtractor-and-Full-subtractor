# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
Write the detailed procedure here 
Connect the power supply (+5V) to the circuit Switch ON the main switch If the output is 1,then the led glows.

## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
module HAdd(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff=(A^B);
assign borrow=(~A&B);
endmodule

module FSub(A,B,C,diff,borrow);
input A,B,C;
output diff,borrow;
assign diff=(A^B^C);
assign borrow=(~A&(B^C)|(B&C));
endmodule

Developed by: Surendhar A
RegisterNumber:  22009022
*/

## Output:

## Truthtable
![Screenshot_20230107_094016](https://user-images.githubusercontent.com/118352907/211160056-a81dfaf9-9da9-4969-9fe9-992540521c37.png)
![Screenshot_20230107_094821](https://user-images.githubusercontent.com/118352907/211160421-a654e994-a02f-450f-94bb-131095765fa9.png)

##  RTL realization
![Screenshot_20230107_082421](https://user-images.githubusercontent.com/118352907/211159931-f6cc6ba2-797d-4885-93da-911c9db91c83.png)
![Screenshot_20230107_094940](https://user-images.githubusercontent.com/118352907/211160468-51828a78-edb0-4b2d-9491-ff5375daf68d.png)

## Timing diagram 
![Screenshot_20230107_083554](https://user-images.githubusercontent.com/118352907/211159951-cf13c2f0-2741-4c8f-8a55-4b35fa72d30b.png)
![Screenshot_20230107_095440](https://user-images.githubusercontent.com/118352907/211160666-bea08da0-cff3-4012-ab68-67035888730c.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
