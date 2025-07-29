# Common Patterns and Algorithms

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