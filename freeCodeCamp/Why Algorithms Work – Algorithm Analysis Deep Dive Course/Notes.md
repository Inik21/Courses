# Why Algorithms Work – Algorithm Analysis Deep Dive Course

These notes are based on the freeCodeCamp [Why Algorithms Work – Algorithm Analysis Deep Dive Course](https://www.youtube.com/watch?v=ku6HZ_k9qgY&ab_channel=freeCodeCamp.org)

## Introduction to Time Complexity

### Notions

Definition of an Algorithm - a well-defined, finite procedure that takes an input and produces an output; an effective method to solve problems

We will use the RAM (Random Access Machine) Model to analyze the efficiency of algorithms:
- A theoretical framework to analyze the time complexity of algorithms
- The computer has an infinite amount of memory
- Each memory access takes a constant amount of time, regardless of the memory location
- Basic arithmetic operations, logic operations, and comparisons take constant time
- Executing a single instruction, such as assignment, branching, or looping, takes constant time

:exclamation: The Time Complexity of an algorithm is determined by counting the number of basic operations it performs :exclamation:

Depending on the input, some algorithms may perform better or worse, which raises different cases for the time complexity:
- Best case - the minimum number of steps that the algorithm could take
- Worst case - the maximum number of steps that the algorithm could take
- Average case - average of the running time of all possible inputs

In most cases, for different steps that take constant time, CN is used as a constant for the n-th step

### Insertion Sort



