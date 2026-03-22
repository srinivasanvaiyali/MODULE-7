# Ex.No:2
# Ex.Name : Write a CPP program for Prefix To Postfix Conversion using Stack STL
## Date:
## Aim:
To write a C++ program to convert a prefix expression into a postfix expression using STL stack.

## Algorithm:
STEP 1: Start the program.

STEP 2: Include the , , and headers.

STEP 3: Read the prefix expression from the user.

STEP 4: Declare a stack of strings to store intermediate expressions.

STEP 5: Traverse the prefix expression from right to left.

STEP 6: If the current character is an operand, push it as a string onto the stack.

STEP 7: If the current character is an operator, pop the top two elements from the stack.

STEP 8: Concatenate the two operands followed by the operator to form a new postfix expression.

STEP 9: Push the new postfix expression back onto the stack.

STEP 10: After traversal, the stack will contain the final postfix expression. Display it.




## Program:
```
#include<bits/stdc++.h>
using namespace std;
bool isOperator(char c)
{
    switch(c)
    {
        case '+':
        case '-':
        case '*':
        case '/':
            return true;
    }
    return false;
}

string preToPost(string prefix)
{
    int n = prefix.size();
    stack<string> s;
    int i;
    for(i=n-1;i>=0;i--)
    {
        if(isOperator(prefix[i]))
        {
            string op1 = s.top();
            s.pop();
            string op2 = s.top();
            s.pop();
            string temp = op1+op2+prefix[i];
            s.push(temp);
        }
        else
        {
            s.push(string(1,prefix[i]));
        }
    }
    string postfix="";
    while(!s.empty())
    {
        postfix += s.top();
        s.pop();
    }
    return postfix;
}

int main()
{
    string prefix;
    cin>>prefix;
    cout<<"Prefix to Postfix expression:"<<endl<<preToPost(prefix);
}
```


## Output:

<img width="795" height="311" alt="519141544-ee7d06f2-0dec-44b9-b129-7a49a1ee9100" src="https://github.com/user-attachments/assets/3a7bc1a1-7c19-4724-8717-dc0232b0bf37" />


## Result:
The program successfully converts a prefix expression into a postfix expression using the stack STL.
