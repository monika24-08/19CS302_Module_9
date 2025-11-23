# EX 41 C program to write a function to find the peek of stack using array.
## DATE:23/05/2025
## AIM:
To write a function to find the peek of stack using array.

## Algorithm
1.Start the program and declare an array to implement the stack.

2.Define a function peek to return the top element of the stack.

3.Check if the stack is empty before accessing the top element.

4.If the stack is empty, return a suitable message or value indicating an empty stack.

5.End the program.
## Program:
```
/*
C program to write a function to find the peek of stack using array.
Developed by: AASHIKA PARVEEN M R
RegisterNumber:  212223060002
*/
#include <stdio.h>
#define MAX 100

int stack[MAX];
int top = -1;

void push(int value)
{
    if(top < MAX - 1)
    {
        stack[++top] = value;
    }
    else
    {
        printf("Stack overflow\n");
    }
}

int peek()
{
    if(top >= 0)
    {
        return stack[top];
    }
    else
    {
        printf("Stack is empty\n");
        return -1;  // Returning -1 to indicate empty stack
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    printf("Top of the stack: %d\n", peek());

    return 0;
}


```

## Output:

![image](https://github.com/user-attachments/assets/28a2ee02-1a3c-4681-890a-80124d8b08ed)


## Result:
Thus the program was executed and the output was verified successfully.
