# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

### Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: P.Deepika.

RegisterNumber:  212221240035.

### Half Adder
```
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
### Full Adder
```
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
Logic symbol & Truthtable
### Output:
### RTL
![rtl1](https://user-images.githubusercontent.com/94154679/195987444-4d0fbcc4-1c38-46d8-8edb-860431579e18.jpg)

### TIMING DIAGRAM
![time1](https://user-images.githubusercontent.com/94154679/195987452-15752f15-ff1b-42ac-bdb9-8f3cf2c241cb.jpg)


### TRUTH TABLE 
![truth1](https://user-images.githubusercontent.com/94154679/195987463-947fea4b-bad0-424b-b806-ad73f4de6b6a.jpg)

### RTL
![rtl2](https://user-images.githubusercontent.com/94154679/195987474-4e7d1b6b-0b1e-46ce-9307-4d6b4a964b22.jpg)

### TIMING DIAGRAM
![time2](https://user-images.githubusercontent.com/94154679/195987478-afccb8d5-e0fe-4053-be64-1d3e8557b732.jpg)


### TRUTH TABLE
![truth2](https://user-images.githubusercontent.com/94154679/195987481-2fda028f-9df0-4b55-8b8f-626db8144557.jpg)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
