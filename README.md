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
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: LOKESH KUMAR P
RegisterNumber: 212222240054 
```

```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.


Half subtractor: module halfsubtractor(A,B,Difference,Borrow); input A,B; output Difference,Borrow; assign Difference = (A^B); assign Borrow = (~A&B); endmodule

Full subtractor: module fullsub(A,B,C,Difference,Borrow); input A,B,C; output Difference,Borrow; assign Difference = (A^B^C); assign Borrow = (~A&(B^C)|(B&C)); endmodule 
```

## Output:

# Logic gate
# FULL SUBTRACTOR:
![241557376-9fb959ae-2711-4db1-8a6c-e2e9a1015a2e](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/0931335b-1920-45db-b4e1-a53f0f19971c)

# HALF SUBTRACTOR:
![241557419-3bca3502-5f1d-4be0-b1d1-e61d14c7c6a5](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/e09a227a-286c-4ac4-9ecc-d2927b9bb431)

# RTL realization
# FULL SUBTRACTOR:
![241557462-b3ffe8cb-6723-4f70-bc79-8ac4224dba60](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/4c89d379-5dfb-413d-9abe-0e4e43661650)

# HALF SUBTRACTOR:
![241557489-544c725d-3cc5-4ab4-a4d4-be2a590336d6](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/cb0bdf59-f18a-4b73-a1b0-2e3489d7095d)

# Timing diagram
# FULL SUBTRACTOR:
![241557573-af1b150e-fd7d-4ebd-ab04-c3890ab15a6d](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/ddd6180a-5847-46e7-a971-8c67175d8d81)

# HALF SUBTRACTOR:
![241557580-bd48f4b9-c719-4cba-b0ab-e6842337bef8](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/73c920ba-8afb-419f-b24a-60319795a3ad)

# Truth Table
![232961530-f3ad4dad-1a5d-43ab-b623-d4c1e970fc59](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/76c8f35f-69df-413e-ba1e-f0a5d254781e)

![232961530-f3ad4dad-1a5d-43ab-b623-d4c1e970fc59](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/33667f8f-7fcb-45e1-9d37-10dc9b98d89e)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
