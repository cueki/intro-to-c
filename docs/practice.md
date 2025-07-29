# Practice Problems Overview

## Pointer Arithmetic Predictions
- Calculate memory addresses manually
- Understand 4-byte integer spacing
- Predict pointer increment/decrement results
- Function parameter passing effects

## Tortoise and Hare Race Simulation
- Random number generation with `srand()` and `rand()`
- Switch statements for movement logic:
  - **Tortoise:** Cases 1-5: FAST_PLOD (+3), Cases 6-7: SLIP (-6), Cases 8-10: SLOW_PLOD (+1)
  - **Hare:** Cases 1-2: SLEEP (0), Case 3-4: BIG_HOP (+9), Case 5: BIG_SLIP (-12), Cases 6-8: SMALL_HOP (+1), Cases 9-10: SMALL_SLIP (-2)
- Boundary checking and race conditions
- Position tracking and winner determination

## String Function Implementations
- Complete missing string functions using both array and pointer methods
- Proper null terminator handling
- Return pointer to modified string

## Memory Management Exercises
- Dynamic string allocation (`get_string` function)
- Proper `malloc`/`free` usage
- Error checking for allocation failures

## Bracket Validation
- Stack-based matching algorithm
- Handling multiple bracket types: `()`, `{}`, `[]`
- Proper memory cleanup on all exit paths

## Array Intersection
- Counting sort algorithm implementation
- O(n) vs O(n²) complexity considerations
- Memory vs speed optimization tradeoffs