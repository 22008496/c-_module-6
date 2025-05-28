
# EX.NO : 6(B)  DOUBLY LINKED LIST 
 
# PROGRAM STATEMENT: 
 
To write a CPP program to INSERT an Element at LOCATION 1 in Doubly Linked List Using 
STL and Display the same. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Initialize an empty list ele of integers. 
3. Use a loop to input 5 integers from the user, adding each to the end of ele using push_back. 
4. Input an additional integer, ent, and add it to the front of ele using push_front. 
5. Print "List: ". 
6. Use a loop to iterate through ele from beginning to end, printing each element. 
7. End the program. 
 
# PROGRAM:
```
#include <iostream>
#include <list>
#include <sstream>

using namespace std;

void displayList(const list<int>& myList) {
    cout << "List: ";
    for (auto it = myList.begin(); it != myList.end(); ++it) {
        cout << *it << " ";
    }
    cout << endl;
}

int main() {
    list<int> myList;
    int element;

    // Input elements into the doubly linked list
    string input;
    getline(cin, input);
    istringstream iss(input);
    while (iss >> element) {
        if (element == -1)
            break;
        myList.push_back(element);
    }

    int insertElement;
    cin >> insertElement;

    // Inserting at location 1
    auto it = myList.begin();
    myList.insert(it, insertElement);

    // Display the updated list
    displayList(myList);

    return 0;
}
```
# output:

![Screenshot 2025-05-27 134118](https://github.com/user-attachments/assets/3fd7d335-1000-478d-af20-680dfbb27cdc)

# RESULT: 
 
Thus, the C++ program to INSERT an Element at LOCATION 1 in Doubly Linked List Using STL and Display the same is created successfully. 
