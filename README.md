# Arithmetic-operation-using-8086
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
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H

MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX

JNC L1
INC CL
L1:

MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL

MOV AH,4CH
INT 21H

CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200              |            68            |
|       1201              |            24            |

#### Manual Calculations
<img width="1280" height="796" alt="image" src="https://github.com/user-attachments/assets/a637e6f4-c6b0-4c3a-a3f0-5ba18625b8ae" />



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/cd27152f-01d2-4d2b-b835-21436c956484" />



## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H

MOV CL,00H
MOV AX,1234H
MOV BX,1234H
SUB AX,BX

JNC L1
INC CL
L1:

MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL

MOV AH,4CH
INT 21H

CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|             1200        |           00             |
|             1201        |           00             |

#### Manual Calculations
<img width="1280" height="910" alt="image" src="https://github.com/user-attachments/assets/b6f90c2c-92f0-49da-bae6-4f61d6aa3f5b" />




## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/d55fa104-84c2-485b-b186-6f087d92effd" />





## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm

CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H

MOV AX, 1234H
MOV BX, 1234H
MUL BX

MOV SI, 1200H
MOV [SI], AX
MOV [SI+02H], DX

MOV AH, 4CH
INT 21H

CODE ENDS
END



```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|           1200          |            90            |
|           1201          |            5A            |

#### Manual Calculations
<img width="689" height="720" alt="image" src="https://github.com/user-attachments/assets/797a8a55-d2e6-47cc-b54a-8e40dd2d0889" />



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/f0200a44-0c1d-4624-87c1-d6457623d2c9" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H

MOV CL, 00H
MOV AX, 0084H
MOV BX, 0004H
MOV DX, 0000H
DIV BX

L1:
MOV SI, 1200H
MOV [SI], AX
MOV [SI+2], DX
MOV AH, 4CH
INT 21H

CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|            1200         |           21             |
|            1201         |           00             |

#### Manual Calculations
<img width="1280" height="737" alt="image" src="https://github.com/user-attachments/assets/1af771a0-ea81-45c1-85f5-0d96c6895d38" />




## OUTPUT FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/7d3dee01-b052-4505-860b-fadaf8caa321" />






## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

