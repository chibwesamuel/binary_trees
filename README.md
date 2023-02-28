# C - Binary trees

This project is an implementation of knowledge learned and gained in using Binary Trees as data structures. We learned about how to qualify trees as well as how to traverse them. Throughout the project, we implemented binary, binary search, AVL, and Max Binary Heap trees.

## Header File :file_folder:

Header file containing definitions and prototypes for all types and functions written for the project.

**Data Structures
```
struct binary_tree_s
{
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
};

typedef struct binary_tree_s binary_tree_t;
typedef struct binary_tree_s bst_t;
typedef struct binary_tree_s avl_t;
typedef struct binary_tree_s heap_t;
```

Function Prototypes

| File                             | Prototype                                                                                        |
| -------------------------------- | ------------------------------------------------------------------------------------------------ |
| `binary_tree_print.c`            | `void binary_tree_print(const binary_tree_t *tree)`                                              |
| `0-binary_tree_node.c`           | `binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);`                             |
| `1-binary_tree_insert_left.c`    | `binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);`                      |
| `2-binary_tree_insert_right.c`   | `binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);`                     |
| `3-binary_tree_delete.c`         | `void binary_tree_delete(binary_tree_t *tree);`                                                  |
| `4-binary_tree_is_leaf.c`        | `int binary_tree_is_leaf(const binary_tree_t *node);`                                            |
| `5-binary_tree_is_root.c`        | `int binary_tree_is_root(const binary_tree_t *node);`                                            |
| `6-binary_tree_preorder.c`       | `void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));`                       |
| `7-binary_tree_inorder.c`        | `void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));`                        |
| `8-binary_tree_postorder.c`      | `void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));`                      |
| `9-binary_tree_height.c`         | `size_t binary_tree_height(const binary_tree_t *tree);`                                          |
| `10-binary_tree_depth.c`         | `size_t binary_tree_depth(const binary_tree_t *tree);`                                           |
| `11-binary_tree_size.c`          | `size_t binary_tree_size(const binary_tree_t *tree);`                                            |
| `12-binary_tree_leaves.c`        | `size_t binary_tree_leaves(const binary_tree_t *tree);`                                          |
| `13-binary_tree_nodes.c`         | `size_t binary_tree_nodes(const binary_tree_t *tree);`                                           |
| `14-binary_tree_balance.c`       | `int binary_tree_balance(const binary_tree_t *tree);`                                            |
| `15-binary_tree_is_full.c`       | `int binary_tree_is_full(const binary_tree_t *tree);`                                            |
| `16-binary_tree_is_perfect.c`    | `int binary_tree_is_perfect(const binary_tree_t *tree);`                                         |
| `17-binary_tree_sibling.c`       | `binary_tree_t *binary_tree_sibling(binary_tree_t *node);`                                       |
| `18-binary_tree_uncle.c`         | `binary_tree_t *binary_tree_uncle(binary_tree_t *node);`                                         |
| `100-binary_trees_ancestor.c`    | `binary_tree_t *binary_trees_ancestor(const binary_tree_t *first, const binary_tree_t *second);` |
| `101-binary_tree_levelorder.c`   | `void binary_tree_levelorder(const binary_tree_t *tree, void (*func)(int));`                     |
| `102-binary_tree_is_complete.c`  | `int binary_tree_is_complete(const binary_tree_t *tree);`                                        |
| `103-binary_tree_rotate_left.c`  | `binary_tree_t *binary_tree_rotate_left(binary_tree_t *tree);`                                   |
| `104-binary_tree_rotate_right.c` | `binary_tree_t *binary_tree_rotate_right(binary_tree_t *tree);`                                  |
| `110-binary_tree_is_bst.c`       | `int binary_tree_is_bst(const binary_tree_t *tree);`                                             |
| `111-bst_insert.c`               | `bst_t *bst_insert(bst_t **tree, int value);`                                                    |
| `112-array_to_bst.c`             | `bst_t *array_to_bst(int *array, size_t size);`                                                  |
| `113-bst_search.c`               | `bst_t *bst_search(const bst_t *tree, int value);`                                               |
| `114-bst_remove.c`               | `bst_t *bst_remove(bst_t *root, int value);`                                                     |
| `120-binary_tree_is_avl.c`       | `int binary_tree_is_avl(const binary_tree_t *tree);`                                             |
| `121-avl_insert.c`               | `avl_t *avl_insert(avl_t **tree, int value);`                                                    |
| `122-array_to_avl.c`             | `avl_t *array_to_avl(int *array, size_t size);`                                                  |

## Tasks

0. New node
```
Write a function that creates a binary tree node

    Prototype: binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);
    Where parent is a pointer to the parent node of the node to create
    And value is the value to put in the new node
    When created, a node does not have any child
    Your function must return a pointer to the new node, or NULL on failure
```


1. Insert left
```
Write a function that inserts a node as the left-child of another node

    Prototype: binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);
    Where parent is a pointer to the node to insert the left-child in
    And value is the value to store in the new node
    Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
    If parent already has a left-child, the new node must take its place, and the old left-child must be set as the left-child of the new node.
```


2. Insert right
```
Write a function that inserts a node as the right-child of another node

    Prototype: binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);
    Where parent is a pointer to the node to insert the right-child in
    And value is the value to store in the new node
    Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
    If parent already has a right-child, the new node must take its place, and the old right-child must be set as the right-child of the new node.
```


3. Delete
```
Write a function that deletes an entire binary tree

    Prototype: void binary_tree_delete(binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to delete
    If tree is NULL, do nothing
```


4. Is leaf
```
Write a function that checks if a node is a leaf

    Prototype: int binary_tree_is_leaf(const binary_tree_t *node);
    Where node is a pointer to the node to check
    Your function must return 1 if node is a leaf, otherwise 0
    If node is NULL, return 0
```


5. Is root
```
Write a function that checks if a given node is a root

    Prototype: int binary_tree_is_root(const binary_tree_t *node);
    Where node is a pointer to the node to check
    Your function must return 1 if node is a root, otherwise 0
    If node is NULL, return 0
```


6. Pre-order traversal
```
Write a function that goes through a binary tree using pre-order traversal

    Prototype: void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));
    Where tree is a pointer to the root node of the tree to traverse
    And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
    If tree or func is NULL, do nothing
```


7. In-order traversal
```
Write a function that goes through a binary tree using in-order traversal

    Prototype: void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));
    Where tree is a pointer to the root node of the tree to traverse
    And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
    If tree or func is NULL, do nothing
```



8. Post-order traversal
```
Write a function that goes through a binary tree using post-order traversal

    Prototype: void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));
    Where tree is a pointer to the root node of the tree to traverse
    And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
    If tree or func is NULL, do nothing
```


9. Height
```
Write a function that measures the height of a binary tree

    Prototype: size_t binary_tree_height(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to measure the height.
    If tree is NULL, your function must return 0
```



10. Depth
```
Write a function that measures the depth of a node in a binary tree

    Prototype: size_t binary_tree_depth(const binary_tree_t *tree);
    Where tree is a pointer to the node to measure the depth
    If tree is NULL, your function must return 0
```


11. Size
```
Write a function that measures the size of a binary tree

    Prototype: size_t binary_tree_size(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to measure the size
    If tree is NULL, the function must return 0
```


12. Leaves
```
Write a function that counts the leaves in a binary tree

    Prototype: size_t binary_tree_leaves(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to count the number of leaves
    If tree is NULL, the function must return 0
    A NULL pointer is not a leaf
```


13. Nodes
```
Write a function that counts the nodes with at least 1 child in a binary tree

    Prototype: size_t binary_tree_nodes(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to count the number of nodes
    If tree is NULL, the function must return 0
    A NULL pointer is not a node
```


14. Balance factor
```
Write a function that measures the balance factor of a binary tree

    Prototype: int binary_tree_balance(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to measure the balance factor
    If tree is NULL, return 0
```


15. Is full
```
Write a function that checks if a binary tree is full

    Prototype: int binary_tree_is_full(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to check
    If tree is NULL, your function must return 0
```


16. Is perfect
```
Write a function that checks if a binary tree is perfect

    Prototype: int binary_tree_is_perfect(const binary_tree_t *tree);
    Where tree is a pointer to the root node of the tree to check
    If tree is NULL, your function must return 0
```


17. Sibling
```
Write a function that finds the sibling of a node

    Prototype: binary_tree_t *binary_tree_sibling(binary_tree_t *node);
    Where node is a pointer to the node to find the sibling
    Your function must return a pointer to the sibling node
    If node is NULL or the parent is NULL, return NULL
    If node has no sibling, return NULL
```


18. Uncle
```
Write a function that finds the uncle of a node

    Prototype: binary_tree_t *binary_tree_uncle(binary_tree_t *node);
    Where node is a pointer to the node to find the uncle
    Your function must return a pointer to the uncle node
    If node is NULL, return NULL
    If node has no uncle, return NULL
```

19. Lowest common ancestor
```
    C function that returns a pointer to the lowest common ancestor node of two given nodes in a binary tree.
    Returns `NULL` if no common ancestor is found.
```

20. Level-order traversal
```
    C function that traverses a binary tree using level-order traversal.
```

21. Is complete
```
    C function that checks if a binary tree is complete.
    Returns `1` if the tree is complete, `0` otherwise.
```

22. Rotate left
```
    C function that performs a left-rotation on a binary tree.
    Returns a pointer to the new root node of the tree after rotation.
```

23. Rotate right
```
    C function that performs a right-rotation on a binary tree.
    Returns a pointer to the new root node of the tree after rotation.
```

24. Is BST
```
    C function that checks if a binary tree is a valid binary search tree.
    Returns `1` if the tree is a valid BST, `0` otherwise.
```

25. BST - Insert
```
    C function that inserts a value into a binary search tree.
    Returns a pointer to the new node, or `NULL` on failure.
    If the tree is `NULL`, the value becomes the root node.
    The value is ignored if it is already present in the tree.
```

26. BST - Array to BST
```
    C function that builds a binary search tree from an array.
    Returns a pointer to the root node of the created tree, or `NULL` on failure.
```

27. BST - Search
```
    C function that searches for a value   in a binary search tree.
  * If the value is matched in the BST, returns a pointer to the matched node.
  * Otherwise, returns `NULL`.
```

28. BST - Remove
```
    C function that removes a node from a binary search tree.
  * Returns a pointer to the new root node of the tree after deletion.
  * If the node to be deleted has two children, it is replaced with its first   in-order successor.
```

29. Big O #BST
```
    Text file containing the average time complexities of binary search tree operations (one answer per line):
    * Inserting the value `n`.
    * Removing the node with the value `n`.
    * Searching for a node in a BST of size `n`.
```

30. Is AVL
```
    C function that checks if a binary tree is a valid AVL tree.
  * If the tree is a valid AVL tree, returns `1`.
  * Otherwise, returns `0`.
```

31. AVL - Insert
```
    C function that inserts a value in an AVL tree.
  * Returns a value to the inserted node, or `NULL` on failure.
```

32. AVL - Array to AVL
```
    C function that builds an AVL tree from an array.
  * Returns a pointer to the root node of the created AVL tree, or `NULL` on failure.
  * Ignores duplicate values.

35. Big O #AVL Tree
```
    Text file containing the average time complexities of AVL tree   opeartions (one answer per line):
    * Inserting the value `n`.
    * Removing the node with the value `n`.
    * Searching for a node in an AVL tree of size `n`.
```

41. Big O #Binary Heap
```
    Text file containing the average time complexities of binary heap opeartions (one answer per line):
    * Inserting the value `n`.
    * Extracting the root node.
    * Searching for a node in a binary heap of size `n`.
```

## Authors :black_nib:

Chibwe Samuel Mukosa__ <[smchibwe](https://github.com/smchibwe)>
