# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:

Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)


## AIM:

To write a Java program that demonstrates stream chaining by placing a BufferedReader on top of an InputStreamReader, which in turn wraps System.in, and then reading user input using this chained stream.


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a BufferedReader object by chaining
4.	System.in → InputStreamReader → BufferedReader.
5.	Use a try block Use readLine() to read the user's name.
6.	Use readLine() again to read the user's age
7.	Catch any IOException and display an appropriate error message.





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Ashqar Ahamed S T
RegisterNumber:  212224240018
*/
```

## SOURCE CODE:

```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        // Chaining: System.in -> InputStreamReader -> BufferedReader
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        try {
            String name = br.readLine();
            String age = br.readLine();
            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }

```



## OUTPUT:

<img width="866" height="553" alt="output 1" src="https://github.com/user-attachments/assets/89e43661-a3c4-4f63-a48d-18b29be6b9a2" />


## RESULT:

Thus, a java was program successfully implemented for chaining of input streams by reading user data through a BufferedReader wrapped over an InputStreamReader.
