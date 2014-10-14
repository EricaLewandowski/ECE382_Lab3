ECE382_Lab3
===========

#PreLab 

|Name	| Pin #	| Type | PxDIR	| PxREN	| PxOUT |
|-----|-------|------|--------|-------|-------|
| GND	|  20	  |POWER |	 X    |   X   |  	X   |
| RST	|   8	  |OUTPUT|	 1    |   0   |  	1   |
|P1.4 |   6	  |OUTPUT|	 1    |   0   |  	1   |
| MOSI|  15	  |OUTPUT|	 1    |   0   |  	1   |
| SCLK|  7	  |OUTPUT|	 1    |   0   |  	1   |
| VCC |  1	  |POWER |	 X    |   X   |  	X   |
| S1	|  9	  |INPUT |	 0    |   0   |  	1   |
| S2	|  10	  |INPUT |	 0    |   0   |  	1   |
| S3	|  11	  |INPUT |	 0    |   0   |  	1   |
| S4	|  12	  |INPUT |	 0    |   0   |  	1   |

| Mystery Label | Register |
|---------------|----------|
|      A        |  P1DIR   |
|      B        |  P1OUT   |
|      C        |  P2DIR   |
|      D        |  P2OUT   |

| ID     | Bit | Function                                                 |
|--------|-----|----------------------------------------------------------|
|UCCKPH  |  7  | Clock phase select                                       | 
|UCMSB   |  3  | Controls the directions of the TX and RX shift registers | 
|UCMST   |  3  | Master mode select                                       | 
|UCSYNCH |  0  | Synchronous mode enabled                                 | 
|UCSSEL_2| 7-6 | Select SMCLK as the source clock in master mode          | 
|UCSWRST |  0  | Software RESET enabled                                   | 

| Symbolic Constant | Hex | Function |
|-------------------|-----|----------|
| #STE2007_RESET    |0xE2 | Internal reset |
| #STE2007_DISPLAYALLPOINTSOFF | 0xA4 | LCD display, normal display |
| #STE2007_POWERCONTROL |      | Sets the power supply function on the chip |
| #STE2007_POWERCTRL_ALL_ON | 0X2F | Voltage regulator, booster |
| #STE2007_DISPLAYNORMAL | 0XA6 | LCD display, normal |
| #STE2007_DISPLAYON | 0XA7 | Display turned on |


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
