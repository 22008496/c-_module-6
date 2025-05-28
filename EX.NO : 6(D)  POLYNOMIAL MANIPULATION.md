
#  EX.NO : 6(D)  POLYNOMIAL MANIPULATION 
 
# PROGRAM STATEMENT: 
 
To debug a C++ function int printList(Node *head) to print the polynomial expression in polynomial addition program using Linked list concept. 
 
# ALGORITHM:   
 
1. Define a function printList that takes a pointer to the head node of a linked list as input. 
2. Print "Linked List" as the header. 
3. Use a while loop to traverse the linked list as long as head is not NULL: 
4. For each node, print its coeff (coefficient) followed by "x^" and its power (exponent). 
5. Move to the next node by setting head = head->next. 
6. Once all nodes are printed, return 1 to indicate successful completion. 
7. End the program. 
 
# PROGRAM:
```
void addPolynomials(Node *head1,
                    Node *head2)
{
  if(head1==NULL &&head2==NULL)
     
    return;
  else if(head1->power ==head2->power)

            {
    cout << " " << head1->coeff +  head2->coeff <<"x^" << head1->power << " ";

                addPolynomials(head1->next,head2->next);
  }
  else if(head1->power > head2->power)
  {
    cout << " " << head1->coeff <<"x^" << head1->power << " ";

                addPolynomials(head1->next, head2);
  }
  else
  {
    cout << " " << head2->coeff <<"x^" << head2->power << " ";

                addPolynomials(head1, head2->next);
  }
}
```
# output:

![image](https://github.com/user-attachments/assets/04ec8bae-5fd3-4a1f-a610-1af725f455d6)

# RESULT: 

Thus, the C++ program to print the polynomial expression in polynomial addition program using Linked list concept is created successfully.
