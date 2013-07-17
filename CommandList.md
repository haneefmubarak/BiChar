Command List
============

Bichar was mainly inspired by C and BrainFuck. However, as you may have noticed, BiChar doesn't really seem to have been influenced by any language. As such, the main similarities to the above languages is shown below:

 - `++` increments the current binary value at the byte at the pointer			(Similar to C and BF)
 - `--` decrements the current binary value at the byte at the pointer			(Similar to C and BF)
 - `..` outputs the current binary value at the byte at the pointer				(Similar to BF)
 - `,,` inputs a new binary value at the byte at the pointer					(Similar to BF)
 - `>>` increments the current binary value of the pointer						(Similar to BF)
 - `<<` decrements the current binary value of the pointer						(Similar to BF)
 - `{{` if binary value at pointer == 0, jump --> to matching }}; else skip		(Similar to BF)
 - `}}` if binary value at pointer != 0, jump <-- to matching {{; else skip		(Similar to BF)
 
One thing you may have noticed is that the above commands seem to be the doubles of the equivalent BrainFuck commands. This is intentional, because in this way, any BrainFuck program can easily be ported to BiChar and then extended.

List of Terms
=============

 - `[val/add]`		Input a value (hex: `"'xxxx'"`; octal: `'"xxxxxx"'`; dec: `''0xxxxx''`; char: `""xx""`) or an address (address in hex: `[[xxxx]]`; address of pointer to address in hex: `[]xxxx[]` (note: pointers cannot currently be nested))



Full List
===================

|Type		|Command		|Syntax												|Function						|
|-----------|---------------|---------------------------------------------------|-------------------------------|
|Arithmetic	|`++`			|`++`												|Increment current byte			|
|Arithmetic |`+=`			|`+= [val/add]										|Add value to current byte		|
|Arithmetic	|`+x`			|`+x [val/add var] [val/add store]`					|Add value of current byte and byte var to byte store|
