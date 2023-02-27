# Activities

## Task 1:

- Refer to the following link. Discuss how Stacks based on linked lists works:
  https://www.cs.usfca.edu/~galles/visualization/StackLL.html

> Push adds a value to top. The first value points to Null. 
When a new value is added the new value points to the older one. Pop (delete) removes a value from the top.

## Task 2:

The following snippet is from `./src/stack.cpp` lines 25-31.

```cpp
void push(StackNode **root, int new_data)
{
    StackNode *stackNode = newNode(new_data);
    stackNode->next = *root;
    *root = stackNode;
    cout << new_data << endl;
}
```

- Discuss in groups how the code works?

- Why do we need to use double pointers?
> pointer points to a location in memory. The first pointer has the address of the variable. The second pointer stores the address of the first pointer.

## Task 3: Individual (At home)

Practice: Asymptotic Analysis and Upper Bounds. Refer to the following link:
https://opendsa-server.cs.vt.edu/OpenDSA/Exercises/AlgAnal/UpperBoundsSumm.html
