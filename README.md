# ARITHMETIC OPERATIONS USING 8086
# 8086 Assembly Language Programs for Arithmetic Operations
## AIM
To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.
---
## APPARATUS REQUIRED
* Personal Computer with MASM Software
---
## 1. ADDITION
#### Algorithm
1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.
## FLOW CHART
<img width="942" height="1412" alt="image" src="https://github.com/user-attachments/assets/2fd505db-5b31-4a42-a8b5-2ba2183d67da" />


#### Program
```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
START:
    MOV AX, CODE
    MOV DS, AX
    MOV SI, 2000H        
    MOV AX, [SI]         
    MOV BX, [SI+02H]     
    MOV CL, 00H          
    ADD AX, BX           
    JNC L1               
    INC CL               
L1:
    MOV [SI+04H], AX     
    MOV [SI+06H], CL     
    MOV AH, 4CH          
    INT 21H
CODE ENDS
END START
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       2000H                      2040H

|         2000H                  |
#### Manual Calculations
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/3fba5984-17db-4344-870f-a5e7bec936ef" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="657" height="452" alt="ADD" src="https://github.com/user-attachments/assets/f27a980d-c520-4eae-84a0-7b1219633fbb" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.
## FLOWCHART
<img width="929" height="1394" alt="image" src="https://github.com/user-attachments/assets/9eb367af-b337-46fe-9f44-be8dcb045e77" />

#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
START:
    MOV AX, CODE
    MOV DS, AX
    MOV SI, 2000H        
    MOV AX, [SI]         
    MOV BX, [SI+02H]     
    MOV CL, 00H          
    SUB AX, BX           
    JNC L1               
    INC CL               
L1:
    MOV [SI+04H], AX     
    MOV [SI+06H], CL     
    MOV AH, 4CH          
    INT 21H
CODE ENDS
END START
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/f02100a2-84be-4bc0-b79c-f77cab07fceb" />

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="636" height="417" alt="HARI SUB EXP 2" src="https://github.com/user-attachments/assets/8bbff3a9-6e76-4652-b9f0-d7c5f5bd3aad" />
<img width="622" height="417" alt="HARI SUB EXP 2 SCREENSHOT 2" src="https://github.com/user-attachments/assets/33ef2b43-aaaa-4aa8-af90-8456e0d4bcc9" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

## FLOWCHART

<img width="989" height="1484" alt="image" src="https://github.com/user-attachments/assets/36984d23-3667-45f6-be4a-1baa998de35e" />

#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
START:
    MOV AX, CODE
    MOV DS, AX
    MOV SI,2000H
    MOV DX,0000H
    MOV AX,[SI]
    MOV BX,[SI+02H]
    MUL BX
    MOV [SI+04H],AX
    MOV [SI+06H],DX
    MOV AH,4CH
    INT 21H
CODE ENDS
END START
```
#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="647" height="422" alt="mul (mpmc)" src="https://github.com/user-attachments/assets/e5c5341d-0c4d-4b83-8d73-5978a7f40bf3" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
   <img width="920" height="1114" alt="image" src="https://github.com/user-attachments/assets/5f6e6b0d-26d4-47d2-aa8a-0e488a44c931" />

#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
START:
    MOV AX, CODE
    MOV DS, AX
    MOV SI,2000H
    MOV DX,0000H        
    MOV AX,[SI]         
    MOV BX,[SI+02H]     
    DIV BX              
    MOV [SI+04H],AX     
    MOV [SI+06H],DX     
    INT 3               
CODE ENDS
END START
```
#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

## OUTPUT FROM MASM SOFTWARE

<img width="635" height="432" alt="DIVISION OUTPUT1" src="https://github.com/user-attachments/assets/dc111371-20c8-41a4-8fb4-5644968dc8c5" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.













