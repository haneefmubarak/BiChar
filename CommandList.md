Command List
============

Bichar was mainly inspired by C and BrainFuck (and a few others). However, as you may have noticed, BiChar doesn't really seem to have been influenced by any language. As such, the main similarities to the above languages is shown below:

 - `++` increments the current binary value at the bvar at the pointer			(Similar to C and BF)
 - `--` decrements the current binary value at the bvar at the pointer			(Similar to C and BF)
 - `**` raises the the current binary value at the bvar at the pointer			(Similar to FORTRAN)
 - `..` outputs the current binary value at the bvar at the pointer				(Similar to BF)
 - `,,` inputs a new binary value at the bvar at the pointer					(Similar to BF)
 - `>>` increments the current binary value of the pointer						(Similar to BF)
 - `<<` decrements the current binary value of the pointer						(Similar to BF)
 - `{{` if binary value at pointer == 0, jump --> to matching }}; else skip		(Similar to BF)
 - `}}` if binary value at pointer != 0, jump <-- to matching {{; else skip		(Similar to BF)
 
One thing you may have noticed is that some of the above commands seem to be the doubles of the equivalent BrainFuck commands. This is intentional, because in this way, any BrainFuck program can easily be ported to BiChar and then extended.

List of Terms
=============

|Term|Meaning|
|---|---|
|`[val/add]`	|	Input a value (hex: `"'xxxx'"`; octal: `'"xxxxxx"'`; dec: `''0xxxxx''`; char: `""xx""`) or an address (address in hex: `[[xxxx]]`; address of pointer to address in hex: `[]xxxx[]` (note: pointers cannot currently be nested))|
|`curbvar`		| 	The current bvar (ie: the bvar at the pointer)|



Full List
===================

Arithmetic
----------

|Command	|Syntax												|Function						|Equivalence		|
|-----------|---------------------------------------------------|-------------------------------|-------------------|
|`++`		|`++`												|Increment curbvar			|`x = x + 1`			|
|`+=`		|`+= [val/add]`										|Add value of variable to curbvar		|`x = x + var`		|
|`+x`		|`+x [val/add var] [val/add stor]`					|Place sum of curbvar and bvar var in bvar stor|`stor = x + var`|
|`--`		|`--`												|Decrement curbvar			|`x = x - 1`|
|`-=`		|`-= [val/add]`										|Subtract value of variable from curbvar		|`x = x - 1`
|`-x`		|`-x [val/add var] [val/add stor]`					|Place non-absolute difference from curbvar to bvar var in bvar stor|`stor = x - var`|
|`**`		|`** [val/add]`										|Raise curbvar to exponent			|`x = x ^ var`|
|`*=`		|`*= [val/add]`										|Replace bvar with product of curbvar and variable		|`x = x * var`|
|`*x`		|`*x [val/add var] [val/add stor]`					|Place product of curbvar and and bvar var in bvar stor|`stor = x * var`|


