# EX-NO-6-Pseudo-Random-Number

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:

STEP-1: Start the program and include the required header files.

STEP-2: Define the constants required for the Linear Congruential Generator (LCG).

STEP-3: Create a function to generate pseudorandom numbers using the formula: Xn + 1​ = (A × Xn ​+ C) mod M

STEP-4: Declare the required variables such as seed value, number of random numbers, and loop counter.

STEP-5: Seed the random number generator using the current time with srand(time(0));.

STEP-6: Read the seed value from the user.

STEP-7: Read the number of random numbers to generate.

STEP-8: Pass the seed value to the LCG function repeatedly using a loop.

STEP-9: Generate and print the pseudorandom numbers one by one.

STEP-10: End the program.

# PROGRAM:

```
#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296

unsigned int lcg(unsigned int seed)
{
    return (A * seed + C) % M;
}

int main()
{
    unsigned int seed;
    int n, i;
    printf("Pseudo Random Number Generator\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("\nEnter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("\nGenerated Random Numbers:\n\n");
    for (i = 0; i < n; i++)
    {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```

# OUTPUT:

<img width="1913" height="932" alt="ex6op" src="https://github.com/user-attachments/assets/c39d0f1d-6e8b-407e-a01b-b5195ac6565c" />

# RESULT:
Thus, the implementation of Pseudo Random Number Generation had been executed successfully.
