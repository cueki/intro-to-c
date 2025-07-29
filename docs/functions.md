# Standard Library Functions

## Input/Output Functions (`stdio.h`)

**`printf(format, ...)`** - Formatted output to stdout

  - Format specifiers: `%d` (int), `%p` (pointer), `%s` (string), `%zu` (size_t)
  
**`scanf(format, ...)`** - Formatted input from stdin

  - `scanf("%s", string)` - read string
  - `scanf("%80[^\n]", buffer)` - read up to 80 chars, stop at newline
  
**`puts(string)`** - Output string + newline to stdout

**`getchar()`** - Read single character from stdin

## Memory Management Functions (`stdlib.h`)

**`malloc(size_t size)`** - Allocate dynamic memory

  - Returns `void*` pointer or `NULL` if failed
  - Example: `char* ptr = malloc(sizeof(char) * (len + 1))`
  
**`free(void* ptr)`** - Deallocate dynamic memory

  - Must pair with every `malloc()`
  
**`srand(unsigned int seed)`** - Seed random number generator

  - Common: `srand((unsigned int)time(NULL))`
  
**`rand()`** - Generate random integer 0 to RAND_MAX

  - `rand() % 10 + 1` gives range 1-10
  
**`system(command)`** - Execute system command

  - `system("pause")` - Use `getchar()` instead

## String Functions (`string.h`)

**`strlen(const char* str)`** - Get string length (excluding `\0`)

  - Returns `size_t`
  
**`strcpy(char* dest, const char* src)`** - Copy entire string

  - Includes `\0` terminator
  
**`strncmp(const char* s1, const char* s2, size_t n)`** - Compare n characters

  - Returns: `<0` (s1<s2), `0` (equal), `>0` (s1>s2)

## Character Classification Functions (`ctype.h`)

- **`isdigit(c)`** - Check if character is digit (0-9)
- **`isalpha(c)`** - Check if character is alphabetic (a-z, A-Z)
- **`isalnum(c)`** - Check if character is alphanumeric
- **`isxdigit(c)`** - Check if character is hexadecimal digit
- **`islower(c)`** - Check if character is lowercase
- **`isupper(c)`** - Check if character is uppercase
- **`isspace(c)`** - Check if character is whitespace
- **`iscntrl(c)`** - Check if character is control character
- **`ispunct(c)`** - Check if character is punctuation
- **`isprint(c)`** - Check if character is printable
- **`isgraph(c)`** - Check if character is graphic (printable, not space)

## Character Conversion Functions (`ctype.h`)

- **`tolower(c)`** - Convert character to lowercase
- **`toupper(c)`** - Convert character to uppercase

## Time Functions (`time.h`)

**`time(time_t* timer)`** - Get current time

  - Used for seeding: `time(NULL)`
