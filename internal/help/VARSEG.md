The **VARSEG** function returns an [INTEGER](INTEGER) value that is the segment part of a variable or array memory address. 

## Syntax

> [DEF SEG](DEF-SEG) = VARSEG(variable_name[(start_index)])

* If variablename is not defined before [VARPTR](VARPTR) or VARSEG is called, the variable is created and its address is returned.
* The start index is the lowest index of an array variable when used. 
* When a string variable, VARSEG returns the segment location address of the first byte of the string.
* Because many QBasic statements change the locations of variables in memory, use the values returned by VARPTR and VARSEG immediately after the functions are used!
* Integer array sizes are limited to 32767 elements when using [VARSEG](VARSEG) in QB and **QB64**!. Create a larger array using [_BYTE](_BYTE). Example: [DIM](DIM) [SHARED](SHARED) Memory (65535) AS [_UNSIGNED](_UNSIGNED) [_BYTE](_BYTE)
* **Warning: DEF SEG, VARSEG , VARPTR, PEEK or POKE access QB64's emulated 16 bit conventional memory block!** 
> **It is highly recommended that QB64's [_MEM](_MEM) memory system be used to avoid running out of memory.**

## See Also

* [BSAVE](BSAVE), [BLOAD](BLOAD) 
* [SADD](SADD), [DEF SEG](DEF-SEG)
* [VARPTR](VARPTR), [VARPTR$](VARPTR$) 
* [POKE](POKE), [PEEK](PEEK)