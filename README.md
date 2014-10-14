ECE382_Lab3
===========

#Logic Analyzer Data
Table 1

| Line |  R12  |  R13   | Purpose                              |
|------|-------|--------|--------------------------------------|
|  66  | 0x001 | 0x00E7 | R12 is the column and R13 is the row |
|  276 | 0x000 | 0x00B0 | R12 is the column and R13 is the row |
|  288 | 0x000 | 0x0010 | R12 is the column and R13 is the row |
|  294 | 0x000 | 0x0000 | R12 is the column and R13 is the row |

Table 2

| Line |  Command/Data  | 8 bit packet   |
|------|----------------|----------------|
|  66  |      Data      |    0x00E7      |
|  276 |      Command   |    0x00B0      |
|  288 |      Command   |    0x0010      |
|  294 |      Command   |    0x0000      |

Logic Analyzer Graphic

RESET Graphic & Data

If you set r12 to 0xFFFF then there are 65535 (in decimal) loops. Reset time equals 7.085 nanoseconds which means that each iteration is 1.08 picoseconds. 

Writing Modes Graphic
