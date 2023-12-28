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

```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sanjai S
RegisterNumber:  23003393

HALF ADDER:

module halfadder(a,b,c,s);
input a,b;
output s,c;
xor(s,a,b);
and(c,a,b);
endmodule

FULL ADDER:

module fulladd(a,b,ci,s,Co);
input a,b,ci;
output s,co;
wire d,e,f;
xor(d,a,b);
xor(s,d,ci);
and(e,ci,d);
and(f,a,b);
or(co,e,f);
endmodule
```

## Logic symbol:

# HALF ADDER:
![half adder logic](https://user-images.githubusercontent.com/120194155/232570317-e7577ea1-58c7-4066-a23f-600fe3f15d11.png)

# FULL ADDER:
![full adder logic](https://user-images.githubusercontent.com/120194155/232570401-c97e4dcc-551d-459a-a2ea-388696958d9d.png)

## Truthtable:

# HALF ADDER:
![half adder truth](https://user-images.githubusercontent.com/120194155/232570504-1117cc92-ac1c-4f75-b4b6-ab230836ad46.png)

# FULL ADDER:
![full truth](https://user-images.githubusercontent.com/120194155/232570579-dd0910fb-d387-42ee-9830-73781c318bdb.png)

### RTL

RTL REALIZATION OF HALF ADDER:
![Screenshot 2023-04-05 142431](https://user-images.githubusercontent.com/120194155/232571149-4c83234e-7ab9-4ac1-865b-a2d7348515ca.png)

RTL REALIZATION OF FULL ADDER:
![ladder circuit](https://user-images.githubusercontent.com/120194155/232571329-a650b349-14f1-43ab-aa77-715c2dd0d1d5.png)

WAVE FORM:

HALF ADDER:
![HALF waveform](https://user-images.githubusercontent.com/120194155/232572389-e71c3826-2f8f-4331-81b0-d1bab2e61517.png)


FULL ADDER:
![full ladder waveform](https://user-images.githubusercontent.com/120194155/232572089-6badf782-5a5d-4f41-9289-0b20e4e0e9f5.png)

### Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.
