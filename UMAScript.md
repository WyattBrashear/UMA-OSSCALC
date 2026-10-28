# UMAScript Specification
UMAScript is a stack-based programming language designed to be easily implementable and embeddable. This specification is designed to be easily readable by the fine folks (probably you) who are interested in implementing a version of it yourself or learning how to use OSSCalc scripting on a deeper level

## The Stack Based Paradigm
UMAScript is based upon a stack of values. The stack's height is only bounded by the size of the memory region the stack occupies. A stack is a LiFo (Last in First out) data structure, meaning the most recent value to be pushed (added) to the stack will be at index 0

## UMAScript Typing
A conforming UMAScript implementation will inference variable types, these types being:
- Number
- Character
- Array
- String
- Function

### The Number Type
A piece of data of the number type in a conforming implementation will be stored as either a floating point number of any width (width of the host system recommended) or, if you're willing to get fancy: a piece of data that automatically selects the proper under the hood representation for each instance it determines to be of the number type.

### The Character Type
A piece of data of the character type in a conforming UMAScript implementation will be stored in any encoding the implementer chooses, it must store only one character. This type is denoted by a character surrounded with single quotes: ''

### The Array Type
A piece of data of the array type in a conforming UMAScript implementation will be variable width and able to store any amount of values of any type. This type is denoted by values in this format: [x, y, z, etc.]

### The String Type
A piece of data of the string type in a conforming UMAScript implementation will be internally stored as an array of characters that can be typed more easily. This type is denoted by a collection of characters surrounded with double quotes: ""

### The Function Type
A piece of data of the function type in a conforming UMAScript implementation will be a data form of executable instructions that can be stored and executed. This type is denoted by a piece of code surrounded by curly brackets: {}