# <Red-Black-Tree-Implementation>

# Description

This project was made as part of an assignment for a CS2000 class
This project aims to make use of the red-black-tree sorting method for binary trees and show how they are able to self balance by making use of the colors of each node instead of having to look at the entire tree each time a new node is inserted and the tree needs to be rebalanced. 

# Usage

to use this code, create a new code block in assignment.ipynb and include the values and functions you would like to test
below is several different examples:

## for inserting new nodes: 
rb_tree = RedBlackTree()
keys = [7, 3, 18, 10, 22, 8, 11, 26, 2, 6, 13]

for key in keys:
    rb_tree.insert(key)

print("In-order traversal after insertion:", rb_tree.in_order())
print("RB properties maintained after insertion:", rb_tree.verify_rb_properties())

## to remove a node from the tree:
rb_tree.delete(18)
print("In-order traversal after deleting 18:", rb_tree.in_order())
print("RB properties maintained after deletion:", rb_tree.verify_rb_properties())

## to search for a specific value and find its location: 
print("Searching for 11:", rb_tree.search(11).key if rb_tree.search(11) != rb_tree.NIL else "Not found")


# about the author:
Joan Krout wrote this code while attending atlas school and taking the CS2000 class while in the Systems Programming course track.