# Comp-Theory-Tasks
## Overview

This repository contains Python implementations of various bit manipulation and hashing functions, as well as explanations for each task.</br>

## Tasks

### Task 1: Binary Representations

This task involves creating Python functions to manipulate binary representations of numbers. The following functions are implemented:</br>

#### Implemented Functions:

1. **rotl(x, n=1):** Rotates the bits in a 32-bit unsigned integer to the left by `n` places.
    - Shifting 1010 left by 2 gives 1000, but the overflowed bits return, so the result is 1010.
    - Example: ``rotl(0b10101010101010101010101010101010, 3)  -> 0b1010101010101010101010101010101``
2. **rotr(x, n=1):** Rotates the bits in a 32-bit unsigned integer to the right by `n` places.
    - Example: 1010 shifted right by 2 results in 1010 again.
    - Example: ```rotr(0b10101010101010101010101010101010, 3)  -> 0b1010101010101010101010101010101```
3. **ch(x, y, z):** Chooses the bits from `y` where `x` has bits set to 1, and bits from `z` where `x` has bits set to 0.
    - Example: ```ch(0b10101010101010101010101010101010, 0b11001100110011001100110011001100, 0b11110000111100001111000011110000) -> 0b11011000110110001101100011011000```
4. **maj(x, y, z):** Performs a majority vote of bits in `x, y, and z`. The output has a 1 in each bit position where at least two of the inputs have 1s.
    - Example: ```maj(0b10101010101010101010101010101010, 0b11001100110011001100110011001100, 0b11110000111100001111000011110000) -> 0b11101000111010001110100011101000```

### Task 2: Hash Functions

This task involves converting a C-based hash function into Python and analyzing its characteristics.</br>

#### Implemented Function:

- **kr_hash(s):** Implements a simple hash function using modular arithmetic.

#### Results:

```
unsigned hash(char *s) {
    unsigned hashval;
    for (hashval = 0; *s != '\0'; s++)
        hashval = *s + 31 * hashval;
    return hashval % 101;
}
```

#### Explanation:

- The hash function works by multiplying each character’s ASCII value by 31 and taking the result modulo 101. This ensures a uniform spread of hash values.</br>

### Task 3: String Manipulation

This task focuses on operations related to strings.</br>

#### Implemented Functions:

- **reverse_string(s):** Flips a string backward. 
    - Example: `"hello"` becomes `"olleh"`.
- **is_palindrome(s):** Checks if a word reads the same forward and backward. 
    - Example: `"racecar"` returns `True`.

### Task 4: Prime Number Verification

This task checks if numbers are prime and finds the next prime.</br>

#### Implemented Functions:

- **is_prime(n):** Checks if `n` is divisible only by 1 and itself.
- **next_prime(n):** Finds the smallest prime number greater than `n`.

#### Results:
``First 10 primes found: [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]``

### Task 5: Sorting Algorithms

Sorting arranges numbers in order from smallest to largest.</br>

#### Implemented Functions:

- **bubble_sort(arr):** Repeatedly swaps adjacent numbers if they are in the wrong order.
- **quick_sort(arr):** Selects a pivot, moves smaller numbers to one side and larger numbers to the other, then repeats.


## Usage

To run the functions, simply execute the Python script containing the code. Ensure Python 3 is installed on your system.</br>

## Requirements
- Python 3.x
- No external libraries required