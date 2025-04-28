# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int M, N;

    // Input the range
    printf("Enter the starting number (M): ");
    scanf("%d", &M);

    printf("Enter the ending number (N): ");
    scanf("%d", &N);

    // Check if the range is valid
    if (M > N) {
        printf("Invalid range! M should be less than or equal to N.\n");
        return 1;
    }

    printf("Even numbers from %d to %d are:\n", M, N);

    for (int i = M; i <= N; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }
    }

    printf("\n");
    return 0;
}

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/00714e1a-6016-4e76-a02e-81735ad9de0f)

## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows;

    // Ask the user for the number of rows
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    // Outer loop for each row
    for (int i = 1; i <= rows; i++) {
        // Inner loop for printing stars in each row
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        // Move to next line after each row
        printf("\n");
    }

    return 0;
}

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/3c103aa2-5b58-4dcd-a0d7-0d7f3ce9b5cb)


## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
```
#include <stdio.h>

// Function to perform addition (with arguments, no return)
void add(int a, int b) {
    int sum = a + b;
    printf("Addition: %d + %d = %d\n", a, b, sum);
}

// Function to perform subtraction (with arguments, no return)
void subtract(int a, int b) {
    int diff = a - b;
    printf("Subtraction: %d - %d = %d\n", a, b, diff);
}

int main() {
    int num1, num2;

    // Input two numbers
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Call the functions
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/84cc3d99-16ec-46c8-9ebb-2027ed5d2017)


## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int number, digit, sum = 0;

    // Input a number
    printf("Enter an integer: ");
    scanf("%d", &number);

    // Make sure the number is positive
    if (number < 0) {
        number = -number;
    }

    // Loop to extract and check each digit
    for (; number > 0; number /= 10) {
        digit = number % 10;
        if (digit % 2 != 0) {  // Check if the digit is odd
            sum += digit;
        }
    }

    // Display the result
    printf("Sum of odd digits = %d\n", sum);

    return 0;
}

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/0b3290a2-06f3-4658-ac49-ba852b75eb30)

## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
```
#include <stdio.h>

// Function to calculate the factorial
void factorial(int n) {
    long long fact = 1;

    // Check if the number is negative
    if (n < 0) {
        printf("Factorial is not defined for negative numbers.\n");
        return;
    }

    // Loop to calculate factorial
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }

    // Print the result
    printf("Factorial of %d = %lld\n", n, fact);
}

int main() {
    int num;

    // Input the number
    printf("Enter a number: ");
    scanf("%d", &num);

    // Call the factorial function
    factorial(num);

    return 0;
}

```

## OUTPUT:
![image](https://github.com/user-attachments/assets/afce0bd9-9427-4910-8861-86ae500f33bc)

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
