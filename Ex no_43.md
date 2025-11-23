 # EX 43 C program to Write a function to display queue elements using array.
## DATE: 23/05/2025
## AIM:
To Write a function to display queue elements using array.

## Algorithm
1.Start the program and declare an array with front and rear variables for the queue.

2.Ensure the queue is not empty before displaying.

3.Traverse the queue from front to rear.

4.Print each element during traversal.

5.End the program.

## Program:
```
/*
C program to write a function to display queue elements using array.
Developed by: AASHIKA PARVEEN M R
RegisterNumber:  212223060002
*/
#include <stdio.h>
#define MAX 100

int queue[MAX];
int front = -1, rear = -1;

void display()
{
    if(front == -1 || front > rear)
    {
        printf("Queue is empty\n");
        return;
    }

    printf("Queue elements: ");
    for(int i = front; i <= rear; i++)
    {
        printf("%d ", queue[i]);
    }
    printf("\n");
}

int main()
{
    front = 0;
    rear = 3;
    queue[0] = 10;
    queue[1] = 20;
    queue[2] = 30;
    queue[3] = 40;

    display();

    return 0;
}


```

## Output:

![image](https://github.com/user-attachments/assets/f6288feb-99c7-4907-8724-1af90badf755)


## Result:
Thus the program was executed and the output was verified successfully.
