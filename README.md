# 19CS301-Module-10
EX: 10.1  Stack

### AIM: 

To create a Python program that pushes even numbers into a stack and pops the last three elements.

### ALGORITHM:
Step 1: Start

Step 2: Read number of elements

Step 3: Read the elements and push even numbers into a stack

Step 4: Print the stack after pushing

Step 5: Pop the last 3 elements

Step 6: Print the updated stack

Step 7: Stop


### PROGRAM:
```
l=[]
n=int(input())
for i in range(n):
    value=int(input())
    if value%2==0:
        l.append(value)
print(l)
for i in range(3):
    l.pop()
print(l)    
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/7dd123f5-297f-42ad-ad1d-307f32043847)



### RESULT: 
The program successfully pushes even numbers into a stack and pops the last 3 elements as expected.

EXP.No: 10.2 Implenetation of Stack

### AIM: 

To check whether the given string is a palindrome or not.


###ALGORITHM:
Step 1: Start

Step 2: Read a string from the user

Step 3: Reverse the string using slicing

Step 4: Compare original and reversed strings

Step 5: If equal, print "Yes" (it’s a palindrome)

Step 6: Stop


### PROGRAM:
```
stack = []
top = -1
def push(ele: str):
    global top
    top += 1
    stack[top]= ele
def pop():
    global top
    ele = stack[top]
    top -= 1
    return ele
def isPalindrome(string: str) -> bool:
        global stack
        length = len(string)
        stack = ['0']*  (length + 1)
        mid = length//2
        i=0
        while i < mid:
            push(string[i])
            i += 1
        if length % 2 != 0:
            i += 1
        while i<length:
            ele = pop()
            if ele !=string[i]:
                return False
            i +=1 
        return True
if __name__=="__main__":
    string = input()
    if isPalindrome(string):
        print("Yes")
    else:
        print("No")
```
###OUTPUT:


![image](https://github.com/user-attachments/assets/589a93cc-c26f-4278-82b9-18278b7928d7)




###RESULT: 

The program correctly identifies whether a given string is a palindrome or not.


EX: 10.3 Queue


### AIM: 
To add only even and unique numbers to a deque using appendleft() from n user inputs.

### ALGORITHM:

1. Start
2. Import deque from collections
3. Read number of elements (n)
4. For each number
5. Print the deque
6. Stop

### PROGRAM:


```from abc import ABC
from collections import deque
class Queue:
    def __init__(self):
        self.queue = deque()
    def add_element(self,val):
        if val%2==0 and val not in self.queue:
            self.queue.appendleft(val)
            return True
        return False
TheQueue = Queue()
n=int(input())
for i in range(n):
    TheQueue.add_element(int(input()))
print(TheQueue.queue)    
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/825a087f-b6c7-4825-a5d5-407780dd1127)



### RESULT: 

The program correctly adds even, unique numbers to the left of the deque using appendleft().

EXP.No: 10.4    Types of Queue

### AIM:

To display the colors and the number of colors input by the user using the multiprocessing library.


###ALGORITHM: 

Step 1: Start

Step 2: Import multiprocessing

Step 3: Define a function to print the count of colors

Step 4: Define a function to print all the colors

Step 5: In main:
  
Step 6: Stop

###PROGRAM:
```
from multiprocessing import Queue

colors = []
cnt = 0
# instantiating a queue object
queue = Queue()
n=int(input())
colours=[]
for i in range(n):
    colours.append(input())
for color in colours:
    queue.put(color)
    cnt += 1
print('count-', cnt)
for i in range(n):
    print(queue.get())
    
```
### OUTPUT:
 
![image](https://github.com/user-attachments/assets/0cb88695-c3e2-4f1a-8a8c-81f5894a13f1)


### RESULT: 

The program successfully uses multiprocessing to display the count and list of colors input by the user.

EXP.No: 10.5   ASSESSMENT EXAM -10 -SEB


### AIM:

To get 5 values from the user, store them in a circular queue, and display the values.


###ALGORITHM: 

Step 1: Start

Step 2: Create a CircularQueue class with methods:
       
Step 3: Initialize the circular queue with size 5

Step 4: Take 5 inputs from the user and enqueue them

Step 5: Display the queue elements

Step 6: Stop


###PROGRAM:
```
import queue
q=queue.Queue()
for i in range(5):
    q.put(int(input()))
for i  in range(5):
    print(q.get(),end=" ")
```
### OUTPUT:
 
![image](https://github.com/user-attachments/assets/2b4949c0-381a-4149-b458-c1e8ac908a34)


 

### RESULT: 

The program uses a circular queue to store 5 user inputs and displays them successfully.




