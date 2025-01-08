# Samsung RISC-V Talent Development Program Task 1

## Overview
This repository contains my submission for Task 1 of the Samsung RISC-V Talent Development Program.
The goal was to set up a RISC-V development environment, perform basic lab exercises using both C and 
RISC-V assembly, and document the process.

## Objectives
1. Install and set up the RISC-V toolchain.
2. Perform and validate lab exercises using:
   - **C Compiler (GCC)**
   - **RISC-V Toolchain (riscv64-unknown-elf-gcc)**
3. Capture and upload output snapshots with timestamps.
4. Ensure proper documentation for each step.
   


## Directory Structure
# Samsung RISC-V Internship Task 1

This repository contains the solution to Task 1 of the RISC-V Talent Development Program.

## Code Files

```c
// sumiton.c - C program for summing numbers from 1 to 10
#include <stdio.h>
int main() {
    int sum = 0;
    for (int i = 1; i <= 10; i++) {
        sum += i;
    }
    printf("Sum = %d\n", sum);
    return 0;
}
 ``` 



---
## Steps to Reproduce
1. **Environment Setup**
   - Followed the steps in the provided lab video to set up the RISC-V development environment.
   - Installed the required dependencies using the provided VDI.
   - Verified successful installation of the toolchain using:
     ```bash
     riscv64-unknown-elf-gcc --version
     ```

2. **C Lab Exercise**
   - Wrote a simple C program (`sumiton.c`) to compute the sum of numbers from 1 to 10.
   - Compiled and executed the program using GCC:
     ```bash
     gcc sumiton.c -o sumiton
     ./sumiton
     ```

3. **RISC-V Lab Exercise**
   - Compiled the same program using the RISC-V toolchain:
     ```bash
     riscv64-unknown-elf-gcc -O1 -march=rv64i -o sumiton.o sumiton.c
     ```
   - Captured and uploaded the RISC-V assembly output.

## Results
1. **C Program Execution**
   - Below is the snapshot of the C program execution:
![Screenshot 2025-01-06 235010](https://github.com/user-attachments/assets/f44e915b-a3c0-40f6-b81b-11a04904f2f8)

    

2. **RISC-V Assembly Output**
   - The following snapshot shows the compiled RISC-V assembly output:
 ![Screenshot 2025-01-06 235341](https://github.com/user-attachments/assets/0f0a7557-7444-41a9-9b76-2524774ffd38)


## Challenges Faced
1. **Toolchain Setup Issues**  
   Faced issues while setting up the virtual machine due to low system performance.  
   **Solution:** Increased VM resources (memory and CPU) to improve performance.

2. **Compilation Errors**  
   Encountered errors while compiling RISC-V programs due to missing dependencies.  
   **Solution:** Installed all required dependencies as suggested in the lab video.

## Conclusion
Completing this task provided valuable experience in setting up a RISC-V development environment 
and performing basic lab exercises. The hands-on approach enhanced my understanding of RISC-V architecture and toolchain usage.
