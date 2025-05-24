# EX-NO-6-Pseudo-Random-Number

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:
Start the program and import the required libraries.
Seed the random number generator using the current time(i.e) rand(time(0));
Get the number of randon number to generate.
Pass the value for number of iterations and print the numbers.
End the program.

# PROGRAM:
```
Name: Markandeyan Gokul
Reg No: 212224240086
```

```
#include <stdio.h>

#define A 1664525
#define C 1013904223

unsigned int lcg(unsigned int seed) {
    return A * seed + C; // No need for % 2^32; it wraps around naturally
}

int main() {
    unsigned int seed;
    int n;

    printf("Enter the seed value: ");
    scanf("%u", &seed);
    
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);

    printf("Random numbers:\n");
    for (int i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }

    return 0;
}
```
# OUTPUT:
![image](https://github.com/user-attachments/assets/764ceef5-41cb-44d6-b8df-383b216e9c01)

# RESULT:
The Program is implemented successfully.
