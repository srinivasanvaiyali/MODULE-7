# Ex.No:5
# Ex.Name :write a C++ program to implement FCFS algorithm(no of.process p1,p2 and p3 and its burst time are 10,5 & 8) find out waiting time of the each process & Average waiting time of the process?
## Date:
## Aim:
To write a C++ program to implement the First-Come, First-Served (FCFS) scheduling algorithm, calculate waiting time for each process, and find the average waiting time.

## Algorithm:
STEP 1: Start the program.

STEP 2: Read the number of processes from the user.

STEP 3: Declare arrays to store process IDs and burst times.

STEP 4: Read the burst time for each process from the user.

STEP 5: Initialize an array to store waiting times. Set the waiting time of the first process as 0.

STEP 6: Calculate the waiting time for each subsequent process using:

WT[i] = WT[i-1] + BT[i-1]

where WT is waiting time and BT is burst time.

STEP 7: Compute the sum of all waiting times to calculate average waiting time.

STEP 8: Calculate average waiting time as:

Average WT = Sum of WT / Number of processes

STEP 9: Display process IDs, burst times, and waiting times.

STEP 10: Display the average waiting time and end the program.




## Program:
```
#include <iostream>
using namespace std;

void calculateWT(int bt[], int wt[], int n)
{
    wt[0] = 0;
    for (int i = 1; i < n; i++) 
    {
        wt[i] = wt[i - 1] + bt[i - 1];
    }
}

void display( int bt[], int wt[], int n) 
{
    cout << "Processes   BT time   WT time"<<endl;
    for (int i = 0; i < n; i++) 
    {
        cout<<"       "<<i+1<<"       "<<bt[i]<<"       "<<wt[i]<<endl;
    }
}

void calculateAverageWT(int wt[], int n) 
{
    float sum = 0;
    for (int i = 0; i < n; i++) 
    {
        sum += wt[i];
    }
    cout << "Average waiting time = " << sum/n << endl;
}

int main()
{
    int n=4;


    int bt[n], wt[n];

    for (int i = 0; i < n; i++) 
    {
        cin >> bt[i];
    }

    calculateWT(bt, wt, n);
    display( bt, wt, n);
    calculateAverageWT(wt, n);

    return 0;
}
```


## Output:
<img width="927" height="595" alt="519144831-8fa08431-f3cb-41a8-a376-d7835352f717" src="https://github.com/user-attachments/assets/acd105c4-ce69-4479-9104-c5cfb5dc7118" />



## Result:
The program successfully calculates the waiting time for each process and the average waiting time using FCFS scheduling based on user input.
