# Tree
A tree is a data structure in which its datat items are connected by usign references.  Trees are made up of nodes.  The different types of trees are binary trees, binary search trees, and balanced binary search trees.  We will talk about each of these.  Before we go into details of each tree, it is important to learn the different parts of a tree first.

![image](https://user-images.githubusercontent.com/75501838/207478694-fcaf6923-09a6-47f9-b178-8fffb53d7801.png)

Root node: Each tree begins with a root node.  This is the beginning of the tree that we use to access each element connected to the tree.

Parent node: After the root node, the parent nodes come next.  These nodes are also referred to as internal nodes since they are a part of the tree that are connected to the root node.  Each of these nodes is also connected to its child nodes.  Parent nodes mist have at least one child node connected to it.

Child node: These are the nodes that are connected to the tree through the parent node.

Leaf node: These nodes are the end of the tree.  These nodes have no children, which means they are no nodes connected to the tree through them.  They are the last nodes in the tree.

# Binary Tree
Binary trees are actually pretty simple.  This type of tree begins with one root node.  A binary tree can only consist of a maximum of 2 children.

![image](https://user-images.githubusercontent.com/75501838/207478748-e38bcee4-dc33-4753-ae9a-fb9863aacaea.png)

Here is an example of how we can make this tree in python:

    class BinaryTreeNode:
      def __init__(self, data):
        self.data = data
        self.leftChild = None
        self.rightChild = None

    node1 = BinaryTreeNode(50)
    node2 = BinaryTreeNode(20)
    node3 = BinaryTreeNode(45)
    node4 = BinaryTreeNode(11)
    node5 = BinaryTreeNode(15)
    node6 = BinaryTreeNode(30)
    node7 = BinaryTreeNode(78)

    node1.leftChild = node2
    node1.rightChild = node3
    node2.leftChild = node4
    node2.rightChild = node5
    node3.leftChild = node6
    node3.rightChild = node7

# Binary Search Tree
A binary search tree folows rules for the data you want to put into the tree.  In a BST (binary search tree), the data will be compared to the data in its parent node.  Is the data is less than the parent node, it will be added to the left of the tree.  If the data is larger than the parent node, it will be added to the right of the tree.  The purpose of doing this is to sort out and organize your data.

![image](https://user-images.githubusercontent.com/75501838/207479787-e5bf62c8-a030-4817-ac64-bde6a9274762.png)

Here is an example of how we can do this in python:

    def search(root,key):
     
        if root is None or root.val == key:
            return root

        if root.val < key:
            return search(root.right,key)
   
        return search(root.left,key)

# Balanced Binary Search Tree
A balanced binary search tree is a tree in which at every node, its left subtree and right subtree have an equal height.  If they do not have an equal height, their height can only differ by 1.

![image](https://user-images.githubusercontent.com/75501838/207479904-389b8762-b419-49a5-985e-6e8ed037f239.png)

Here is an example of how we can do this in python:

    class TreeNode(object):
      def __init__(self, x):
        self.val = x
        self.left = None
        self.right = None

    def sorted_array_to_bst(nums):
    
        if not nums:
            return None
        mid_val = len(nums)//2
        node = TreeNode(nums[mid_val])
        node.left = sorted_array_to_bst(nums[:mid_val])
        node.right = sorted_array_to_bst(nums[mid_val+1:])
        return node

    def preOrder(node): 
        if not node: 
            return      
        print(node.val)
        preOrder(node.left) 
        preOrder(node.right) 

# Operations

# Example

# Problme to Solve
