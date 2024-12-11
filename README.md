# Undefined Behavior in C: Order of Evaluation in printf
This repository demonstrates a common, yet subtle, source of undefined behavior in C: the order of evaluation of side effects within a function call, specifically `printf`. 

## The Bug
The `bug.c` file contains a simple program that increments a variable `x` and prints its value twice using `printf`.  Due to the undefined behavior, the output might vary between different compilers or even different runs of the same compiler. 

## The Solution
The `bugSolution.c` file provides a corrected version that explicitly separates the increment and the print operations. This removes the ambiguity and produces a consistent output. 

## How to Compile and Run

1.  Save the code in `bug.c` and `bugSolution.c`.
2. Compile using a C compiler (like GCC):
   ```bash
gcc bug.c -o bug
gcc bugSolution.c -o bugSolution
```
3. Run the executables:
   ```bash
./bug
./bugSolution
```

Observe the output of each. The solution will always have a consistent and predictable output.