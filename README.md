# Comp-Theory
## Overview

This repository contains Python implementations of various bit manipulation and hashing functions, as well as explanations for each task.</br>

## Tasks

### Task 1: Binary Representations

This task involves creating Python functions to manipulate binary representations of numbers. The following functions are implemented:</br>

1. rotl(x, n=1): Rotates the bits in a 32-bit unsigned integer to the left by n places.
2. rotr(x, n=1): Rotates the bits in a 32-bit unsigned integer to the right by n places.
3. ch(x, y, z): Chooses the bits from y where x has bits set to 1, and bits from z where x has bits set to 0.
4. maj(x, y, z): Performs a majority vote of bits in x, y, and z. The output has a 1 in each bit position where at least two of the inputs have 1s.

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