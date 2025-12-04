# Ex.No:4  
# Ex.Name: Remove a Node from a Doubly Linked List using STL  

## Date:  

## Aim:  
To write a C++ program to remove a node from a doubly linked list using STL and display the list before and after removal.  

## Algorithm:  
1. Start the program.  
2. Create an STL `list<int>` to store integer elements.  
3. Insert `n` elements into the list.  
4. Display the list before removing any element.  
5. Read the element to be removed.  
6. Use the `remove()` function of STL to delete the specified element.  
7. Display the list after removal.  
8. Stop the program.  

## Program:
```cpp
#include <list>
#include <iostream>
using namespace std;

int main() {
    list<int> a;
    int data;

    // Insert 5 elements into the list
    for (int i = 0; i < 5; i++) {
        cin >> data;
        a.push_back(data);
    }

    cout << "List before removing elements: ";
    for (auto it = a.begin(); it != a.end(); it++) {
        cout << *it << " ";
    }

    // Read element to be removed
    cin >> data;
    a.remove(data);

    cout << "\nList after removing elements: ";
    for (auto it = a.begin(); it != a.end(); it++) {
        cout << *it << " ";
    }

    return 0;
}
```

## Output:
<img width="865" height="449" alt="image" src="https://github.com/user-attachments/assets/996a5499-5036-46f5-bc29-7aa8a74144d2" />

## Result:
```
Input:
10 20 30 40 50
30

Output:
List before removing elements: 10 20 30 40 50
List after removing elements: 10 20 40 50
```
