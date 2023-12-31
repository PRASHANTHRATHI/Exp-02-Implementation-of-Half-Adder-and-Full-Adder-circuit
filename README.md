## NAME:PRASHANTH.K
## REGISTER NUMBER: 212223230152


# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## Theory:
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits. 
Sum = A’B+AB’ =A ⊕ B Carry = AB
#### Figure -01 HALF ADDER 
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/881166b3-0966-425d-b01c-e7e9d867e0dc)


### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
#### Figure -02 FULL ADDER 
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/b30284b0-586c-467b-934b-07530c4f772f)

### Program:
## HALF ADDER
```
module ha(sum,carry,a,b);
output sum,carry;
input a,b;
assign sum=a^b;
assign carry=a&b;
endmodule
```
## FULL ADDER
```
module FULLADDER(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire x,p,q,r;
xor(x,b,c);
xor(sum,x,a);
and(p,a,b);
and(q,b,c);
and(r,a,c);
or(carry,p,q,r);
endmodule
```
### Output:
### RTL
##  HALF ADDER
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/6336b07b-a7c8-4b67-9450-50738c06af7e)
## FULL ADDER
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/94f242f8-0a3c-44a2-be52-5b11c69c5644)


### TIMING DIAGRAM
## HALF ADDER
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/c7dd06ed-4778-4a3f-9ecc-040e432fc3e9)
## FULL ADDER
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/cc103f10-4765-4c8a-9e5e-502d60ca5c19)

### TRUTH TABLE 
## HALF ADDER
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/4ffb9b2c-1be0-4a87-9eca-d3fd196c2c99)
## FULL ADDER
![image](https://github.com/PRASHANTHRATHI/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145743120/8ccd5898-5c0b-4852-a5a0-405adfcf7f19)

### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
