# Ex.No:3  
# Ex.Name: Modify an Element from a Circular Linked List  

## Date:  

## Aim:  
To write a C++ program to modify (replace) an element from a circular linked list and display the list before and after modification.  

## Algorithm:  
1. Start the program.  
2. Define a `node` class with `value` and `next` pointer.  
3. Create a function `create(int dat)` to insert nodes into the circular linked list.  
4. Create a function `display()` to print all elements of the list.  
5. Create a function `replace(int a, int b)` to:  
   - Traverse the circular list.  
   - Find the node with value `a` and replace it with `b`.  
6. In the `main()` function:  
   - Read 5 integers and create the circular linked list.  
   - Display the list.  
   - Read the element to be replaced and the new element.  
   - Call `replace()` and display the modified list.  
7. Stop the program.  

## Program:
```cpp
#include<iostream>
using namespace std;

class node {
public:
    int value;
    node* next;
} *head, *tail, *temp, *newnode;

void create(int dat) {
    newnode = new node();
    newnode->value = dat;
    newnode->next = NULL;
    if (head == NULL) {
        head = newnode;
        tail = newnode;
    } else {
        tail->next = newnode;
        tail = newnode;
        tail->next = head;
    }
}

void display() {
    temp = head;
    while (temp->next != head) {
        cout << "Data = " << temp->value << " ";
        temp = temp->next;
    }
    cout << "Data = " << temp->value << " ";
}

void replace(int a, int b) {
    temp = head;
    while (temp->next != head) {
        if (temp->value == a) {
            temp->value = b;
            break;
        }
        temp = temp->next;
    }
    if (temp->value == a)  // check last node
        temp->value = b;
}

int main() {
    int data;
    for (int i = 0; i < 5; i++) {
        cin >> data;
        create(data);
    }
    display();

    int x, y;
    cin >> x >> y;
    replace(x, y);

    cout << endl;
    display();
    return 0;
}
```

## Output:
<img width="885" height="451" alt="image" src="https://github.com/user-attachments/assets/cbe98852-2b10-4b21-a272-d34a15604077" />

## Result:
```
Input:
10 20 30 40 50
40
24

Output:
Data = 10 Data = 20 Data = 30 Data = 40 Data = 50 
Data = 10 Data = 20 Data = 30 Data = 24 Data = 50
```
