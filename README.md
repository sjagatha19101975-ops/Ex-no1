Arithmetic-operation-using-8086
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
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1600" height="844" alt="WhatsApp Image 2026-05-23 at 10 15 35 PM" src="https://github.com/user-attachments/assets/d1a6223c-2d75-4f3a-96a6-2bb0b2ebcb36" />


#### Manual Calculations

<img width="720" height="1280" alt="WhatsApp Image 2026-05-23 at 10 15 11 PM" src="https://github.com/user-attachments/assets/f8cf4114-7591-46e9-b805-01ef766bffbf" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="499" height="301" alt="image" src="https://github.com/user-attachments/assets/ad256a78-1281-4708-8111-82df8856358a" />


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
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table
<img width="1068" height="1280" alt="WhatsApp Image 2026-05-23 at 10 17 03 PM" src="https://github.com/user-attachments/assets/70f5a7d3-b8b8-4202-aa52-7e67d30d1e55" />

#### Manual Calculations

<img width="702" height="1280" alt="WhatsApp Image 2026-05-23 at 10 16 42 PM" src="https://github.com/user-attachments/assets/bb3213fe-7ba6-4ee9-ad4a-03a7e77e9830" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="798" height="496" alt="image" src="https://github.com/user-attachments/assets/a7355e7c-e568-43f8-8db1-7a02c4be2e37" />


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
ASSUME CS: CODE, DS: CODE
ORG 1000H
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
END
```

#### Output Table
<img width="1600" height="785" alt="WhatsApp Image 2026-05-23 at 10 19 55 PM" src="https://github.com/user-attachments/assets/b0a7ef42-2ec3-4716-85f4-7eb4e660878e" />
<img width="721" height="1280" alt="WhatsApp Image 2026-05-23 at 10 19 32 PM" src="https://github.com/user-attachments/assets/549e12b3-ecf4-4334-b036-44dec5d97750" />


#### Manual Calculations

<img width="685" height="1280" alt="WhatsApp Image 2026-05-23 at 10 17 44 PM" src="https://github.com/user-attachments/assets/d2ec1d22-5b02-4c56-a99c-7ca72d8b895f" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="807" height="516" alt="image" src="https://github.com/user-attachments/assets/7549f4eb-dab0-4aee-b75e-9f497fbac5ef" />

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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

<img width="1299" height="1600" alt="WhatsApp Image 2026-05-23 at 10 20 50 PM" src="https://github.com/user-attachments/assets/7d8759e2-452a-4bad-adc8-e4dff82828fe" />


#### Manual Calculations

<img width="746" height="1280" alt="WhatsApp Image 2026-05-23 at 10 20 23 PM" src="https://github.com/user-attachments/assets/e8e51f83-ec4a-415c-aa2e-42bf6af60b93" />


---
## OUTPUT FROM MASM SOFTWARE

<img width="798" height="511" alt="image" src="https://github.com/user-attachments/assets/4aef66c4-1e9a-4cea-aba5-c063d8cfe00f" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

