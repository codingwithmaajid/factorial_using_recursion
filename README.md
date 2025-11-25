# Factorial Program in C

This repository contains a simple C program to calculate the factorial of a given number using **recursion**.

---

## 🚀 Features
- Prompts the user to enter a number.
- Uses a recursive function to compute factorial.
- Handles the base case (`0! = 1`).
- Demonstrates recursion in C programming.

---

## 📂 Code Explanation
1. **Function Declaration**  
   `int fact(int n);` declares the recursive function.

2. **Main Function**  
   - Reads input from the user.  
   - Calls the `fact()` function.  
   - Prints the result.

3. **Recursive Function**  
   - Base case: if `n == 0`, return `1`.  
   - Recursive case: `n! = n * (n-1)!`.

---

## 🖥️ Example Run

Enter a number to find the factorial of: 5
Factorial is: 120
```c
#include <stdio.h>

// Function prototype declaration
int fact(int n);

int main() {
    int n;
    // Prompt user for input
    printf("Enter a number to find the factorial of: ");
    scanf("%d", &n);

    // Display the result
    printf("Factorial is: %d\n", fact(n));
    return 0;
}

// Recursive function to calculate factorial
int fact(int n) {
    // Base case: factorial of 0 is 1
    if (n == 0) {
        return 1;
    }

    // Recursive case: n! = n * (n-1)!
    int factnm1 = fact(n - 1);   // factorial of (n-1)
    int factn   = factnm1 * n;   // multiply by n
    return factn;
}
