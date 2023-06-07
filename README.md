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


## Program
half subtractor
module HalfSub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference=(a^b);
assign borrow=(~a&b);
endmodule
full subtractor
module FullSub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assignborrow=(~a&(b^c)|(b&c));
assign difference=(a^b^c);
endmodule
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: mohamed yahya J 
Register212222050037  
*/

## Output:
'''
'''
'''
## Truthtable
half subtractor
![image](https://github.com/mohammadyahya10/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/130548526/142aab10-1a35-4369-9573-867871e40555)
full subtractor
![image](https://github.com/mohammadyahya10/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/130548526/f39a56cb-b881-479e-be0c-0ab4090ab9a0)




##  RTL realization
half subtractor
![image](https://github.com/mohammadyahya10/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/130548526/6cde6f61-859f-4dbe-ba13-0f7fda308f32)
full subtractor
![image](https://github.com/mohammadyahya10/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/130548526/9bf68085-279b-47e6-8270-8df9e6f565fb)


## Timing diagram 
![image](https://github.com/mohammadyahya10/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/130548526/f650c202-4bf0-4d32-bd44-5ac2365c286f)
![image](https://github.com/mohammadyahya10/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/130548526/0abe52c1-98fe-4408-87ec-2d897f9627a7)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
