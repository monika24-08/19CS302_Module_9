 # EX 44 C functions to perform enqueue, dequeue, display, peek in Queue using Array.
## DATE: 23/05/2025
## AIM:
To write a C Write a functions to perform enqueue, dequeue, display, peek in Queue using Array.

## Algorithm
1.Start the program and declare an array with front and rear pointers for the queue.

2.Define enqueue() to add an element at the rear if the queue is not full.

3.Define dequeue() to remove an element from the front if the queue is not empty.

4.Define peek() to return the front element without removing it.

5.Define display() to print all elements from front to rear.
## Program:
```
/*
C functions to perform enqueue, dequeue, display, peek in Queue using Array.
Developed by: AASHIKA PARVEEN M R
RegisterNumber: 212223060002
*/
#include <stdio.h>
#define MAX 100

int queue[MAX];
int front = -1, rear = -1;

void enqueue(int value)
{
    if(rear == MAX - 1)
    {
        printf("Queue overflow\n");
        return;
    }
    if(front == -1)
        front = 0;
    queue[++rear] = value;
    printf("%d enqueued to queue\n", value);
}

void dequeue()
{
    if(front == -1 || front > rear)
    {
        printf("Queue underflow\n");
        return;
    }
    printf("%d dequeued from queue\n", queue[front++]);
}

int peek()
{
    if(front == -1 || front > rear)
    {
        printf("Queue is empty\n");
        return -1;
    }
    return queue[front];
}

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
    enqueue(10);
    enqueue(20);
    enqueue(30);

    display();

    printf("Front element: %d\n", peek());

    dequeue();
    display();

    return 0;
}


```

## Output:

![image](https://github.com/user-attachments/assets/8702557e-a403-4205-b10e-0e0ac36e711b)


## Result:
Thus the program was executed and the output was verified successfully.
