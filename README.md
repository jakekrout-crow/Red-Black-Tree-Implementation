# Assignment: Red-Black Tree Implementation

### Length as Designed: 60 minutes

## Introduction

In this assignment, you will implement a complete Red-Black Tree, a self-balancing binary search tree. This assignment tests your ability to implement key operations such as insertion, deletion, and searching while maintaining the Red-Black Tree properties.

### Starter Files

Create a new Jupyter Notebook for your implementation.

## Requirements

Implement a complete Red-Black Tree class in Python with the following methods:

1. Insertion
2. Deletion
3. Search
4. In-order traversal
5. Property verification

Your implementation should include all necessary helper methods, such as color flipping, rotation operations, and property checks.

## Instructions

Implement the Red-Black Tree class with all required methods in your Jupyter Notebook. Ensure your implementation maintains the Red-Black Tree properties after each insertion and deletion operation.

Your implementation should include:

1. A `Node` class to represent individual nodes in the Red-Black Tree, including color property.
2. A `RedBlackTree` class with the following methods:
   - `insert`: Insert a new key into the tree
   - `delete`: Remove a key from the tree
   - `search`: Find a node with a given key
   - `in_order`: Perform an in-order traversal of the tree
   - `verify_rb_properties`: Check if the tree maintains Red-Black properties
   - Any necessary helper methods (e.g., for rotations, color flipping, property checks)

3. Implement the following operations:
   - Left rotation
   - Right rotation
   - Color flipping

4. Ensure that the tree maintains all Red-Black Tree properties after each insertion and deletion operation:
   - Every node is either red or black
   - The root is black
   - Every leaf (NIL) is black
   - If a node is red, then both its children are black
   - For each node, all simple paths from the node to descendant leaves contain the same number of black nodes

5. Include appropriate error handling and edge case management in your implementation.

6. Implement the `verify_rb_properties` method to check if the tree maintains Red-Black properties:
   - Verify that the root is black
   - Check that there are no two adjacent red nodes
   - Ensure that every path from root to leaf has the same number of black nodes

## Testing

To test your implementation, use the following code after your class definitions:

```python
# Test the implementation
rb_tree = RedBlackTree()
keys = [7, 3, 18, 10, 22, 8, 11, 26, 2, 6, 13]

for key in keys:
    rb_tree.insert(key)

print("In-order traversal after insertion:", rb_tree.in_order())
print("RB properties maintained after insertion:", rb_tree.verify_rb_properties())

rb_tree.delete(18)
print("In-order traversal after deleting 18:", rb_tree.in_order())
print("RB properties maintained after deletion:", rb_tree.verify_rb_properties())

print("Searching for 11:", rb_tree.search(11).key if rb_tree.search(11) != rb_tree.NIL else "Not found")
print("Searching for 15:", rb_tree.search(15).key if rb_tree.search(15) != rb_tree.NIL else "Not found")

# Test edge cases
edge_case_keys = [1, 4, 5, 9, 12, 14]
for key in edge_case_keys:
    rb_tree.insert(key)
print("In-order traversal after edge case insertions:", rb_tree.in_order())
print("RB properties maintained after edge case insertions:", rb_tree.verify_rb_properties())
```

Ensure that your implementation produces correct output for these test cases and maintains Red-Black Tree properties throughout all operations.

### Conclusion

This assignment tests your ability to implement a complete Red-Black Tree, including insertion, deletion, search, and traversal operations while maintaining the tree's properties. It also challenges you to implement a method to verify the Red-Black Tree properties. After completing this assignment, you should have a solid grasp of how Red-Black Trees work and how to implement them efficiently.