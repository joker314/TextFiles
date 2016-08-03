Syntax for Potato.

Potato is a Reverse Polish Notation language. This means that the function name goes at the end, after the arguments.

The official Potato interpreter found at https://scratch.mit.edu/projects/XXX/ uses a stack to interpret te language. Here are the definitions to stack-based terminology.

	POP
		This will return and delete the last item pushed to the stack
	PUSH
		This will insert the item into the stack

Here are the built-in functions (and there JavaScript equivalents [NOTE: No return value means nothing gets PUSHed to the stack]):

+
JavaScript: `function +(arg1, arg2){return arg1 + arg2;}`
Description: POPs two values and PUSHes their sum

-
JavaScript: `function -(arg1, arg2){return arg1 - arg2;}`
Description: POPs two values and PUSHes the first minus the second

*
JavaScript: `function *(arg1, arg2){return arg1 * arg2;}`
Description: POPs two values and PUSHes their product

/
JavaScript: `function /(arg1, arg2){return arg1 / arg2;}`
Description: POPs two values and PUSHes the first divided by the second

%
JavaScript: `function %(arg1, arg2){return arg1 % arg2;}`
Description: POPs two values and PUSHes the first modulo the second

?
JavaScript: `function ?(){return prompt();}`
Description: Takes user input and PUSHes it

~
JavaScript: `function ~(arg1){console.log(arg1);}`
Description: Takes user input and PUSHes it

a
JavaScript: `function a(){return storage["a"];}`
Description: Reads variable "a". Value of "" by default.

b
JavaScript: `function b(){return storage["b"];}`
Description: Reads variable "b". Value of "" by default.

c
JavaScript: `function c(){return storage["c"];}`
Description: Reads variable "c". Value of "" by default.

d
JavaScript: `function d(){return storage["b"];}`
Description: Reads variable "d". Value of "" by default.

e
JavaScript: `function e(arg1){return storage["e"][arg1];}`
Description: Reads from array "e", index from POP.

f
JavaScript: `function f(arg1){return storage["f"][arg1];}`
Description: Reads from array "f", index from POP.

g, h, i, j, all set the variables (a-d) getting the new value as a POP
k, l all push to their lists (e, f) getting the value from the stack.
