
# EX.NO : 6(C)  CIRCULAR LINKED LIST 
 
# PROGRAM STATEMENT: 
 
To write a CPP program to SEARCH an element from the Circularly Linked List and Display the same. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define a Node class with data and nextptr (pointer to next node). 
3. Create a create() function to create a new node with given data and set its nextptr to 0. 
4. If the list is empty (head == 0), set both head and tail to the new node, otherwise, add the node at the end and update tail->nextptr to head. 
5. Implement the display() function to traverse the circular linked list and print each node’s data until it reaches back to head. 
6. Implement the search() function to traverse the list and compare each node’s data with a given target, printing whether it is found or not. 
7. In main(), input 5 integers to create the list, input a target element, display the list, and search for the target in the list. 
8. End the program 
 
# PROGRAM:
```
#include <iostream>
using namespace std;

class circular
{
public:
    int data;
    circular *next;
};

circular *start = NULL, *end1 = NULL;

void create(int);
void display();
void search(int);

int main()
{
    int data;

    for (int i = 0; i < 5; i++)
    {
        cin >> data;
        create(data);
    }
    display();

    cin >> data;
    search(data);

    return 0;
}

void create(int data)
{
    circular *newnode = new circular;

    newnode->data = data;
    newnode->next = start;

    if (start == NULL)
    {
        start = newnode;
        end1 = newnode;
    }
    else
    {
        end1->next = newnode;
        end1 = newnode;
    }
}

void display()
{
    if (start == NULL)
    {
        cout << "List is empty\n";
        return;
    }

    circular *node = start;

    cout << "Data = " << node->data << " ";
    node = node->next;

    while (node != start)
    {
        cout << "Data = " << node->data << " ";
        node = node->next;
    }
    cout << endl;
}

void search(int key)
{
    if (start == NULL)
    {
        cout << "List is empty. Element not found.\n";
        return;
    }

    circular *temp = start;
    bool found = false;

    do
    {
        if (temp->data == key)
        {
            cout << "Element " << key << " Found\n";
            found = true;
            break;
        }
        temp = temp->next;
    } while (temp != start);

    if (!found)
    {
        cout << "Element not Found\n";
    }
}
```
# output:

![image](https://github.com/user-attachments/assets/0e91f80c-4431-4546-bcaf-cda0d66bd157)

#  RESULT: 
 
Thus, the C++ program to SEARCH an element from the Circularly Linked List and Display the same is created successfully. 
