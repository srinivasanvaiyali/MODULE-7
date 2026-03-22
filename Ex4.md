# Ex.No:4
# Ex.Name :Write a CPP Program to implement Queue using Linked List, insert double elements in to Q and delete two items from Q. 


## Date:
## Aim:
To write a C++ program to implement a queue using a linked list, insert character elements, delete two items from the queue, and display the remaining elements.

## Algorithm:
STEP 1: Start the program.

STEP 2: Define a Node structure with members:

data → character value of the node

next → pointer to the next node

STEP 3: Declare front and rear pointers for the queue and initialize them as nullptr.

STEP 4: Read 5 character values from the user and insert them into the queue using enqueue.

STEP 5: For insertion, create a new node and link it at the rear of the queue.

STEP 6: Update the rear pointer to point to the new node.

STEP 7: To delete elements, remove nodes from the front of the queue using dequeue.

STEP 8: Update the front pointer after deletion.

STEP 9: Display the remaining elements in the queue by traversing from front to rear.

STEP 10: End the program.




## Program:
```
#include<iostream>
using namespace std;

class Node
{
    public:
        char data;
        Node *next;
}*rear,*temp,*front;

void push()
{
    temp = new Node;
    cin>>temp->data;
    temp->next=NULL;
    if(rear == NULL)
    {
        front = temp;
        rear = temp;
    }
    else
    {
        rear->next = temp;
        rear = rear->next;
    }
}

void pop()
{
    if(front == NULL)
    {
        cout<<"Underflow."<<endl;
    }
    
    else
    {
        temp = front;
        front = front->next;
        temp->next=NULL;
        free(temp);
    }
}


void display()
{
    temp = front;
    while(temp!=NULL)
    {
        cout<<temp->data<<" ";
        temp = temp->next;
    }
    cout<<endl;
}

void disp()
{
    temp = front;
    cout<<"Queue Front : "<<temp->data;
    
    while(temp->next!=NULL)
    {
        temp = temp->next;
    }
    cout<<endl;
    cout<<"Queue Rear : "<<temp->data;
}


int main()
{
    int n;
    cin>>n;
    pop();
    for(int i=0;i<n;i++)
    {
        push();
    }
    cout<<"Queue :";
    display();
    pop();
    pop();
    
    cout<<"After DeQueue :";
    display();
    disp();
}
```



## Output:
<img width="814" height="802" alt="519143896-a6ae2351-d649-4026-aeb5-11c1850c87b3" src="https://github.com/user-attachments/assets/b9d6f686-6a83-431a-ad9b-7031af49e4bd" />



## Result:
The program successfully implements a queue using a linked list, inserts character elements, deletes two items, and displays the remaining elements.
