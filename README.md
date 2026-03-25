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
```
#include <stdio.h>

int main() {
    int a = 44;
    int b = 3;
    int result;

    result = a << b;
    printf("Original value: %d\n", a);
    printf("Number of shifts: %d\n", b);
    printf("Result after left shift: %d\n", result);

    return 0;
}
```
## OUTPUT



<img width="1153" height="308" alt="image" src="https://github.com/user-attachments/assets/140581be-86a7-43b1-a18e-1b2f03b49fff" />






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
```
#include <stdio.h>

int main() {
    int num1, num2;
    printf("Enter the first number: ");
    scanf("%d", &num1);
    printf("Enter the second number: ");
    scanf("%d", &num2);

    if (num1 == num2) {
        printf("Both numbers are equal.\n");
    } 
    else {
        printf("Both numbers are not equal.\n");
    }
    return 0;
}
```

## OUTPUT
     <img width="1124" height="425" alt="image" src="https://github.com/user-attachments/assets/3bc76cc8-2b15-49c2-9b3c-4b538c9162e5" />
      
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
```
#include <stdio.h>
#include <ctype.h>  // Required for tolower()

int main() {
    char str[100];
    int i = 0;
    printf("Enter a string in UPPERCASE or Mixed Case: ");
    scanf("%s", str);
    while (str[i] != '\0') {
        str[i] = tolower(str[i]);
        i++;
    }
    printf("String in lowercase: %s\n", str);
    return 0;
}
```
## OUTPUT
<img width="1302" height="345" alt="image" src="https://github.com/user-attachments/assets/0a880f0a-c72c-4e64-be93-48c165c58cc7" />




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
```
#include <stdio.h>

int main() {
    char str[200];
    int i = 0, words = 1;
    printf("Enter a sentence: ");
    scanf("%[^\n]", str);
    do {
        if (str[i] == ' ') {
            words++;
        }
        i++;
    } while (str[i] != '\0'); // 6. Stop when we reach the end of the string
    if (str[0] == '\0') {
        words = 0;
    }

    printf("Total number of words: %d\n", words);

    return 0;
}
```
## OUTPUT


<img width="1171" height="459" alt="image" src="https://github.com/user-attachments/assets/e341314d-1226-4508-b382-a87d5b050932" />



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
```
#include <stdio.h>

int main() {
    char c1[100], c2[100];
    int flag = 0;
    int i = 0;

    printf("Enter the first string: ");
    scanf("%[^\n]", c1);

    printf("Enter the second string: ");
    scanf("%s", c2);

    while (c1[i] != '\0' && c2[i] != '\0') {
        if (c1[i] != c2[i]) {
            flag = 1;
            break; // Optimization: stop as soon as a difference is found
        }
        i++;
    }

    if (c1[i] != '\0' || c2[i] != '\0') {
        flag = 1;
    }

    if (flag == 0) {
        printf("\nStrings are same.\n");
    } else {
        printf("\nStrings are not same.\n");
    }
    return 0;
}
```

## OUTPUT
 <img width="1320" height="732" alt="image" src="https://github.com/user-attachments/assets/c8b5ade6-a773-4e95-8565-a74420bf52e3" />


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

