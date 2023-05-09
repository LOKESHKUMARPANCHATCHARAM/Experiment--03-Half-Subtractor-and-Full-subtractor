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
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: LOKESH KUMAR P
RegisterNumber: 212222240054 
*/
### HALF SUBTRACTOR:
```
module exp3(output B,D, input X,Y);
assign D = (X ^ Y);
assign B = (~X & Y);
endmodule
```


### FULL SUBTRACTOR:
```
module exp3(X,Y,Z,B,D);
input X,Y,Z;
output B,D;
assign D = (X^Y^Z);
assign B = (~X&(Y^Z)|(Y&Z));
endmodule
```


## Output:

### HALF SUBTRACTOR:

##  RTL realization
![Screenshot 2023-05-09 142256](https://user-images.githubusercontent.com/119644432/237046206-05fcc85f-f63d-4a27-aa22-856a1efe559c.png)


## Truthtable

![Screenshot 2023-05-09 142348](https://user-images.githubusercontent.com/119644432/237046790-1dd80368-8e5a-42c0-84c5-5537a3a664a3.png)


## Timing diagram 
![Screenshot 2023-05-09 142401](https://user-images.githubusercontent.com/119644432/237046630-3cb53861-e99b-405c-bcc4-ee16f1f0c923.png)


### FULL SUBTRACTOR:


##  RTL realization

![Screenshot 2023-05-09 142828](https://user-images.githubusercontent.com/119644432/237047727-fb2bc1fb-92e9-43d0-9c99-1e278b88bada.png)

## Truthtable
![Screenshot 2023-05-09 142848](https://user-images.githubusercontent.com/119644432/237047781-8ed930ac-df60-476a-b971-11b0d63e4205.png)

## Timing diagram 
![Screenshot 2023-05-09 142858](https://user-images.githubusercontent.com/119644432/237047835-23d20711-21d9-4fb5-8ce6-406e41e97e7e.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
