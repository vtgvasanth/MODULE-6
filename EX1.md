# Ex.No:1  
# Ex.Name: Subtract two polynomials using Linked List  

## Date:  

## Aim:  
To write a C++ function `void subPolynomials(Node *head1, Node *head2)` to subtract and display the difference of two polynomial expressions using the Linked List concept.  

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with members `coeff`, `power`, and `next`.  
3. Create two linked lists representing polynomials.  
4. Write a function `subPolynomials(Node *head1, Node *head2)` that:  
   - Traverses both lists simultaneously.  
   - If the powers are equal, subtract the coefficients and print the term.  
   - If one power is greater, print that term directly.  
   - Continue until both lists are exhausted.  
5. Call the function to display the result of subtraction.  
6. Stop the program.  

## Program:
```cpp
void subPolynomials(Node *head1, Node *head2)
{
    if (head1 == NULL && head2 == NULL)
        return;

    else if (head1->power == head2->power) {
        cout << " " << head1->coeff - head2->coeff 
             << "x^" << head1->power << " ";
        subPolynomials(head1->next, head2->next);
    }
    else if (head1->power > head2->power) {
        cout << " " << head1->coeff << "x^" << head1->power << " ";
        subPolynomials(head1->next, head2);
    }
    else {
        cout << " " << head2->coeff << "x^" << head2->power << " ";
        subPolynomials(head1, head2->next);
    }
}
```

## Output:
<img width="875" height="411" alt="image" src="https://github.com/user-attachments/assets/9896e5e5-f865-4e52-8183-f44e2ab215a7" />

## Result:
```
Linked List
 5x^2 4x^1
Linked List
 6x^2 4x^1
Difference :
 -1x^2  0x^1
```
