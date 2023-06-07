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
HALF SUBTRACTOR:
module halfsub(a,b,diff,borrow);
input a,b;
output diff,borrow;
wire x;
xor(diff,a,b);
not(x,a);
and(borrow,x,b);
endmodule


FULL SUBTRACTOR:
module fullsub(a,b,c,diff,borrow);
input a,b,c;
output borrow,diff;
wire an,q,r,s,t,cn,u;
not(an,a);
not(cn,c);
xor(q,a,b);
xor(diff,q,c);
and(s,a,b);
and(t,q,cn);
or(borrow,s,t);
endmodule
```

### Output:
### Truthtable:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/8422c7b2-9ece-4cc9-8bf3-2f04c10b5359)
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/2a3d4479-b7d8-4038-beb2-c9d448e9ee62)

### RTL realization:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/9ed85cc4-1cbf-4b16-af2a-28a052774028)

![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/270b7a4b-7753-44ab-813e-bb09594f7bea)


### Timing diagram:
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/c49cfc79-da53-42f4-9007-bf8138beed41)
![image](https://github.com/LOKESHKUMARPANCHATCHARAM/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119644432/045fa48b-c8f4-4aa1-b661-712a85ab7dff)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
