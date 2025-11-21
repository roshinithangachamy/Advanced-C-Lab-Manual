## EXP NO:11 C PROGRAM TO FIND THE PEEK OF STACK USING ARRAY.

### Aim:
To write a C program using function to find the peek of stack using array.
### Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
### Program:
```
int stack[100],top;
void peek()
{
    if(top==-1)
    printf("Underflow");
    else
    {
        printf("%d",stack[top]);
    }
}
```
### Output:
<img width="379" height="380" alt="image" src="https://github.com/user-attachments/assets/412ea2b5-10e9-47e0-8edd-3d4d8ef0a78e" />



### Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
### Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
### Program:
```
int size=3,top=-1;
char stack[100];
void push (char data)
{
    if(top==size-1)
    printf("stack is full\n");
    else
    {
        top++;
        stack[top]=data;
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/a2eed418-b2cb-4130-bb8e-667de43e185e)

### Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
### Aim:
To write a C program to display queue elements using array

### Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
### Program:
```
int front,rear;
int queue[100];
void display()
{
    int i=0;
    if(front==-1|| front>rear)
    printf("No elements to display\n");
    else
    {
        for(i=front;i<=rear; i++){
            printf("%d ", queue[i]);
        }
    }
}
```
### Output:
![image](https://github.com/user-attachments/assets/4a302c24-be7d-4a74-bc02-48decf2fe531)

### Result:
Thus, the program to display queue elements using array is verified successfully.
 
## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
### Aim:
To write a C program to insert elements in queue using array.

### Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

### Program:
```
int size=10,rear,front;
int queue[50];
void enqueue(int data)
{
    if(rear<size){
        if(front==-1){
            front=0;
        }
        rear=rear+1;
        queue[rear]=data;
    }
}
```
### Output:

![image](https://github.com/user-attachments/assets/bfebeb8c-236f-4cd9-9e6e-31f8947e0401)

### Result:
Thus, the program to insert elements in queue using array is verified successfully.

## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY
### Aim:

To create a function in C that deletes an element from a queue implemented using an array.

### Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.
### Program:
```
int front, rear;
void dequeue()
{
    if(front==-1|| front>rear){
        
        printf("Queue Underflow.\n");
        return;
    }else{
        front=front+1;
    }
}
```

### Output:
<img width="543" height="471" alt="image" src="https://github.com/user-attachments/assets/779b8d72-d7d5-48a5-9662-4c2e932cb70c" />

### Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
