
#  EX.NO : 6(A)  SINGLY LINKED LIST 
 
# PROGRAM STATEMENT : 
 
To write a CPP program to INSERT an Element at location 2 using STL and Display the same. 
 
# ALGORITHM:   
 
1. Start the program 
2. Initialize a forward_list of integers, flist, with values {1, 2, 3, 4, 5}. 
3. Create an iterator it pointing to the beginning of the list. 
4. Move the iterator it to the second position in the list. 
5. Insert the integer 50 after the position indicated by it. 
6. Use a loop to iterate over flist from the beginning to the end, printing each element. 
7. End the program. 
 
# PROGRAM: 
```
#include <iostream>
#include <forward_list>
using namespace std;

int main() {
    forward_list<int> sll = {1, 2, 3, 4, 5};

    // Target position and value to insert
    int position = 2;
    int value = 50;

    // Use iterator to reach position before the desired index
    auto it = sll.before_begin();  // Before the first element
    for (int i = 0; i < position; ++i) {
        ++it;
    }

    // Insert the value
    sll.insert_after(it, value);

    // Display the updated list
    for (int val : sll) {
        cout << val << " ";
    }
    cout << endl;

    return 0;
}
```
# output:

![Screenshot 2025-05-27 133745](https://github.com/user-attachments/assets/9f3e30ab-9e39-4bb1-b1cf-83936b068f10)

# Result:
Thus, the C++ program to INSERT an Element at location 2 using STL and Display the same is created successfully. 
