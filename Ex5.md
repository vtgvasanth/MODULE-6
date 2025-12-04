# Ex.No:5  
# Ex.Name: Insert 5 Elements into a Singly Linked List using STL  

## Date:  

## Aim:  
To write a C++ program to insert 5 elements into a singly linked list using STL and display the list.  

## Algorithm:  
1. Start the program.  
2. Define a `Node` class with members `data` and `next`.  
3. Write a function `push()` to insert elements at the beginning of the list.  
4. Insert 5 elements into the list by calling `push()`.  
5. Write a function `printList()` to traverse and display the list.  
6. Call the function to print all elements of the list.  
7. Stop the program.  

## Program:
```cpp
#include <bits/stdc++.h>
using namespace std;

class Node {
public:
    int data;
    Node* next;
};

// Function to insert a node at the beginning
void push(Node** head_ref, int new_data) {
    Node* new_node = new Node();
    new_node->data = new_data;
    new_node->next = (*head_ref);
    (*head_ref) = new_node;
}

// Function to print the linked list
void printList(Node* node) {
    while (node != NULL) {
        cout << node->data << " ";
        node = node->next;
    }
}

int main() {
    Node* head = NULL;

    // Insert 5 elements
    push(&head, 50);
    push(&head, 40);
    push(&head, 30);
    push(&head, 20);
    push(&head, 10);

    cout << "The forward list operation: ";
    printList(head);

    return 0;
}
```

## Output:
<img width="881" height="314" alt="image" src="https://github.com/user-attachments/assets/45d9b978-0caa-4e68-8eb1-ae8e451280f7" />

## Result:
```
The forward list operation: 10 20 30 40 50
```
