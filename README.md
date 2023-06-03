# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
  
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D F2=xy’z+x’y’z+w’xy+wx’y+wxy

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B

## Procedure:
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: C.Prabha
RegisterNumber: 212222110032

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
module f1(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy
module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
*/
```

## RTL realization
### F1:
![image](https://github.com/22008837/Experiment--02-Implementation-of-combinational-logic-/assets/120194155/24874b80-7a70-4e57-9725-41e34a424b44)
### F2:
![image](https://github.com/22008837/Experiment--02-Implementation-of-combinational-logic-/assets/120194155/6028dcc0-5a2a-4b2a-aa21-e712eec27223)

## Timing Diagram:
### F1:
![image](https://github.com/22008837/Experiment--02-Implementation-of-combinational-logic-/assets/120194155/3263589c-4047-47b9-9df0-44eede262afc)
### F2:
![image](https://github.com/22008837/Experiment--02-Implementation-of-combinational-logic-/assets/120194155/f49c5d41-2ed6-48c1-9b06-519744381db6)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
