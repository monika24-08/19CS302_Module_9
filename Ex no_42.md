 # EX 42 C program to write a fuctions to perform push,pop,display,peek in stack using array.
## DATE:23/05/2025
## AIM:
To write a fuctions to perform push,pop,display,peek in stack using array.

## Algorithm
1.Start the program and declare a stack array and a variable top initialized to -1.

2.Define push() to insert an element into the stack if it is not full.

3.Define pop() to remove the top element from the stack if it is not empty.

4.Define peek() to return the topmost element without removing it.

5.Define display() to print all stack elements from top to bottom.

## Program:
```
/*
C program to write a fuctions to perform push,pop,display,peek in stack using array.
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
        printf("%d pushed to stack\n", value);
    }
    else
    {
        printf("Stack overflow\n");
    }
}

void pop()
{
    if(top >= 0)
    {
        printf("%d popped from stack\n", stack[top--]);
    }
    else
    {
        printf("Stack underflow\n");
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
        return -1;
    }
}

void display()
{
    if(top >= 0)
    {
        printf("Stack elements: ");
        for(int i = top; i >= 0; i--)
        {
            printf("%d ", stack[i]);
        }
        printf("\n");
    }
    else
    {
        printf("Stack is empty\n");
    }
}

int main()
{
    push(10);
    push(20);
    push(30);

    display();

    printf("Top element: %d\n", peek());

    pop();
    display();

    return 0;
}


```

## Output:

![image](https://github.com/user-attachments/assets/4831e776-f2b9-4fae-abba-04e8a51f5f28)


## Result:
Thus the program was executed and the output was verified successfully.
