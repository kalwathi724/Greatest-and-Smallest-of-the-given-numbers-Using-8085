<img width="1465" height="835" alt="image" src="https://github.com/user-attachments/assets/81f999e4-06b1-45e3-b5f7-97330f09b5fe" /># Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
LDA 300H;
MOV C,A;
LXI H, 301H;
MOV A,M;
INX H;
DCR C;
LOOP: CMP M;
JNC NEXT;
MOV A,M;
NEXT: INX H;
DCR C;
JNZ LOOP;
STA 400H;
HLT;
## Output:
<img width="1458" height="694" alt="image" src="https://github.com/user-attachments/assets/47b87fc8-44f9-4a21-9d42-a613801741c0" />
<img width="302" height="405" alt="image" src="https://github.com/user-attachments/assets/48f9a905-9b0b-45c9-accc-aaaa17cf0ce7" />
<img width="300" height="376" alt="image" src="https://github.com/user-attachments/assets/3e7bf6f0-afb5-483a-afcd-18212b5d9d7a" />


## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
LDA 600H
MOV C,A
LXI H, 601H
MOV A,M
INX H
DCR C
LOOP: CMP M
JC NEXT
MOV A,M
NEXT: INX H
DCR C
JNZ LOOP
STA 701H
HLT
## Output:
<img width="1454" height="742" alt="image" src="https://github.com/user-attachments/assets/dff6aca3-69a0-4401-8c30-e5f3545d4e53" />
<img width="306" height="453" alt="image" src="https://github.com/user-attachments/assets/c8260310-b1f2-4c34-a872-407718c818a2" />
<img width="307" height="393" alt="image" src="https://github.com/user-attachments/assets/87c1f238-e39a-4968-a31c-2a1c7f110895" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
