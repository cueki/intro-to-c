# Common Patterns and Algorithms

## Pointer Patterns

### Basic Pointer Declaration and Usage
```c
int value = 42;
int *ptr = &value;      // Point to value
printf("%d", *ptr);     // Dereference to get 42
*ptr = 100;             // Modify value through pointer
```

### Pointer Arithmetic with Arrays
```c
int arr[5] = {10, 20, 30, 40, 50};
int *ptr = arr;         // Same as ptr = &arr[0]

// These are equivalent:
arr[2] == *(arr + 2) == *(ptr + 2) == ptr[2]

// Moving through array:
ptr++;                  // Now points to arr[1]
ptr += 2;               // Now points to arr[3]
```

### Function Parameter Passing with Pointers
```c
// Modify original variable
void increment(int *num) {
    (*num)++;           // Increment the value at address
}

// Pass array to function
void printArray(int *arr, int size) {
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);    // or *(arr + i)
    }
}
```

### Pointer to Pointer Pattern
```c
int value = 42;
int *ptr = &value;
int **ptrToPtr = &ptr;

// Accessing value through double pointer:
printf("%d", **ptrToPtr);    // Prints 42
```

### Dynamic Array Allocation Pattern
```c
int size = 10;
int *dynamicArray = malloc(sizeof(int) * size);
if (dynamicArray == NULL) {
    // Handle allocation failure
    return -1;
}

// Use the array
for (int i = 0; i < size; i++) {
    dynamicArray[i] = i * 2;
}

// Don't forget to free
free(dynamicArray);
dynamicArray = NULL;    // Good practice
```

### Pointer Arithmetic Memory Address Calculation
```c
int arr[4] = {10, 20, 30, 40};
int *ptr = arr;

// If arr starts at address 0x1000:
// ptr + 0 → 0x1000 (points to arr[0])
// ptr + 1 → 0x1004 (points to arr[1]) 
// ptr + 2 → 0x1008 (points to arr[2])
// ptr + 3 → 0x100C (points to arr[3])

// Distance between pointers:
int *ptr1 = &arr[1];
int *ptr2 = &arr[3];
int distance = ptr2 - ptr1;  // Result: 2 (not 8 bytes!)
```

### String Processing with Pointers
```c
// Count characters using pointer
int countChars(const char *str) {
    int count = 0;
    while (*str != '\0') {
        count++;
        str++;              // Move to next character
    }
    return count;
}

// Copy string using pointers
void stringCopy(char *dest, const char *src) {
    while (*src != '\0') {
        *dest = *src;
        dest++;
        src++;
    }
    *dest = '\0';           // Don't forget null terminator
}
```

## String Length Calculation

**Method 1 (while loop):**
```c
size_t count = 0;
while (*ptr != '\0') {
  ++count;
  ++ptr;
}
return count;
```

**Method 2 (for loop):**
```c
size_t count = 0;
for (; *ptr != '\0'; ++ptr, ++count);
return count;
```

## String Comparison Pattern
```c
len1 = strlen(string1);
len2 = strlen(string2);
compareLen = (len1 < len2) ? len1 : len2;
result = strncmp(string1, string2, compareLen);
```

## Dynamic Memory Allocation Pattern
```c
char* ptr = malloc(sizeof(char) * (length + 1));
if (ptr == NULL) {
  // Handle error
  return NULL;
}
// Use the memory
strcpy(ptr, source);
// Remember to free(ptr) when done
```

## Stack Implementation Pattern
```c
char* stack = malloc(strlen(input));
int stackPos = 0;

// Push: stack[stackPos++] = item;
// Pop: item = stack[--stackPos];
// Empty check: stackPos <= 0

free(stack);
```

## Boundary Checking Pattern
```c
if (position < 1) {
  position = 1;
}
if (position > MAX_POSITION) {
  position = MAX_POSITION;
}
```