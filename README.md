Lab 1: Create a C program to find the sum of n natural numbers, compile it using gcc compiler. Verify the output of the C program after execution.

Step 1:
Create a new sum1ton.c file in the desired directory in Linux environment.

Here, I am using the GEDIT text editor from Ubuntu.

Write and save your C program in the text editor.


Step 2:
Compile your code using GCC compiler in the terminal window of Ubuntu enivronment and ensure there are no errors during compilation.

Step 3:
After compilation, the executable will be generated. Run the executable in terminal window to see the ouput.

Final Output:
In the below image we can observe the C code and the output together.
***
<details>
  <summary>Click to expand!</summary>
  <p>Your hidden content goes here.</p>
# My Project

## Instruction Table

|Sl. No | Instruction| Type |Description of the Instruction |Format                            | Binary Representation          |
|--------|----------------|---------------------------------------|------|-----------------------------------|--------------------------------|
|1| ADD r11, r12, r13  | R    |Perform Addition between the values stored in registers R11 and R12, and store the result in register R13| funct7 rs2 rs1 funct3 rd opcode   | 0000000 01101 01100 000 01011 0110011 |
|2| SUB r13, r11, r12  | R    |Perform Subtraction between the value stored in register R11 from R13, and store the result in register R12| funct7 rs2 rs1 funct3 rd opcode   | 0100000 01100 01011 000 01101 0110011 |
|3| AND r12, r11, r13  | R    | Perform Logical AND between the values stored in registers R11 and R12, and store the result in register R13 | ofunct7 rs2 rs1 funct3 rd opcode   | 0000000 01101 01011 111 01100 0110011 |
|4| OR r8, r12, r5     | R    | Perform Logical OR between the values stored in registers R8 and R12, and store the result in register R5|funct7 rs2 rs1 funct3 rd opcode   | 0000000 00101 01100 110 01000 0110011 |
|5| XOR r8, r11, r4    | R    | Perform Logical XOR between the values stored in registers R8 and R11, and store the result in register R5| funct7 rs2 rs1 funct3 rd opcode   | 0000000 00100 01011 100 01000 0110011 |
|6| SLT r30, r20, r4   | R    |Compare if the data in register R30 is less than that of R20, If yes, set destination register as 1, else, set it as 0| funct7 rs2 rs1 funct3 rd opcode   | 0000000 00100 10100 010 11110 0110011 |


</details>


