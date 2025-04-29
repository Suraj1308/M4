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
           #include <stdio.h>
           
           int main() 
           {
               int num = 44;
               int shifts = 3;
               int result;
           
               result = num << shifts;
           
               printf("Original number: %d\n", num);
               printf("After left shifting by %d positions: %d\n", shifts, result);
           
               return 0;
           }
        

## OUTPUT
 ![image](https://github.com/user-attachments/assets/3ad4f563-39c2-41d0-823e-bf6409ed5faa)








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
      #include <stdio.h>
      
      int main() {
      
          int num1, num2;
      
      
          printf("Enter first number: ");
          scanf("%d", &num1);
      
          printf("Enter second number: ");
          scanf("%d", &num2);
      
      
          if (num1 == num2) {
              printf("The two numbers are equal.\n");
          }
      
          return 0;
      }


## OUTPUT
![image](https://github.com/user-attachments/assets/d90fa784-d90a-46c7-ab17-850bedd0e71b)

           
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
       #include <stdio.h>
       
       #include <ctype.h>
       
       int main() {
       
           char str[100];
           int i = 0;
       
           
           printf("Enter a string: ");
           fgets(str, sizeof(str), stdin);
       
       
           while (str[i] != '\0') {
               str[i] = tolower(str[i]);
               i++;
           }
       
       
           printf("Lowercase string: %s", str);
       
           return 0;
       }


## OUTPUT
![image](https://github.com/user-attachments/assets/5590a9d6-fd37-4e28-be0a-2bf48f542e3e)





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
        #include <stdio.h>
        
        int main() {
        
            char str[200];
            
            int i = 0, wordCount = 0;
        
        
            printf("Enter a string: ");
            fgets(str, sizeof(str), stdin);
        
        
            do {
                if ((str[i] != ' ' && str[i] != '\n' && str[i] != '\0') &&
                    (str[i + 1] == ' ' || str[i + 1] == '\n' || str[i + 1] == '\0')) {
                    wordCount++;
                }
                i++;
            } while (str[i] != '\0');
        
            
            printf("Total number of words: %d\n", wordCount);
        
            return 0;
        }


## OUTPUT
![image](https://github.com/user-attachments/assets/e1c25587-018f-41bb-aa78-7e760e3d1bc8)





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
       #include <stdio.h>
       
       int compareStrings(const char *str1, const char *str2) {
       
           int i = 0;
           while (str1[i] != '\0' && str2[i] != '\0') {
               if (str1[i] != str2[i]) {
                   return (str1[i] - str2[i]);
               }
               i++;
           }
           if (str1[i] == '\0' && str2[i] == '\0') {
               return 0;
           } else if (str1[i] == '\0') {
               return -1;
           } else {
               return 1;
           }
       }
       
       int main() {
           char str1[100], str2[100];
       
           printf("Enter the first string: ");
           scanf("%s", str1);
           printf("Enter the second string: ");
           scanf("%s", str2);
       
           int result = compareStrings(str1, str2);
       
           if (result == 0) {
               printf("Strings are equal.\n");
           } else if (result < 0) {
               printf("String 1 is less than String 2.\n");
           } else {
               printf("String 1 is greater than String 2.\n");
           }
       
           return 0;
       }



## OUTPUT
![image](https://github.com/user-attachments/assets/3ab0b633-185c-4e93-a28c-971daea03607)

 

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

