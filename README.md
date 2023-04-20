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


## Program:
```
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: MOHAMMED IMTHIYAS
RegisterNumber: 212222230083
HALF SUBTRACTOR

module HalfSubtractor(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire x;
xor (Diff, A,B);
not(x,A);
and(Borrow,x,B);
endmodule

FULL SUBTRACTOR

module FullSubtractor(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
*/
```

## Output:

### HALF SUBRACTOR :
### LOGIC SYMBOL:


![image](https://user-images.githubusercontent.com/120353416/233367555-b4e181bc-8cb2-457c-b295-64cfdd3303c3.png)


## Truthtable


![image](https://user-images.githubusercontent.com/120353416/233367634-be010dd4-e02f-4849-9619-79fd29420ec3.png)




##  RTL realization


![image](https://user-images.githubusercontent.com/120353416/233367716-6e39a04d-616e-4e35-a551-da0822f49656.png)


### TIMING DIAGRAM

![image](https://user-images.githubusercontent.com/120353416/233367964-4c79b0cd-4188-4cb3-8f98-7871ff9e4e87.png)

## FULL SUBRACTOR:
LOGIC

![image](https://user-images.githubusercontent.com/120353416/233368188-1f0bd406-ff0d-4aee-88c6-0806c86fbf7f.png)

### Truthtable

![image](https://user-images.githubusercontent.com/120353416/233368334-6b59e49a-6e48-499e-9ea0-6e479ef6048e.png)

## RTL realization

![image](https://user-images.githubusercontent.com/120353416/233368572-b7f6e981-b5f4-4a61-befa-bc78322ddc5a.png)

### Timing diagram

![image](https://user-images.githubusercontent.com/120353416/233368711-43a14cbf-ce47-47fa-9d03-7730e1bb115c.png)





## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
