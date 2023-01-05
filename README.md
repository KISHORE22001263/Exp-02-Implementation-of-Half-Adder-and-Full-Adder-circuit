developed by:-KISHORE.B  

reference number:-22001263

## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Figure -02 FULL ADDER 

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
````
 HALF ADDER:
module HALFADDER(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

  FULL ADDER:
module FULLADDER(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
````

## LOGIC SYMBOL:  
<img width="162" alt="210394807-f0abebca-ed18-4300-9533-c8be717bf3d1" src="https://user-images.githubusercontent.com/121484538/210770218-0dccde10-2d39-4223-bd34-d0e5dd41caaa.png">

<img width="145" alt="210394842-56ad9780-b0bf-4091-8330-58f7b0a9b1bb" src="https://user-images.githubusercontent.com/121484538/210770276-f9185e2a-b104-47f8-94ae-4eabd711a850.png">

<img width="157" alt="210394854-0f7bebd5-084e-42a4-b621-a96ba502d937" src="https://user-images.githubusercontent.com/121484538/210770353-03cef48d-f499-4472-ad8f-8ce64877e3ca.png">




## Output:

## RTL REALIZATION:
## HALF ADDER:
![Screenshot_20230103_052923](https://user-images.githubusercontent.com/121484538/210356501-143e3c3c-29d1-45be-a891-211d7fc90ac4.png)

##  FULL ADDER:
![Screenshot_20230103_050457](https://user-images.githubusercontent.com/121484538/210356534-d1b138fe-940d-413b-958f-359b2fb3fb77.png)

## TIMING DIAGRAM:
- ## HALF ADDER:

![Screenshot_20230105_052301](https://user-images.githubusercontent.com/121484538/210776984-5a01d300-4fb1-4bc8-af7b-d05ab85f3478.png)


- ## FULL ADDER:

![Screenshot_20230105_053430](https://user-images.githubusercontent.com/121484538/210777046-a5c7cd38-3783-4353-8ff6-9c2690a7d11e.png)


## TRUTH TABLE :

- ### HALF ADDER:  
![210396385-88c8d334-817f-438d-a83a-76ff5151a49a](https://user-images.githubusercontent.com/121484538/210770046-5ed837a8-9618-4e98-aa57-d56552d79d3f.jpg)



- ### FULL ADDER:
![210396429-e8b265c9-05a8-4cc8-b3ed-e540335a6e7d](https://user-images.githubusercontent.com/121484538/210770082-ad7c5b55-5c35-4d72-abce-d298ea5419de.jpg)


## Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
