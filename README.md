# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM

```c
#include <stdio.h>

int main() {
    int a = 44;  // Step 2: Assign a = 44
    int b = 3;   // Step 2: Assign b = 3
    int result;

    // Step 3: Perform left shift
    result = a << b;  // Shifting 'a' to the left by 'b' positions

    // Step 4: Display the result
    printf("The result of left shifting %d by %d positions is: %d\n", a, b, result);

    return 0;
}
```

## OUTPUT
The result of left shifting 44 by 3 positions is: 352

## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT

## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM

```c
#include <stdio.h>

int main() {
    int num1, num2;

    // Step 2: Read two numbers
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Step 3: Check if the numbers are equal
    if (num1 == num2) {
        printf("Both numbers are equal.\n");
    }
    // Step 4: Otherwise, they are not equal
    else {
        printf("Both numbers are not equal.\n");
    }

    return 0;
}
```

## OUTPUT
Enter the first number: 23
Enter the second number: 23
Both numbers are equal.
           
## RESULT
Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully


# EX-18-STRING-LOWERCASE-CONVERSION

## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM

```c
#include <stdio.h>
#include <ctype.h>  // Needed for tolower()

int main() {
    char str[100];

    // Step 2: Read a string
    printf("Enter a string: ");
    scanf("%s", str);  // Reads string without spaces

    // Step 3: Convert each character to lowercase
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]);
    }

    // Step 4: Display the result
    printf("Lowercase string: %s\n", str);

    return 0;
}
```

## OUTPUT
Enter a string: RITHANYA
Lowercase string: rithanya

## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 

# EX-19-COUNT-OF-WORDS-IN-A-STRING

## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM

```c
#include <stdio.h>

int main() {
    char str[100];
    int i = 0, count = 1;  // Start count at 1 assuming the first word exists

    // Step 2: Read a string
    printf("Enter a string: ");
    scanf(" %[^\n]", str);  // Reads string including spaces until newline

    // Step 3: Inspect character by character using do-while loop
    do {
        if (str[i] == ' ' && str[i+1] != ' ' && str[i+1] != '\0') {
            count++;  // Step 4: Increment count when a space followed by a character
        }
        i++;
    } while (str[i] != '\0');  // Continue until end of string

    // Step 5: Display the result
    printf("Total number of words: %d\n", count);

    return 0;
}
```

## OUTPUT
Enter a string: Don't watch the clock; do what it does. Keep going.
Total number of words: 10

## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 
# EX  -20 -COMPARING TWO STRINGS

## AIM
write a Program to compare two strings without using strcmp().

## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM

```c
#include <stdio.h>

int main() {
    char c1[100], c2[100];
    int i = 0, flag = 0;

    // Step 3: Read the first string (including spaces)
    printf("Enter the first string: ");
    scanf(" %[^\n]", c1);

    // Step 4: Read the second string (no spaces)
    printf("Enter the second string: ");
    scanf("%s", c2);

    // Step 5 and Step 6: Compare characters one by one
    while (c1[i] != '\0' && c2[i] != '\0') {
        if (c1[i] != c2[i]) {
            flag = 1;  // Mismatch found
            break;
        }
        i++;
    }

    // Check if both strings ended together
    if (c1[i] != '\0' || c2[i] != '\0') {
        flag = 1;  // One string is longer than the other
    }

    // Step 7: Display the result
    if (flag == 0) {
        printf("Strings are same.\n");
    } else {
        printf("Strings are not same.\n");
    }

    return 0;
}
```

## OUTPUT
Enter the first string: Jasmine
Enter the second string: Jasmine
Strings are same. 

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.
