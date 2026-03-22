# Ex.No:1
# Ex.Name :Write a CPP Program to insert five double elements in to stack using linked list (use STL for Stack)
## Date:
## Aim:
To write a C++ program to insert five double elements into a stack using the STL stack container (which is internally implemented as a linked list) and display the elements.

## Algorithm:
STEP 1: Start the program.

STEP 2: Include the and headers.

STEP 3: Declare a stack of type double.

STEP 4: Read 5 double values from the user.

STEP 5: Use the push() function to insert each value into the stack.

STEP 6: Display a message indicating that elements are inserted into the stack.

STEP 7: Use a loop to display the elements using the top() function.

STEP 8: Remove each element from the stack after displaying using pop().

STEP 9: Repeat until the stack becomes empty.

STEP 10: End the program.




## Program:
```
#include <iostream>
#include <stack>
using namespace std;

int main() 
{
    stack<double> st;
    int n;

    cin >> n;

    for (int i = 0; i < n; ++i) 
    {
        double val;
        cin >> val;
        st.push(val);
    }

    cout << "Current size of the stack is " << st.size() << endl;

    cout << "The top element of the stack is " << st.top() << endl;

    st.pop();
    cout << "The top element after 1 pop operation is " << st.top() << endl;

    st.pop();
    cout << "The top element after 2 pop operations is " << st.top() << endl;

    cout << "Size of the stack after 2 pop operations is " << st.size() << endl;

    return 0;
}
```



## Output:
<img width="1169" height="486" alt="519140865-b9420aba-ca0c-485f-83f1-01a2aacc953c" src="https://github.com/user-attachments/assets/ed11f437-c3ba-49d6-80e3-3411d12a83dc" />



## Result:
The program successfully inserts five double elements into the stack and displays them in LIFO (Last In First Out) order.
