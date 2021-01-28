<div align="center">

# AVR Instruction Set

</div>

Summary from [Official PDF](http://ww1.microchip.com/downloads/en/devicedoc/atmel-0856-avr-instruction-set-manual.pdf).

Also see [AVR All Opcodes Table](http://lyons42.com/AVR/Opcodes/AVRAllOpcodes.html).

## CPU Versions

- AVR - AT90 - Original instruction set from 1995.
- AVRe - megaAVR® - Multiply (xMULxx), Move Word (MOVW), and enhanced Load Program
  Memory (LPM) added to the AVR instruction set. No timing differences.
- AVRe - tinyAVR® - Multiply not included, but else equal to AVRe for megaAVR.
- AVRxm - XMEGA® - Significantly different timing compared to AVR(e). The Read Modify Write
  (RMW) and DES encryption instructions are unique to this version.
- AVRxt - (AVR) - AVR 2016 and onwards. This variant is based on AVRe and AVRxm.
  Closer related to AVRe, but with improved timing.
- AVRrc - tinyAVR - The Reduced Core AVR CPU was developed for ultra-low pinout (6-pin)
  size constrained devices. The AVRrc therefore only has a 16 registers
  register-file (R31-R16) and a limited instruction set.

## Registers and Operands

- Rd - Destination (and source) register in the Register File
- Rr - Source register in the Register File
- R - Result after instruction is executed
- K - Constant data
- k - Constant address
- b - Bit in the Register File or I/O Register (3-bit)
- s - Bit in the Status Register (3-bit)
- X,Y,Z - Indirect Address Register (X=R27:R26, Y=R29:R28, and Z=R31:R30)
- A - I/O location address
- q - Displacement for direct addressing (6-bit)

## Status Register (SREG)

- C - Carry Flag
- Z - Zero Flag
- N - Negative Flag
- V - Two’s complement overflow indicator
- S - N ⊕ V, for signed tests
- H - Half Carry Flag
- T - Transfer bit used by BLD and BST instructions I Global Interrupt Enable/Disable Flag

## Convert table between Markdown ↔ CSV

Regex replace all: `\\n` ↔ `\n` and `\|` ↔ `\t`.

## Arithmetic and Logic

| Mnemonic | Operands | Description                              | Operation                                                                                         | Flags       | AVR #Clocks | AVRxm #Clocks | AVRxt #Clocks | AVRrc #Clocks |
| -------- | -------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------- | ----------- | ----------- | ------------- | ------------- | ------------- |
| ADC      | Rd, Rr   | Add with Carry                           | Rd ← Rd + Rr + C                                                                                  | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| ADD      | Rd, Rr   | Add without Carry                        | Rd ← Rd + Rr                                                                                      | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| ADIW     | Rd, K    | Add Immediate to Word                    | Rd ← Rd + 1:Rd + K                                                                                | Z,C,N,V,S   | 2           | 2             | 2             | N/A           |
| AND      | Rd, Rr   | Logical AND                              | Rd ← Rd • Rr                                                                                      | Z,N,V,S     | 1           | 1             | 1             | 1             |
| ANDI     | Rd, K    | Logical AND with Immediate               | Rd ← Rd • K                                                                                       | Z,N,V,S     | 1           | 1             | 1             | 1             |
| CBR      | Rd,K     | Clear Bit(s) in Register                 | Rd ← Rd • ($FFh - K)                                                                              | Z,N,V,S     | 1           | 1             | 1             | 1             |
| CLR      | Rd       | Clear Register                           | Rd ← Rd ⊕ Rd                                                                                      | Z,N,V,S     | 1           | 1             | 1             | 1             |
| COM      | Rd       | One’s Complement                         | Rd ← $FF - Rd                                                                                     | Z,C,N,V,S   | 1           | 1             | 1             | 1             |
| DEC      | Rd       | Decrement                                | Rd ← Rd - 1                                                                                       | Z,N,V,S     | 1           | 1             | 1             | 1             |
| DES      | K        | Data Encryption                          | "if (H = 0) then R15:R0 ← Encrypt(R15: R0, K)\nelse if (H = 1) then R15:R0 ← Decrypt(R15: R0, K)" |             | N/A         | 1/2           | N/A           | N/A           |
| EOR      | Rd, Rr   | Exclusive OR                             | Rd ← Rd ⊕ Rr                                                                                      | Z,N,V,S     | 1           | 1             | 1             | 1             |
| FMUL     | Rd,Rr    | Fractional Multiply Unsigned             | R1:R0 ← Rd x Rr<<1 (UU)                                                                           | Z,C         | 2           | 2             | 2             | N/A           |
| FMULS    | Rd,Rr    | Fractional Multiply Signed               | R1:R0 ← Rd x Rr<<1 (SS)                                                                           | Z,C         | 2           | 2             | 2             | N/A           |
| FMULSU   | Rd,Rr    | Fractional Multiply Signed with Unsigned | R1:R0 ← Rd x Rr<<1 (SU)                                                                           | Z,C         | 2           | 2             | 2             | N/A           |
| INC      | Rd       | Increment                                | Rd ← Rd + 1                                                                                       | Z,N,V,S     | 1           | 1             | 1             | 1             |
| MUL      | Rd,Rr    | Multiply Unsigned                        | R1:R0 ← Rd x Rr (UU)                                                                              | Z,C         | 2           | 2             | 2             | N/A           |
| MULS     | Rd,Rr    | Multiply Signed                          | R1:R0 ← Rd x Rr (SS)                                                                              | Z,C         | 2           | 2             | 2             | N/A           |
| MULSU    | Rd,Rr    | Multiply Signed with Unsigned            | R1:R0 ← Rd x Rr (SU)                                                                              | Z,C         | 2           | 2             | 2             | N/A           |
| NEG      | Rd       | Two’s Complement                         | Rd ← $00 - Rd                                                                                     | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| OR       | Rd, Rr   | Logical OR                               | Rd ← Rd v Rr                                                                                      | Z,N,V,S     | 1           | 1             | 1             | 1             |
| ORI      | Rd, K    | Logical OR with Immediate                | Rd ← Rd v K                                                                                       | Z,N,V,S     | 1           | 1             | 1             | 1             |
| SBC      | Rd, Rr   | Subtract with Carry                      | Rd ← Rd - Rr - C                                                                                  | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| SBCI     | Rd, K    | Subtract Immediate with Carry            | Rd ← Rd - K - C                                                                                   | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| SBIW     | Rd, K    | Subtract Immediate from Word             | Rd + 1:Rd ← Rd + 1:Rd - K                                                                         | Z,C,N,V,S   | 2           | 2             | 2             | N/A           |
| SBR      | Rd,K     | Set Bit(s) in Register                   | Rd ← Rd v K                                                                                       | Z,N,V,S     | 1           | 1             | 1             | 1             |
| SER      | Rd       | Set Register                             | Rd ← $FF                                                                                          |             | 1           | 1             | 1             | 1             |
| SUB      | Rd, Rr   | Subtract without Carry                   | Rd ← Rd - Rr                                                                                      | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| SUBI     | Rd, K    | Subtract Immediate                       | Rd ← Rd - K                                                                                       | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| TST      | Rd       | Test for Zero or Minus                   | Rd ← Rd • Rd                                                                                      | Z,N,V,S     | 1           | 1             | 1             | 1             |

## Bit and Bit-test

| Mnemonic | Operands | Description                     | Operation                               | Flags     | AVR #Clocks | AVRxm #Clocks | AVRxt #Clocks | AVRrc #Clocks |
| -------- | -------- | ------------------------------- | --------------------------------------- | --------- | ----------- | ------------- | ------------- | ------------- |
| ASR      | Rd       | Arithmetic Shift Right          | Rd(n) ← Rd(n+1), n=0..6                 | Z,C,N,V   | 1           | 1             | 1             | 1             |
| BCLR     | s        | Flag Clear                      | SREG(s) ← 0                             | SREG(s)   | 1           | 1             | 1             | 1             |
| BLD      | Rd, b    | Bit load from T to Register     | Rd(b) ← T                               |           | 1           | 1             | 1             | 1             |
| BSET     | s        | Flag Set                        | SREG(s) ← 1                             | SREG(s)   | 1           | 1             | 1             | 1             |
| BST      | Rr, b    | Bit Store from Register to T    | T ← Rr(b)                               | T         | 1           | 1             | 1             | 1             |
| CBI      | A, b     | Clear Bit in I/O Register       | I/O(A, b) ← 0                           |           | 2           | 1             | 1             | 1             |
| CLC      |          | Clear Carry                     | C ← 0                                   | C         | 1           | 1             | 1             | 1             |
| CLH      |          | Clear Half Carry Flag in SREG   | H ← 0                                   | H         | 1           | 1             | 1             | 1             |
| CLI      |          | Global Interrupt Disable        | I ← 0                                   | I         | 1           | 1             | 1             | 1             |
| CLN      |          | Clear Negative Flag             | N ← 0                                   | N         | 1           | 1             | 1             | 1             |
| CLS      |          | Clear Signed Test Flag          | S ← 0                                   | S         | 1           | 1             | 1             | 1             |
| CLT      |          | Clear T in SREG                 | T ← 0                                   | T         | 1           | 1             | 1             | 1             |
| CLV      |          | Clear Two’s Complement Overflow | V ← 0                                   | V         | 1           | 1             | 1             | 1             |
| CLZ      |          | Clear Zero Flag                 | Z ← 0                                   | Z         | 1           | 1             | 1             | 1             |
| LSL      | Rd       | Logical Shift Left              | "Rd(n+1) ← Rd(n)\nRd(0) ← 0\nC ← Rd(7)" | Z,C,N,V,H | 1           | 1             | 1             | 1             |
| LSR      | Rd       | Logical Shift Right             | "Rd(n) ← Rd(n+1)\nRd(7) ← 0\nC ← Rd(0)" | Z,C,N,V   | 1           | 1             | 1             | 1             |
| ROL      | Rd       | Rotate Left Through Carry       | "Rd(0) ← C\nRd(n+1) ← Rd(n)\nC ← Rd(7)" | Z,C,N,V,H | 1           | 1             | 1             | 1             |
| ROR      | Rd       | Rotate Right Through Carry      | "Rd(7) ← C\nRd(n) ← Rd(n+1)\nC ← Rd(0)" | Z,C,N,V   | 1           | 1             | 1             | 1             |
| SBI      | A, b     | Set Bit in I/O Register         | I/O(A, b) ← 1                           |           | 2           | 1             | 1             | 1             |
| SEC      |          | Set Carry                       | C ← 1                                   | C         | 1           | 1             | 1             | 1             |
| SEH      |          | Set Half Carry Flag in SREG     | H ← 1                                   | H         | 1           | 1             | 1             | 1             |
| SEI      |          | Global Interrupt Enable         | I ← 1                                   | I         | 1           | 1             | 1             | 1             |
| SEN      |          | Set Negative Flag               | N ← 1                                   | N         | 1           | 1             | 1             | 1             |
| SES      |          | Set Signed Test Flag            | S ← 1                                   | S         | 1           | 1             | 1             | 1             |
| SET      |          | Set T in SREG                   | T ← 1                                   | T         | 1           | 1             | 1             | 1             |
| SEV      |          | Set Two’s Complement Overflow   | V ← 1                                   | V         | 1           | 1             | 1             | 1             |
| SEZ      |          | Set Zero Flag                   | Z ← 1                                   | Z         | 1           | 1             | 1             | 1             |
| SWAP     | Rd       | Swap Nibbles                    | Rd(3..0) ↔ Rd(7..4)                     |           | 1           | 1             | 1             | 1             |

## Branch

| Mnemonic | Operands | Description                         | Operation                             | Flags       | AVR #Clocks | AVRxm #Clocks | AVRxt #Clocks | AVRrc #Clocks |
| -------- | -------- | ----------------------------------- | ------------------------------------- | ----------- | ----------- | ------------- | ------------- | ------------- |
| BRBC     | s, k     | Branch if Status Flag Cleared       | if (SREG(s) = 0) then PC ← PC + k + 1 |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRBS     | s, k     | Branch if Status Flag Set           | if (SREG(s) = 1) then PC ← PC + k + 1 |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRCC     | k        | Branch if Carry Cleared             | if (C = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRCS     | k        | Branch if Carry Set                 | if (C = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BREQ     | k        | Branch if Equal                     | if (Z = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRGE     | k        | Branch if Greater or Equal, Signed  | if (N ⊕ V= 0) then PC ← PC + k + 1    |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRHC     | k        | Branch if Half Carry Flag Cleared   | if (H = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRHS     | k        | Branch if Half Carry Flag Set       | if (H = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRID     | k        | Branch if Interrupt Disabled        | if (I = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRIE     | k        | Branch if Interrupt Enabled         | if (I = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRLO     | k        | Branch if Lower                     | if (C = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRLT     | k        | Branch if Less Than, Signed         | if (N ⊕ V= 1) then PC ← PC + k + 1    |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRMI     | k        | Branch if Minus                     | if (N = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRNE     | k        | Branch if Not Equal                 | if (Z = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRPL     | k        | Branch if Plus                      | if (N = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRSH     | k        | Branch if Same or Higher            | if (C = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRTC     | k        | Branch if T Flag Cleared            | if (T = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRTS     | k        | Branch if T Flag Set                | if (T = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRVC     | k        | Branch if Overflow Flag is Cleared  | if (V = 0) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| BRVS     | k        | Branch if Overflow Flag is Set      | if (V = 1) then PC ← PC + k + 1       |             | 1 / 2       | 1 / 2         | 1 / 2         | 1 / 2         |
| CALL     | k        | Call Subroutine                     | PC ← k                                |             | 4 / 5(1)    | 3 / 4(1)      | 3 / 4         | N/A           |
| CP       | Rd,Rr    | Compare                             | Rd - Rr                               | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| CPC      | Rd,Rr    | Compare with Carry                  | Rd - Rr - C                           | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| CPI      | Rd,K     | Compare with Immediate              | Rd - K                                | Z,C,N,V,S,H | 1           | 1             | 1             | 1             |
| CPSE     | Rd,Rr    | Compare, skip if Equal              | if (Rd = Rr) PC ← PC + 2 or 3         |             | 1 / 2 / 3   | 1 / 2 / 3     | 1 / 2 / 3     | 1 / 2         |
| EICALL   |          | Extended Indirect Call to (Z)       | "PC(15:0) ← Z\nPC(21:16) ← EIND"      |             | 4(1)        | 3(1)          | 2 / 3         | N/A           |
| EIJMP    |          | Extended Indirect Jump to (Z)       | "PC(15:0) ← Z\nPC(21:16) ← EIND"      |             | 2           | 2             | 2             | N/A           |
| ICALL    |          | Indirect Call to (Z)                | "PC(15:0) ← Z\nPC(21:16) ← 0"         |             | 3 / 4(1)    | 2 / 3(1)      | 2 / 3         | 3(1)          |
| IJMP     |          | Indirect Jump to (Z)                | "PC(15:0) ← Z\nPC(21:16) ← 0"         |             | 2           | 2             | 2             | 2             |
| JMP      | k        | Jump                                | PC ← k                                |             | 3           | 3             | 3             | N/A           |
| RCALL    | k        | Relative Call Subroutine            | PC ← PC + k + 1                       |             | 3 / 4(1)    | 2 / 3(1)      | 2 / 3         | 3(1)          |
| RET      |          | Subroutine Return                   | PC ← STACK                            |             | 4 / 5(1)    | 4 / 5(1)      | 4 / 5         | 6(1)          |
| RETI     |          | Interrupt Return                    | PC ← STACK                            | I           | 4 / 5(1)    | 4 / 5(1)      | 4 / 5         | 6(1)          |
| RJMP     | k        | Relative Jump                       | PC ← PC + k + 1                       |             | 2           | 2             | 2             | 2             |
| SBIC     | A, b     | Skip if Bit in I/O Register Cleared | if (I/O(A,b) = 0) PC ← PC + 2 or 3    |             | 1 / 2 / 3   | 2 / 3 / 4     | 1 / 2 / 3     | 1 / 2         |
| SBIS     | A, b     | Skip if Bit in I/O Register Set     | If (I/O(A,b) =1) PC ← PC + 2 or 3     |             | 1 / 2 / 3   | 2 / 3 / 4     | 1 / 2 / 3     | 1 / 2         |
| SBRC     | Rr, b    | Skip if Bit in Register Cleared     | if (Rr(b) = 0) PC ← PC + 2 or 3       |             | 1 / 2 / 3   | 1 / 2 / 3     | 1 / 2 / 3     | 1 / 2         |
| SBRS     | Rr, b    | Skip if Bit in Register Set         | if (Rr(b) = 1) PC ← PC + 2 or 3       |             | 1 / 2 / 3   | 1 / 2 / 3     | 1 / 2 / 3     | 1 / 2         |

## Data Transfer

| Mnemonic | Operands | Description                                     | Operation                                   | Flags | AVR #Clocks | AVRxm #Clocks | AVRxt #Clocks | AVRrc #Clocks |
| -------- | -------- | ----------------------------------------------- | ------------------------------------------- | ----- | ----------- | ------------- | ------------- | ------------- |
| ELPM     |          | Extended Load Program Memory                    | R0 ← (RAMPZ:Z)                              |       | 3           | 3             | 3             | N/A           |
| ELPM     | Rd, Z    | Extended Load Program Memory                    | Rd ← (RAMPZ:Z)                              |       | 3           | 3             | 3             | N/A           |
| ELPM     | Rd, Z+   | Extended Load Program Memory and Post-Increment | "Rd ← (RAMPZ:Z)\n(RAMPZ:Z) ← (RAMPZ:Z) + 1" |       | 3           | 3             | 3             | N/A           |
| IN       | Rd, A    | In From I/O Location                            | Rd ← I/O(A)                                 |       | 1           | 1             | 1             | 1             |
| LAC      | Z, Rd    | Load and Clear                                  | "(Z) ← ($FF – Rd) • (Z)\nRd ← (Z)"          |       | N/A         | 1             | N/A           | N/A           |
| LAS      | Z, Rd    | Load and Set                                    | "(Z) ← Rd v (Z)\nRd ← (Z)"                  |       | N/A         | 1             | N/A           | N/A           |
| LAT      | Z, Rd    | Load and Toggle                                 | "(Z) ← Rd ⊕ (Z)\nRd ← (Z)"                  |       | N/A         | 1             | N/A           | N/A           |
| LD       | Rd, X    | Load Indirect                                   | Rd ← (X)                                    |       | 2(1)        | 1(1)          | 2(1)          | 1 / 2         |
| LD       | Rd, X+   | Load Indirect and Post-Increment                | "Rd ← (X)\nX ← X + 1"                       |       | 2(1)        | 1(1)          | 2(1)          | 2 / 3         |
| LD       | Rd, -X   | Load Indirect and Pre-Decrement                 | "X ← X - 1\nRd ← (X)"                       |       | 2(1)        | 2(1)          | 2(1)          | 2 / 3         |
| LD       | Rd, Y    | Load Indirect                                   | Rd ← (Y)                                    |       | 2(1)        | 1(1)          | 2(1)          | 1 / 2         |
| LD       | Rd, Y+   | Load Indirect and Post-Increment                | "Rd ← (Y)\nY ← Y + 1"                       |       | 2(1)        | 1(1)          | 2(1)          | 2 / 3         |
| LD       | Rd, -Y   | Load Indirect and Pre-Decrement                 | "Y ← Y - 1\nRd ← (Y)"                       |       | 2(1)        | 2(1)          | 2(1)          | 2 / 3         |
| LD       | Rd, Z    | Load Indirect                                   | Rd ← (Z)                                    |       | 2(1)        | 1(1)          | 2(1)          | 1 / 2         |
| LD       | Rd, Z+   | Load Indirect and Post-Increment                | "Rd ← (Z)\nZ ← Z + 1"                       |       | 2(1)        | 1(1)          | 2(1)          | 2 / 3         |
| LD       | Rd, -Z   | Load Indirect and Pre-Decrement                 | "Z ← Z - 1\nRd ← (Z)"                       |       | 2(1)        | 2(1)          | 2(1)          | 2 / 3         |
| LDD      | Rd, Y+q  | Load Indirect with Displacement                 | Rd ← (Y + q)                                |       | 2(1)        | 2(1)          | 2(1)          | N/A           |
| LDD      | Rd, Z+q  | Load Indirect with Displacement                 | Rd ← (Z + q)                                |       | 2(1)        | 2(1)          | 2(1)          | N/A           |
| LDI      | Rd, K    | Load Immediate                                  | Rd ← K                                      |       | 1           | 1             | 1             | 1             |
| LDS      | Rd, k    | Load Direct from data space                     | Rd ← (k)                                    |       | 2(1)        | 2(1)          | 3(1)          | 2             |
| LPM      |          | Load Program Memory                             | R0 ← (Z)                                    |       | 3           | 3             | 3             | N/A           |
| LPM      | Rd, Z    | Load Program Memory                             | Rd ← (Z)                                    |       | 3           | 3             | 3             | N/A           |
| LPM      | Rd, Z+   | Load Program Memory and Post-Increment          | "Rd ← (Z)\nZ ← Z + 1"                       |       | 3           | 3             | 3             | N/A           |
| MOV      | Rd, Rr   | Copy Register                                   | Rd ← Rr                                     |       | 1           | 1             | 1             | 1             |
| MOVW     | Rd, Rr   | Copy Register Pair                              | Rd+1:Rd ← Rr+1:Rr                           |       | 1           | 1             | 1             | N/A           |
| OUT      | A, Rr    | Out To I/O Location                             | I/O(A) ← Rr                                 |       | 1           | 1             | 1             | 1             |
| POP      | Rd       | Pop Register from Stack                         | Rd ← STACK                                  |       | 2           | 2(1)          | 2             | 3(1)          |
| PUSH     | Rr       | Push Register on Stack                          | STACK ← Rr                                  |       | 2           | 1(1)          | 1             | 1(1)          |
| SPM      |          | Store Program Memory                            | (RAMPZ:Z) ← R1:R0                           |       | (4)         | (4)           | 4(3)          | N/A           |
| SPM      | Z+       | Store Program Memory and Post-Increment by 2    | "(RAMPZ:Z) ← R1:R0\nZ ← Z + 2"              |       | (4)         | (4)           | 4(3)          | N/A           |
| ST       | X, Rr    | Store Indirect                                  | (X) ← Rr                                    |       | 1(1)(2)     | 1(1)(2)       | 1(1)(2)       | 1             |
| ST       | X+, Rr   | Store Indirect and Post-Increment               | "(X) ← Rr\nX ← X + 1"                       |       | 1(1)(2)     | 1(1)(2)       | 1(1)(2)       | 1             |
| ST       | -X, Rr   | Store Indirect and Pre-Decrement                | "X ← X - 1\n(X) ← Rr"                       |       | 2(1)(2)     | 2(1)(2)       | 1(1)(2)       | 2             |
| ST       | Y, Rr    | Store Indirect                                  | (Y) ← Rr                                    |       | 2(1)(2)     | 1(1)(2)       | 1(1)(2)       | 1             |
| ST       | Y+, Rr   | Store Indirect and Post-Increment               | "(Y) ← Rr\nY ← Y + 1"                       |       | 2(1)(2)     | 1(1)(2)       | 1(1)(2)       | 1             |
| ST       | -Y, Rr   | Store Indirect and Pre-Decrement                | "Y ← Y - 1\n(Y) ← Rr"                       |       | 2(1)(2)     | 2(1)(2)       | 1(1)(2)       | 2             |
| ST       | Z, Rr    | Store Indirect                                  | (Z) ← Rr                                    |       | 2(1)(2)     | 1(1)(2)       | 1(1)(2)       | 1             |
| ST       | Z+, Rr   | Store Indirect and Post-Increment               | "(Z) ← Rr\nZ ← Z + 1"                       |       | 2(1)(2)     | 1(1)(2)       | 1(1)(2)       | 1             |
| ST       | -Z, Rr   | Store Indirect and Pre-Decrement                | "Z ← Z - 1\n(Z) ← Rr"                       |       | 2(1)(2)     | 2(1)(2)       | 1(1)(2)       | 2             |
| STD      | Y+q, Rr  | Store Indirect with Displacement                | (Y + q) ← Rr                                |       | 2(1)(2)     | 2(1)(2)       | 1(1)(2)       | N/A           |
| STD      | Z+q,Rr   | Store Indirect with Displacement                | (Z + q) ← Rr                                |       | 2(1)(2)     | 2(1)(2)       | 1(1)(2)       | N/A           |
| STS      | k, Rr    | Store Direct to Data Space                      | (k) ← Rd                                    |       | 2(1)(2)     | 2(1)(2)       | 2(1)(2)       | 1             |
| XCH      | Z, Rd    | Exchange                                        | "(Z) ← Rd\nRd ← (Z)"                        |       | N/A         | 1             | N/A           | N/A           |

## MCU Control

| Mnemonic | Operands | Description    | Operation | Flags | AVR #Clocks | AVRxm #Clocks | AVRxt #Clocks | AVRrc #Clocks |
| -------- | -------- | -------------- | --------- | ----- | ----------- | ------------- | ------------- | ------------- |
| BREAK    |          | Break          |           |       | 1           | 1             | 1             | 1             |
| NOP      |          | No Operation   |           |       | 1           | 1             | 1             | 1             |
| SLEEP    |          | Sleep          |           |       | 1           | 1             | 1             | 1             |
| WDR      |          | Watchdog Reset |           |       | 1           | 1             | 1             | 1             |

## Notes

1. Cycle time for data memory accesses assume internal RAM access, and are not valid for accesses
   through the NVM controller. A minimum of one extra cycle must be added when accessing memory
   through the NVM controller (such as Flash and EEPROM), but depending on simultaneous
   accesses by other masters or the NVM controller state, there may be more than one extra cycle.
2. One extra cycle must be added when accessing lower (64 bytes of) I/O space.
3. The instruction is not available on all devices.
4. Device dependent. See the device specific datasheet.
