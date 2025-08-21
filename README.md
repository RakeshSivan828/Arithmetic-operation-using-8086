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
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1200:24         |
|         1201:34         |          1205:68         |
|         1202:12         |          1206:00         |
|         1203:34         |                          |



#### Manual Calculations

![WhatsApp Image 2025-08-21 at 21 34 34_f972801f](https://github.com/user-attachments/assets/9abbf4cf-1107-4675-a8bb-886bb201b450)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="637" height="401" alt="image" src="https://github.com/user-attachments/assets/fed86a22-182d-486e-833c-3d0a0219cc66" />



<img width="648" height="390" alt="image" src="https://github.com/user-attachments/assets/5794b89c-bd29-4ed9-bf37-d31047737cbe" />



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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1200:00         |
|         1201:34         |          1205:00         |
|         1202:12         |          1206:00         |
|         1203:34         |                          |

#### Manual Calculations

![WhatsApp Image 2025-08-21 at 21 45 38_a3277686](https://github.com/user-attachments/assets/959df3cc-8f6c-4a13-bd68-98e993715702)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="639" height="405" alt="image" src="https://github.com/user-attachments/assets/cb8abd9a-9211-48e1-8e91-4426a7eceee9" />
<img width="641" height="389" alt="image" src="https://github.com/user-attachments/assets/a08952d5-66ea-4db4-90b8-9cf7a6db0a05" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1200:44         |
|         1201:34         |          1205:51         |
|         1202:12         |          1206:97         |
|         1203:34         |          1207:0A         |

#### Manual Calculations

![WhatsApp Image 2025-08-21 at 21 58 57_66ae0884](https://github.com/user-attachments/assets/4c53c9f1-33cf-470f-a599-320b9ec2b581)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="641" height="403" alt="image" src="https://github.com/user-attachments/assets/0ee0cc52-932e-4d95-b8ec-2337fff39365" />
<img width="644" height="402" alt="image" src="https://github.com/user-attachments/assets/d8d3a250-9ad4-4998-84e7-183c00825719" />


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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200:12         |          1200:01         |
|         1201:34         |          1205:00         |
|         1202:12         |          1206:00         |
|         1203:34         |          1207:00         |

#### Manual Calculations

![WhatsApp Image 2025-08-21 at 22 06 49_372570e8](https://github.com/user-attachments/assets/23604f67-c214-433d-8f8c-7774d0ee2a85)


---
## OUTPUT FROM MASM SOFTWARE

<img width="639" height="401" alt="image" src="https://github.com/user-attachments/assets/ed90c2c5-2489-49e5-9b96-0710842ebd63" />

<img width="644" height="401" alt="image" src="https://github.com/user-attachments/assets/24d10b50-beda-4e1a-b821-70eb8fc19eae" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
