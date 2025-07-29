# Core Programming Concepts

## Functions
- Function prototypes and definitions
- Parameter passing by value vs by reference
- Return values and types
- Simple mult function: `int square(int number) { return number * number; }`

## Pointers
**Critical concepts:**
- Pointer declaration: `int *ptr`

- Address-of operator: `&variable`

- Dereference operator: `*ptr`

- Pointer arithmetic: `ptr+1`, `ptr++`, `ptr--`

- Array-pointer relationship: `myArray ≡ &myArray[0]`

- Pointer to pointer: `int **ptrToPtr`

- Function parameter passing with pointers

**Key relationships:**

- `arr[i] ≡ *(arr+i)`

- `&arr[i] ≡ arr+i`

- Arrays passed to functions become pointers

## Arrays and Strings
- Arrays as function parameters (passed as pointers)
- Pointer arithmetic with arrays
- Boundary checking and memory management
- Null terminator (`\0`) handling in strings
- String indexing vs pointer notation

## Dynamic Memory Allocation
- `malloc()` and `free()`
- **Error checking for allocation failures** (Don't forget...)

Dynamic string allocation based on input length is a good usecase for this.

## Stack Data Structure
- Using arrays to implement stack behavior
- Push operation: `stack[stackPos++] = value`
- Pop operation: `value = stack[--stackPos]`
- Stack empty check: `stackPos <= 0`

## Key Topics by Class

### Class 08 - Functions
- Basic function structure and prototypes
- Function calls and return values
- Parameter passing mechanisms

### Class 09 - Pointers
- Memory addresses and pointer arithmetic
- Predicting memory addresses and values
- Array-pointer relationships
- Function parameter passing with pointers
- Understanding output from pointer exercises

### Class 10 - Character Handling & String Processing
- Character classification functions (`ctype.h`)
- String length calculations (manual vs `strlen`)
- Advanced string comparison logic
- Character conversion functions

### Class 11 - String Manipulation
**Functions to implement:**

- `stringCopy1/2()` - copying strings with arrays vs pointers

- `stringNCopy1/2()` - copying n characters

- `stringCat1/2()` - string concatenation  

- `stringNCat1/2()` - concatenating n characters

- String comparison using `strncmp()` with shortest length
