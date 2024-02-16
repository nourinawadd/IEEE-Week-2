# IEEE-Week-2
Summary of an [introductory video](https://www.youtube.com/watch?v=bCSeXFRBhLg&t=5s) on Embedded Systems

### Computing systems consists of 3 main components:
- Processor
- Memory
- I/O devices

These 3 components communicate through the system buses (data, address, control).

## Languages of MicroProcessors (MP)
1. Machine language (binary - 0’s and 1’s)
   
     -  For the instruction decoder to understand the instruction, it needs to know its set and format.
     -  AKA, first 3 numbers is the OPCode, next 3 is OP1, etc.
     -  For the OPCode to be understood, the ID needs to refer to the instruction set, which contains the OPCode and name of each operation

3. Assembly Language
    - Assembler translates assembly language to machine language
    - However, there are 4 problems that appear:
      
      1. OPCode depends on the MP.
      2. Assembly instructions vary from one machine to the other.
      3. Some MP don’t understand complex operations (like multiplication)
      4. Difficult process to deal with assembly language.

   - Advantages of assembly language:
     1. Optimized size & execution time
     2. No need for compiler, just the assembler.

All the problems that appeared in the assembly language were solved by programming languages.

## Programming Languages
### History:
1. **1960** - ALGOL is the first prog. language & appeared in Europe.
2. **1967** - BCPL (Basic Combined Programming Language) made by Martin Richards
3. **1970** - B language made by Ken Thompson (BCPL + some features). Based on Unix operating systems (disadvantage) & done at AT&T and Bell labs
4. **1972** - C made by Dennis Ritchie at Bell labs (ALGOL + BCPL + B + some features). Also based on Unix OS. Many compilers were then released for cross-platforms, which made it compatible with Windows, Linux.

After this, many languages were made out of C + some features. So, to bring back some standardization in the programming languages, ANSI created the C89 Standard Language in 1989.

It was proposed to the ISO to make this the standard language, and this got approved in 1990 - called **ANSI C** or **C89**.


### Applications of C Language:
- Operating Systems
- Desktop Applications
- Adobe Applications
- Browsers
- Compilers
- Embedded Systems

### Why do we use C & not assembly languages?
1. C is easier, simpler & faster to develop
2. Portable (regarding cross-platform)

### Why do we use C in embedded systems (as opposed to other languages)?
1. Memory allocation
   - Directly addresses memory, which also accesses registers
   - High-level languages like Java cannot access memory and give absolute addresses to the bus like C.
2. Layout

## Building/ Compilation Process
- A “.c” file is compiled into a “.exe” (executable) file through the tool chain.
- The tool chain used is the GNU C Compiler (GCC) which is free & open-source.

### Tool Chain
1. Native Tool Chain
   - Runs on the same architecture of microprocessor.
   - Compiles into an executable file.

2. Cross Tool Chain
   - Runs on different architectures of microprocessors.
   - Compiles it into a binary file.

Brief explanation of how a tool chain works
- A source file (.c) goes through a preprocessor, where text replacement occurs (including libraries, expanding macros, etc.) and returns a (.i) file.
- This file goes into the compiler and returns a (.s) file.
- Then the (.s) file goes through the assembler and returns an object (.o) file.
- Finally, the object file goes through the linker along with the linker script and static libraries and returns the executable (.exe) file.





