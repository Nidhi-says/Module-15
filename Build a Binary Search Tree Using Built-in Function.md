# Ex. No: 15A - Build a Binary Search Tree Using Built-in Function

## AIM:
To write a Python program to build a binary search tree using a built-in function.

## ALGORITHM:

1. **Start the program.**
2. Define `_build_bst_from_sorted_values(sorted_values)` to recursively build a binary search tree (BST) from a sorted list.
3. Define `right_subtree(l)` to print the right subtree of the BST.
4. Take user input for the number of elements and store the values in a list `a`.
5. Sort the list and pass it to `_build_bst_from_sorted_values()` to construct the BST.
6. Print the postorder traversal of the BST.
7. Call `right_subtree(l)` to print the right subtree.
8. Check whether the tree is a binary search tree using the `is_bst` property.
9. **End the program.**

## PROGRAM:

```
from binarytree import Node

def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values)==0:
        return None
    mid_index=len(sorted_values)//2
    root=Node(sorted_values[mid_index])
    root.left=_build_bst_from_sorted_values(sorted_values[:mid_index])
    root.right=_build_bst_from_sorted_values(sorted_values[mid_index+1:])
    return (root)
    
def subtree(l):
    print("Right Subtree :")
    for i in l[2].values:
        print(i,'-->',end='')
    return
        

a=[]
s=int(input())
for i in range(s):
    val=int(input())
    a.append(val)
x=sorted(a)
t=_build_bst_from_sorted_values(x)
print("Postorder :",t.postorder)
subtree(t)
print("\nIs this a Binary Search Tree? ",t.is_bst)
```

## OUTPUT
![image](https://github.com/user-attachments/assets/00fcea75-b5a0-4339-8484-c6a6fdc81261)

## RESULT
Thus a Python program to build a binary search tree using a built-in function is implemented successfully.
