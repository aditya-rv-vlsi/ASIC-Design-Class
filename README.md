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


Identify various RISC-V instruction type (R, I, S, B, U, J) and exact 32-bit instruction code in the instruction type format for below RISC-V instructions
ADD r11, r12, r13
SUB r13, r11, r12
AND r12, r11, r13
OR r8, r12, r5
XOR r8, r11, r4
SLT r30, r20, r4
ADDI r31, r21, 5
SW r21, r19, 4
SRL r26, r21, r20
BNE r0, r19, 20
BEQ r0, r0, 15
LW r23, r21, 2
SLL r25, r21, r20

The instructions format of a processor is the way in which machine language instructions are structured and organized for a processor to execute. It is made up of series of 0s and 1s, each containing information about the location and operation of data.
There are 6 instruction formats in RISC-V:

<li>R-format</li>
<li>I-format</li>
<li>S-format</li>
<li>B-format</li>
<li>U-format</li>
<li>J-format</li>


![image](https://github.com/user-attachments/assets/04fbc6f6-5f98-48b0-a346-292e0c9c115e)

## 1. R-type Instruction

In R-type instruction, R stands for register which means that operations are carried on the Registers and not on memory location. This instruction type is used to execute various arithmetic and logical operations. The entire 32 bits instruction is divided into 6 fields as shown below.

![image](https://github.com/user-attachments/assets/2ffba883-3d7d-4dce-b152-258a85fc1815)

<li>The first field in the instruction format is known as opcode, also referred as operation code.</li>
<li>The opcode is of length 7 bits and is used to determine the type of instruction format.</li>
<li>The next subfield is known as rd field which is referred as Destination Register.</li>
<li>The rd field is of length 5 bits and is used to store the final result of operation.</li>
<li>The next subfield is func3 also referred as function 3. </li>
<li>Here the ‘3’ represents the size of this field. </li>
<li>This field tells the detail about the operation, i.e., the type of arithmetic and logical that is performed.</li>
<li>The next two subfields are the source registers, rs1 and rs2 each of length 5 bits.</li>
<li>These are mainly used to store and manipulate the data during the execution of instructions.</li>
<li>The last subfield is func7 also referred as function 7. Here ‘7’ represents the size of the field. The function of func7 field is same as that of func3 field.</li>

## 2. I-type Instruction

In I-type instruction, I stand for immediate which means that operations use Registers and Immediate value for their execution and are not related with memory location. This instruction type is used in immediate and load operations. The entire 32 bits instruction is divided into 5 fields as shown below.

![image](https://github.com/user-attachments/assets/b4f0e45a-7c24-4864-978b-a4a9b658cc44)


<li>The first field in the instruction format is known as opcode, also referred as operation code. The opcode is of length 7 bits and is used to determine the type of instruction format.</li>
<li>The next subfield is known as rd field which is referred as Destination Register. The rd field is of length 5 bits and is used to store the final result of operation.</li>
<li>The next subfield is func3 also referred as function 3. Here the ‘3’ represents the size of this field. This field tells the detail about the operation, i.e., the type of arithmetic and logical that is performed.</li>
<li>The next subfield is the source registers, rs1 of length 5 bits. It is mainly used to store and manipulate the data during the execution of instructions.</li>
<li>The only difference between R-type and I-type is rs2 and func7 field of R-type has been replaced by 12-bits signed immediate, imm[11:0].</li>

## 3. S-type Instruction
   
In S-type instruction, S stand for store which means it is store type instruction that helps to store the value of register into the memory. Mainly, this instruction type is used for store operations. The entire 32 bits instruction is divided into 6 fields as shown below.

![image](https://github.com/user-attachments/assets/3c04cfaf-34b3-4a6c-9704-ed45d55c3401)

<li>The first field in the instruction format is known as opcode, also referred as operation code. </li>
<li>The opcode is of length 7 bits and is used to determine the type of instruction format.</li>
<li>S-type instructions encode a 12-bit signed immediate, with the top seven bits imm[11:5] in bits [31:25] of the instruction and the lower five bits imm[4:0] in bits [11:7] of the instruction.</li>
<li>S-type instruction doesn’t have rd fields which states that these instructions are not used to write value to a register, but to write/store a value to a memory.</li>
<li>The value to be stored is defined in rs1 field and address to which we have to store this value is calculated using rs1 and immediate field. The width of the operation and types of instruction is defined by func3, it can be a word, half-word or byte.</li>

## 4. B-type Instruction
   
In B-type instruction, B stand for branching which means it is mainly used for branching based on certain conditions. The entire 32 bits instruction is divided into 8 fields as shown below.

![image](https://github.com/user-attachments/assets/ae38579f-e051-4a5a-bbe1-42b68d629f98)

<li>The first field in the instruction format is known as opcode, also referred as operation code. </li>
<li>The opcode is of length 7 bits and is used to determine the type of instruction format.</li>
<li>B-type instructions encode a 12-bit signed immediate, with the most significant bit imm[12] in bit [31] of the instruction, six bits imm[10:5] in bits [25:30] of the instruction, four bits imm[4:1] in bits [11:8] and one bit imm[11] on bit[7].</li>
<li>There are two source registers rs1 and rs2 on which various operations are performed based on certain conditions, and those conditions are defined by func3 field.</li>
<li>After performing operations on the source register based on the conditions, it is evaluated that if the condition is true, Program Counter value gets updated by PC = Present PC Value + Immediate Value, and if the condition is false then PC will be given as PC = Present PC value + 4 bytes, which states that PC will move to next instruction set.</li>
<li>RV32 instructions are word-aligned, which means that address is always defined in the multiple of 4 bytes.</li>

## 5. U-type Instruction
   
In U-type instruction, U stand for Upper Immediate instructions which means it is simply used to transfer the immediate data into the destination register. The entire 32 bits instruction is divided into 3 fields as shown below.

![image](https://github.com/user-attachments/assets/e155a78d-489a-4b86-9e9f-9904401dfcc7)

<li>The first field in the instruction format is known as opcode, also referred as operation code.</li>
<li>The opcode is of length 7 bits and is used to determine the type of instruction format.</li>
<li>The U-type instruction only consists of two instructions, i.e., LUI and AUIPC.</li>
<li>For Example, lets take the instruction lui rd, imm and understand this instruction. lui x15, 0x13579 : This instruction will be executed and the immediate value 0x13579 will be written in the MSB of the rd x15, and it will look like x15 = 0x13579000.</li>

## 6. J-type Instruction
   
In U-type instruction, J stand for jump, which means that this instruction format is used to implement jump type instruction. The entire 32 bits instruction is divided into 6 fields as shown below.

![image](https://github.com/user-attachments/assets/06de5c85-ff12-4cc5-b301-758817730e78)

<li>The first field in the instruction format is known as opcode, also referred as operation code.</li>
<li>The opcode is of length 7 bits and is used to determine the type of instruction format.</li>
<li>The J-type instruction only consists of single instruction, JAL.</li>
<li>J-type instruction encode 20 bits signed immediate which is divided into four fields.</li>
<li>The J-type instructions are often used to perform jump to the desired memory location. </li>
<li>The address of the desired memory location is defined in the instruction. </li>
<li>These instructions are also used to implement loops.</li>



|Sl. No | Instruction| Type |Description of the Instruction |Format                            | Binary Representation          |
|--------|----------------|---------------------------------------|------|-----------------------------------|--------------------------------|
|1| ADD r11, r12, r13  |R|Perform Addition between the values stored in registers R12 and R13, and store the result in register R11|funct7_rs2_rs1_funct3_rd_opcode|0000000_01101_01100_000_01011_0110011|
|2| SUB r13, r11, r12  |R|Perform Subtraction between the value stored in register R12 from R11, and store the result in register R13|funct7_rs2_rs1_funct3_rd_opcode|0100000_01100_01011_000_01101_0110011|
|3| AND r12, r11, r13  |R|Perform Logical AND between the values stored in registers R11 and R13, and store the result in register R12 |funct7_rs2_rs1_funct3_rd_opcode|0000000_01101_01011_111_01100_0110011|
|4| OR r8, r12, r5     |R|Perform Logical OR between the values stored in registers R5 and R12, and store the result in register R8|funct7_rs2_rs1_funct3_rd_opcode|0000000_00101_01100_110_01000_0110011|
|5| XOR r8, r11, r4    |R|Perform Logical XOR between the values stored in registers R4 and R11, and store the result in register R8|funct7_rs2_rs1_funct3_rd_opcode|0000000_00100_01011_100_01000_0110011|
|6| SLT r30, r20, r4   |R|Compare if the data in register R30 is less than that of R20, If yes, set destination register as 1, else, set it as 0|funct7_rs2_rs1_funct3_rd_opcode|0000000_00100_10100_010_111100110011|
7| ADDI r31, r21, 5   |I|Perform addition between data in register R21 and Immediate value (5), and store the result in register R31|imm[11:0]_rs1_funct3_rd_opcode|000000000101_10101_000_11111_0010011|
|8| SW r21, r19, 4     |S|Store Word (32 bits or 4 bytes) from the address pointed by the sum of address held in register R19 and the immediate value (4) and store it in register R21 |imm[11:5]_rs2_rs1_funct3_imm[4:0]_opcode|0000000_10011_10101_010_00100_0100011|
|9| SRL r26, r21, r20  |R| Perform Shift Logical Right on data present in register R21, based on the data present in register R20, and store the result in register R26|funct7_rs2_rs1_funct3_rd_opcode|0000000_10100_10101_101_11010_0110011 |
|10| BNE r0, r19, 20    |B|Branch if the contents of registers R0 and R19 are not equal, to the address denoted by the sum of the address held by the program counter (PC) and the immediate value (20)|imm[12|10:5] rs2_rs1_funct3_imm[4:1|11]_opcode|000000_10011_00000_001_01000_1100011|
|11| BEQ r0, r0, 15     |B| Branch if the contents of registers R0 and R0 are equal, to the address denoted by the sum of the address held by the program counter (PC) and the immediate value (15)|[12|10:5] rs2 rs1_funct3_imm[4:1|11]_opcode|000000_00000_00000_000_01111_1100011|
|12| LW r23, r21, 2     |I|Load Word (32 bits or 4 bytes) from the address pointed by the sum of address held in register R21 and the immediate value (2) and store it in register R23|imm[11:0]_rs1_funct3_rd_opcode|000000000010_10101_010_10111_0000011|
|13| SLL r25, r21, r20  |R| Perform Shift Logical Left on data present in register R21, based on the data present in register R20, and store the result in register R25|funct7 rs2 rs1 funct3 rd opcode   | 0000000_10100_10101_001_11001_0110011|

</details>


