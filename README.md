# Comp-Theory
## Overview

This repository contains Python implementations of various bit manipulation and hashing functions, as well as explanations for each task.</br>

## Tasks

### Task 1: Binary Representations

This task involves creating Python functions to manipulate binary representations of numbers. The following functions are implemented:</br>

1. rotl(x, n=1): Rotates the bits in a 32-bit unsigned integer to the left by `n` places.
    - Example: ``rotl(0b10101010101010101010101010101010, 3)  -> 0b1010101010101010101010101010101``
2. rotr(x, n=1): Rotates the bits in a 32-bit unsigned integer to the right by `n` places.
    - Example: ```rotr(0b10101010101010101010101010101010, 3)  -> 0b1010101010101010101010101010101```
3. ch(x, y, z): Chooses the bits from `y` where `x` has bits set to 1, and bits from `z` where `x` has bits set to 0.
    - Example: ```ch(0b10101010101010101010101010101010, 0b11001100110011001100110011001100, 0b11110000111100001111000011110000) -> 0b11011000110110001101100011011000```
4. maj(x, y, z): Performs a majority vote of bits in `x, y, and z`. The output has a 1 in each bit position where at least two of the inputs have 1s.
    - Example: ```maj(0b10101010101010101010101010101010, 0b11001100110011001100110011001100, 0b11110000111100001111000011110000) -> 0b11101000111010001110100011101000```

### Task 2: Hash Functions

This task involves converting a C-based hash function into Python and analyzing its characteristics.</br>

- hash_function(s): Implements the following hash function in Python:
```
unsigned hash(char *s) {
    unsigned hashval;
    for (hashval = 0; *s != '\0'; s++)
        hashval = *s + 31 * hashval;
    return hashval % 101;
}
```
- The function is tested for correctness, and an explanation is provided on why the values 31 and 101 are used in the hashing process.</br>

## Usage

To run the functions, simply execute the Python script containing the code. Ensure Python 3 is installed on your system.</br>

## Requirements
- Python 3.x
- No external libraries required