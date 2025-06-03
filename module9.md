EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
#include <stdio.h>
#define MAX 5

int stack[MAX];
int top = -1;

void display() {
    if (top == -1) {
        printf("Stack is empty.\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

void push(int value) {
    if (top == MAX - 1) {
        printf("Stack Overflow! Cannot push %d\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("%d pushed into stack.\n", value);
    }
}

void pop() {
    if (top == -1) {
        printf("Stack Underflow! Cannot pop.\n");
    } else {
        printf("%d popped from stack.\n", stack[top]);
        top--;
    }
}

int main() {
    int choice, value;
    while (1) {
        printf("\n--- Stack Menu ---\n");
        printf("1. Push\n");
        printf("2. Pop\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
        case 1:
            printf("Enter value to push: ");
            scanf("%d", &value);
            push(value);
            break;
        case 2:
            pop();
            break;
        case 3:
            display();
            break;
        case 4:
            printf("Exiting program.\n");
            return 0;
        default:
            printf("Invalid choice! Please try again.\n");
        }
    }
    return 0;
}
Output:

--- Stack Menu ---

1.Push
2.Pop
3.Display
4.Exit Enter your choice: 1 Enter value to push: 10 10 pushed into stack.


--- Stack Menu ---

1.Push
2.Pop
3.Display
4.Exit Enter your choice: 1 Enter value to push: 20 20 pushed into stack.


--- Stack Menu ---

1.Push
2.Pop
3.Display
4.Exit Enter your choice: 3 Stack elements are: 20 10


--- Stack Menu ---

1.Push
2.Pop
3.Display
4.Exit Enter your choice: 2 20 popped from stack.

--- Stack Menu ---

1.Push
2.Pop
3.Display
4.Exit Enter your choice: 3 Stack elements are: 10


--- Stack Menu ---

1.Push
2.Pop
3.Display
4.Exit Enter your choice: 4 Exiting program.



Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

//type your code here

Output:

//paste your output here#include <stdio.h>
#define MAX 5

float stack[MAX];
int top = -1;

void push(float value) {
    if (top == MAX - 1) {
        printf("Stack Overflow! Cannot push %.2f\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("%.2f pushed into stack.\n", value);
    }
}

int main() {
    int choice;
    float value;
    while (1) {
        printf("\n--- Stack Menu ---\n");
        printf("1. Push\n");
        printf("2. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
        case 1:
            printf("Enter floating value to push: ");
            scanf("%f", &value);
            push(value);
            break;
        case 2:
            printf("Exiting program.\n");
            return 0;
        default:
            printf("Invalid choice! Please try again.\n");
        }
    }
    return 0;
}
Output:

--- Stack Menu ---

1.Push
2.Exit Enter your choice: 1 Enter floating value to push: 12.5 12.50 pushed into stack.

--- Stack Menu ---

1.Push
2.Exit Enter your choice: 1 Enter floating value to push: 45.75 45.75 pushed into stack.

--- Stack Menu ---

1.Push
2.Exit Enter your choice: 1 Enter floating value to push: 30.25 30.25 pushed into stack.

--- Stack Menu ---

1.Push
2.Exit Enter your choice: 2 Exiting program.




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d\n", queue[i]);
        }
    }
}

void enqueue(int value) {
    if (rear == MAX - 1) {
        printf("Queue Overflow! Cannot enqueue %d\n", value);
    } else {
        if (front == -1) {
            front = 0;
        }
        rear++;
        queue[rear] = value;
        printf("%d enqueued into queue.\n", value);
    }
}

void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue Underflow! Cannot dequeue.\n");
    } else {
        printf("%d dequeued from queue.\n", queue[front]);
        front++;
    }
}

int main() {
    int choice, value;
    while (1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Enqueue\n");
        printf("2. Dequeue\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
        case 1:
            printf("Enter value to enqueue: ");
            scanf("%d", &value);
            enqueue(value);
            break;
        case 2:
            dequeue();
            break;
        case 3:
            display();
            break;
        case 4:
            printf("Exiting program.\n");
            return 0;
        default:
            printf("Invalid choice! Please try again.\n");
        }
    }
    return 0;
}


Output:

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Display
4.Exit Enter your choice: 1 Enter value to enqueue: 10 10 enqueued into queue.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Display
4.Exit Enter your choice: 1 Enter value to enqueue: 20 20 enqueued into queue.


--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Display
4.Exit Enter your choice: 3 Queue elements are: 10 20

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Display
4.Exit Enter your choice: 2 10 dequeued from queue.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Display
Exit Enter your choice: 3 Queue elements are: 20

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Display
4.Exit Enter your choice: 4 Exiting program.


Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
#include <stdio.h>
#define MAX 5

float queue[MAX];
int front = -1;
int rear = -1;

void enqueue(float value) {
    if (rear == MAX - 1) {
        printf("Queue Overflow! Cannot enqueue %.2f\n", value);
    } else {
        if (front == -1) {
            front = 0;
        }
        rear++;
        queue[rear] = value;
        printf("%.2f enqueued into queue.\n", value);
    }
}

int main() {
    int choice;
    float value;
    while (1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Enqueue\n");
        printf("2. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
        case 1:
            printf("Enter float value to enqueue: ");
            scanf("%f", &value);
            enqueue(value);
            break;
        case 2:
            printf("Exiting program.\n");
            return 0;
        default:
            printf("Invalid choice! Please try again.\n");
        }
    }
    return 0;
}
Output:

--- Queue Menu ---

1.Enqueue
2.Exit Enter your choice: 1 Enter float value to enqueue: 12.5 12.50 enqueued into queue.


--- Queue Menu ---

1.Enqueue
2.Exit Enter your choice: 1 Enter float value to enqueue: 45.75 45.75 enqueued into queue.


--- Queue Menu ---

1.Enqueue
2.Exit Enter your choice: 1 Enter float value to enqueue: 30.25 30.25 enqueued into queue.


--- Queue Menu ---

1.Enqueue
2.Exit Enter your choice: 2 Exiting program.

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
#include <stdio.h>
#define MAX 5

int queue[MAX];
int front = -1;
int rear = -1;

void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue is empty. Cannot delete element.\n");
    } else {
        printf("%d deleted from queue.\n", queue[front]);
        front++;
        if (front > rear) {
            front = -1;
            rear = -1;
        }
    }
}

void enqueue(int value) {
    if (rear == MAX - 1) {
        printf("Queue Overflow! Cannot enqueue %d\n", value);
    } else {
        if (front == -1) {
            front = 0;
        }
        rear++;
        queue[rear] = value;
        printf("%d enqueued into queue.\n", value);
    }
}

int main() {
    int choice, value;
    while (1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Enqueue\n");
        printf("2. Dequeue\n");
        printf("3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        switch (choice) {
        case 1:
            printf("Enter value to enqueue: ");
            scanf("%d", &value);
            enqueue(value);
            break;
        case 2:
            dequeue();
            break;
        case 3:
            printf("Exiting program.\n");
            return 0;
        default:
            printf("Invalid choice! Please try again.\n");
        }
    }
    return 0;
}
Output:

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Exit Enter your choice: 1 Enter value to enqueue: 10 10 enqueued into queue.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Exit Enter your choice: 1 Enter value to enqueue: 20 20 enqueued into queue.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Exit Enter your choice: 2 10 deleted from queue.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Exit Enter your choice: 2 20 deleted from queue.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Exit Enter your choice: 2 Queue is empty. Cannot delete element.

--- Queue Menu ---

1.Enqueue
2.Dequeue
3.Exit Enter your choice: 3 Exiting program.


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
