🔗 clsDoublyLinkedList

A Generic, Fully-Featured Doubly Linked List Implementation in C++

This repository provides a robust and extensible implementation of a Doubly Linked List in C++ using templates.
The class clsDoublyLinkedList<T> is designed to be efficient, easy to integrate, and suitable for academic practice, projects, and production-level systems that require custom data structures.

🚀 Features
✔ Generic Template Support

Works with any data type (int, string, custom structs, and more).

✔ Full Node Control

Includes a complete internal clsNode structure with direct access to:

prev

data

next

✔ Core Operations

The library provides all essential linked list operations:

Insert at beginning, end, or after a specific node or index.

Delete first, last, by node, or by index.

Search for nodes or values.

Update nodes by index.

Clean and reset the entire list.

✔ Safe and Flexible Access

Get first or last node/data.

Get node or data by index (supports negative indices like Python).

Check size and empty state.

✔ Utility Functions

Print list in normal mode.

Print detailed node relations.

Reverse the list in-place.

📦 Class Overview
Class Template
template <class T>
class clsDoublyLinkedList

Main Components

clsNode
Internal node structure storing the data and two pointers.

Size Tracking
Efficient O(1) list size tracking via _size.

Head Pointer
Private _head pointer with static/instance operation variations.

📘 Example Usage
#include "clsDoublyLinkedList.h"

int main() {
    clsDoublyLinkedList<int> list;

    list.insert_at_beginning(3);
    list.insert_at_end(10);
    list.insert_after(0, 7);

    list.print();  // NULL <--> 3 <--> 7 <--> 10 <--> NULL

    list.del_first_node();
    list.print_detail();

    return 0;
}

🧩 Key Static vs Instance Functions

Static Functions:
Work on any passed head pointer — ideal for standalone list manipulation.

Instance Functions:
Operate directly on the list object and maintain _size properly.

This dual design makes the library flexible for:

Utility usage

Encapsulated OOP usage

Educational demonstrations

🛠 Implementation Highlights

Manual memory management using new (delete is intentionally commented for flexibility).

Supports bidirectional traversal.

Reversible by swapping prev and next.

Negative indexing for convenience:

get(-1) returns the last element.

get(-2) returns the second last.

📏 Complexity
Operation	Complexity
Insert At Beginning	O(1)
Insert At End	O(n)
Insert After Node	O(1)
Delete Node	O(1)
Find	O(n)
Get by Index	O(n)
Reverse	O(n)
📄 License

This project is open-source and free to use for education, commercial, or personal development.

🤝 Contributing

Pull requests are welcome. If you have improvements, optimizations, or new features, feel free to contribute!
