# Ex. No: 15B - Build a Binary Tree with Integer & String Values

## AIM:
To write a Python program to build a binary tree with a root, left, and right node using string & integer-point values.

## ALGORITHM:

1. **Start the program.**
2. **Import** the `Node` class from the `binarytree` module.
3. **Create a root node** using the `Node` class and assign a string & integer-point value.
4. **Create left and right child nodes** for the root with string & integer values.
5. **Convert the tree** to a list and print the list of nodes.
6. **End the program.**

## PYTHON PROGRAM

```
from binarytree import Node
l=[]
for i in range(0,3):
    a=input()
    l.append(a)
root = Node(l[0])
root.left = Node(l[1])
root.right = Node(l[2])
print("Binary Tree : ")
for i in root.values:
    print(i,'-->',end=" ")
```

## OUTPUT
![image](https://github.com/user-attachments/assets/f2e90fa8-786a-45e3-81b6-34d48ab1b24f)

## RESULT
Thus a Python program to build a binary tree with string & integer values is implemented successfully.
