class BST:
    def _init_(self, val):
        self.left=None
        self.data=val
        self.right=None
        
    def insert_node(self, new_node):
        if new_node.data<self.data:
            if self.left==None:
                self.left=new_node
                print("Node is inserted: ", new_node.data)
            else:
                self.left.insert_node(new_node)
        else:
            if self.right==None:
                self.right=new_node
                print("Node is inserted: ",new_node.data)
            else:
                self.right.insert_node(new_node)
                
#Inorder Traversal        
def inorder_traversal(self):
    if self==None:
        return
    print(self.data, end=" ")
    inorder_traversal(self.left)
    inorder_traversal(self.right)
        
#Preorder Traversal        
def preorder_traversal(self):
    if self==None:
        return
    print(self.data, end=" ")
    preorder_traversal(self.left)
    preorder_traversal(self.right)  

#Postorder Traversal        
def postorder_traversal(self):
    if self==None:
        return
    postorder_traversal(self.left)
    postorder_traversal(self.right) 
    print(self.data, end=" ")
    
    
#Calling code      
root=BST(14)
root.insert_node(BST(20))
root.insert_node(BST(18))
root.insert_node(BST(12))
root.insert_node(BST(2))
root.insert_node(BST(30))
print("Inorder traversal...")
inorder_traversal(root)
print()
print("Preorder traversal...")
preorder_traversal(root)
print()
print("Postorder traversal...")
postorder_traversal(root)
