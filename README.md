# 8051-Assembly-Program-to-reverse-the-elements-in-an-array

AIM
To write a program for 8051 to get n size of array and print the array in reversed order in a different memory location.

SOFTWARE REQUIRED
Keil µVision IDE
Personel computer
ALGORITHM
Start the program.
Move the value from memory location 30H into accumulator A.
Copy the value of A into register R2 (used as a loop counter).
If A = 0, jump to DONE and stop execution.
Add 30H to A to form the starting address, store it in R0.
Load R1 with 40H (destination start address).
Copy data byte from source (@R0) to destination (@R1).
Decrement R0, increment R1, and decrement loop counter R2.
Repeat step 7 until R2 = 0.
End the program (infinite jump at DONE).
PROGRAM
ORG 0000H
MOV A,30H
MOV R2,A
JZ DONE
ADD A,#30H
MOV R0,A
MOV R1,#40H
AGAIN:
MOV A,@R0
MOV @R1,A
DEC R0
INC R1
DJNZ R2,AGAIN
DONE:
SJMP $
END
OUTPUT IMAGE FROM KEIL
SA1-2 SA1-1
RESULT
The 8051 program to get an array of n size and print it in reverse order in different memory address is successful.
