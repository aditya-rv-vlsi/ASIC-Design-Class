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

| Instruction        | Type | Format                            | Binary Representation          |
|--------------------|------|-----------------------------------|--------------------------------|
| ADD r11, r12, r13  | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 01101 01100 000 01011 0110011 |
| SUB r13, r11, r12  | R    | funct7 rs2 rs1 funct3 rd opcode   | 0100000 01100 01011 000 01101 0110011 |
| AND r12, r11, r13  | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 01101 01011 111 01100 0110011 |
| OR r8, r12, r5     | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 00101 01100 110 01000 0110011 |
| XOR r8, r11, r4    | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 00100 01011 100 01000 0110011 |
| SLT r30, r20, r4   | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 00100 10100 010 11110 0110011 |
| ADDI r31, r21, 5   | I    | imm[11:0] rs1 funct3 rd opcode    | 000000000101 10101 000 11111 0010011 |
| SW r21, r19, 4     | S    | imm[11:5] rs2 rs1 funct3 imm[4:0] opcode | 0000000 10011 10101 010 00100 0100011 |
| SRL r26, r21, r20  | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 10100 10101 101 11010 0110011 |
| BNE r0, r19, 20    | B    | imm[12|10:5] rs2 rs1 funct3 imm[4:1|11] opcode | 000000 10011 00000 001 01000 1100011 |
| BEQ r0, r0, 15     | B    | imm[12|10:5] rs2 rs1 funct3 imm[4:1|11] opcode | 000000 00000 00000 000 01111 1100011 |
| LW r23, r21, 2     | I    | imm[11:0] rs1 funct3 rd opcode    | 000000000010 10101 010 10111 0000011 |
| SLL r25, r21, r20  | R    | funct7 rs2 rs1 funct3 rd opcode   | 0000000 10100 10101 001 11001 0110011 |

</details>


