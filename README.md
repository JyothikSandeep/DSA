# Stack:

```python
#Last In First Out LIFO
len_stack=3
stack=[]
def push(character):
    
    if overflow():
        return("stack too full")
    else:
        stack.append(character)
        return("element has been pushed in stacked")
def pop():
    if nothing():
        return("cannot delete")
    else:
        stack.pop()
        return ("element has been poped from the list")
def overflow():
    if len(stack)>=len_stack:
        return(True)
    else:
        return(False)
def nothing():
    if len(stack)==0:
        return(True)
    else:
        return(False)
def peek():
    if nothing()==True:
        return ("there is nothing")
    else:
        return(stack[-1])
def paste():
    return(stack)

while True:
     print("1. press 1 to push the element")
     print("2. press 2 to pop the element ")
     print("3. press 3 to find the peek element ")
     print("4. press 4 to print the stack ")
     print("5. press 5 to exit the code ")
    val1=input()
     if val1=="1":
        b=str(input())
        a=push(b)
        print(a)
     elif val1=="2":
        a=pop()
        print(a)
     elif val1=="3":
        a=peek()
        print(a)
     elif val1=="4":
        a=paste()
        print(a)
     elif val1=="5":
        break
     else:
         print("please enter valid input")


```
Example pattern of stack concepr:
Matching paranthesis:

```python

s1=")()"
l1=[]
count=0
for i in range(len(s1)):
	if s1[i]=="(":
		l1.append(s1[i])
		print(l1)
	elif s1[i]==")":
		if len(l1)>0:
			l1.pop()
			print(l1)
		elif len(l1)==0:
			count=count+1
	else:
		print("Please enter a valid input")
		break
if len(l1)>0 or count>0:
 print("False")
else:
 print("True")


```

# Queue

```python
queue=[]
head=[-1]
rear=[-1]
len_queue=3
def qenqueue(character):
# global head
# global rear
     if qoverflow():
         return("Can not enqueue character")
     else:
     if head[0]==-1 and rear[0]==-1:
         head[0]=0
         rear[0]=0
         queue.append(character)
         return("Character was enqued")
     else:
         rear[0]=rear[0]+1
         queue
        .append
        (character)
         return
        ("Character was enqueued")


def qdequeue():
 #head=-1
 #rear=-1
     global queue
     if qempty():
        return("Can't dequeue")
     elif head[0]==rear[0]:
         head[0]=-1
         rear[0]=-1
         queue=[]
        return("Character was dequeued")
     else:
         queue[head[0]]=-1
         head[0]=head[0]+1
        return("Character was dequeued")

def qhead():
     if qempty():
        return ("No head")
     else:
        return(queue[head[0]])
def qrear():
     if qempty():
        return("No rear")
     else:
        return(queue[rear[0]])
def printqueue():
     print(head[0],rear[0])
     return(queue[head[0]:rear[0]+1])
def qoverflow():
    if len(queue)>=len_queue:
        return True
    else:
        return False
def qempty():
    if head[0]==-1 and rear[0]==-1:
        return True
    else:
        return False

i=0
while i==i:

    print("1. enqueue")
    print("2. dequeue")
    print("3. head")
    print("4. rear")
    print("5. print queue")
    print("6. end")
    val1=input()
    if val1=="1":
        a=qenqueue(input())
     print(a)
    elif val1=="2":
        a=qdequeue()
        print(a)
     elif val1=="3":
        a=qhead()
        print(a)
     elif val1=="4":
        a=qrear()
        print(a)
     elif val1=="5":
        a=printqueue()
        print(a)
     elif val1=="6":
        break
     else:
        print("please enter a valid input")


```

# Linked List:

1. Insertion at begining
2. Insertion at end
3. Insertiion in any position
4. Deletion at begining
5. Deletion at end
6. Deletion at any position 

``` python
head=None
class Node:
    def _init_(self,val):
        self.val=val1
        self.next=None
while(1):
    print(" ")
    print("press 1 to insert Begin")
    print("press 2 to insertion at end")
    print("press 3 to insertion at any pos")
    print("press 4 to delete at begining")
    print("press 5 to delete at end")
    print("press 6 to delete at any postion")
    print("press 7 to display Linked list")
    print("press 8 to break")
    print(" ")
    option=int(input())
    if(option==1):
        val1=int(input("insert at begin value: "))
        obj1=Node(val1)
        if(head==None):
            head=obj1
        else:
            obj1.next=head
            head=obj1
    elif(option==2):
        # insert at last
        val1=int(input("insert at end value: "))
        obj1=Node(val1)
        temp=head
        if(head==None):
            head=obj1
        else:
            while(temp.next!=None):
                temp=temp.next
            temp.next=obj1
    elif(option==3):
        val1=int(input("insertion at any position value:"))
        obj1=Node(val1)
        position=int(input("enter the ppostion: "))
        
        pos=0
        curr=head
        
        while(curr!=None ):
            if(pos==position-1):                
                break
            pos=pos+1
            curr=curr.next
        if(curr==None):
            # print("hello")
            curr=obj1
            if(head==None):
                head=obj1
        else:
            obj1.next=curr.next
            curr.next=obj1
         
            pos=pos+1
#         curr
    elif(option==4):
      if(head==None):
        print("It is not possible as you have not yet added a value")
      else:
        head=head.next
    elif(option==5):
      temp=head
      if(head==None):
        print("It is not possible as you have not yet added a value")
      else:
        while(temp.next!=None):
          curr=temp
          temp=temp.next
        curr.next=None
    elif(option==6):
        poss=int(input("Enter the position which you want to delete"))
        pos1=0
        curr=head
        print(head.val,"-")
        prev=None
        if(curr==None):
          print("It is not possible as you have not yet added a value")
        else:
          
          while(curr!=None ):
              if(pos1==poss-1):                
                  break
              pos1=pos1+1
              prev=curr
              curr=curr.next
          if(curr==None):
            print("It is not possible as the position you have given has exeeded the length of list")
          else:
            after=curr.next
            prev.next=after
            curr=curr.next
    elif(option==7):
        temp=head
        while(temp!=None):
            print(temp.val,end=" ")
            temp=temp.next
        print(" ")
    elif(option==8):
        break
```


recursions:

dividing the problem into subproblems and finding the solution until we find a base condition.
If we are unable to find the base condition then it will run the loop recursively.

```python
#code to find power of a 2
def find_pow(val1):
    if val1==0:
        return 1
    else:
        pow1=find_pow(val1-1)
        return 2*pow1
find_pow(3)

```

when to user recursions and when not to use?

When we are dividing the problems into subproblems then we need to use recursions and solve the given problem.

When we have some constriants like need to solve it in some particular timecomplexity then this is not a better approach to follow and we need to remember that recursions will take more memory while solving the problems


Question1:
easy pattern:

231. Power of Two
342. Power of Four
326. Power of Three
509. Fibonacci Number
3304. Find the K-th Character in String Game I

Easy done.

medium:





formula:

If we have two type of burgers one is normal one and another is premium one and we have some amount we need to buy max premium without exceeding cost:







        remaining_budget = r - (n * x)
        max_premium_burgers = remaining_budget // (y - x)
        premium_burgers = min(max_premium_burgers, n)
        normal_burgers = n - premium_burgers
        
Dynamic programming:


 In dynamic programming there are some concepts:

 1D DP:

1.recursion.
2.Top down approach
3. bottom up approach

Climbing stairs:

recursions:

```python
def climb(n):
    if n <= 2:
        return n
    return climb(n-1) + climb(n-2)

```

top down approach:

```python
def climbStairs(n, dp):
    if n <= 2:
        return n
    if dp[n] != -1:
        return dp[n]
    dp[n] = climbStairs(n-1, dp) + climbStairs(n-2, dp)
    return dp[n]

n = 5
dp = [-1] * (n+1)
print(climbStairs(n, dp))  # Output: 8

```

bottom up approach:

```python
def climbStairs(n):
    if n <= 2:
        return n
    dp = [0] * (n+1)
    dp[1], dp[2] = 1, 2
    for i in range(3, n+1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]

print(climbStairs(5))  # Output: 8


```


# 2D dynamic programming:
62. Unique Paths
```python
class Solution:
    def uniquePaths(self, m: int, n: int) -> int:

        def call(i,j):

            if(i<0 or j<0 or i>m or j>n):
                return 0
            if(i==0 and j==0):
                return 1
            if(DP[i][j]!=-1):
                return DP[i][j]
            up=call(i,j-1)
            left=call(i-1,j)
            DP[i][j]=up+left
            
            return DP[i][j]
        DP=[[-1 for i in range(n)] for i in range(m)]
        return call(m-1,n-1)
        

```

What is the Fractional Knapsack Problem?

You’re a thief with:

A knapsack (bag) of capacity W.

n items, each with a weight and a value.

Your goal is to maximize total value in your bag.
But here’s the twist:

You can take fractions of an item (cutting it if needed).

For example, take half of a gold bar if your bag is almost full.


🔑 Intuition

This is a pure Greedy problem (no DP needed):

Compute value per weight ratio: value/weight.

Sort items in descending order of ratio.

Take as much as you can from the highest ratio item.

If you can’t take the whole item, take a fraction.

Repeat until the bag is full.

This works because:

Choosing the highest value/weight ratio first always gives an optimal solution when fractional items are allowed.

Input:
Capacity (W): 50
Items:
Weight: [10, 20, 30]
Value:  [60, 100, 120]

Steps:
Item	Weight	Value	Value/Weight
1	10	60	6
2	20	100	5
3	30	120	4

Take item 1 fully → bag has 40 left → total = 60

Take item 2 fully → bag has 20 left → total = 60+100=160

Take 20/30 of item 3 → total = 160+ (20 * 4)=160+80=240

✅ Max value = 240.

```python

class Item:
    def __init__(self, value, weight):
        self.value = value
        self.weight = weight

def fractional_knapsack(W, items):
    # Sort by value-to-weight ratio
    items.sort(key=lambda x: x.value / x.weight, reverse=True)

    total_value = 0.0
    for item in items:
        if W >= item.weight:
            # Take full item
            W -= item.weight
            total_value += item.value
        else:
            # Take fraction
            total_value += item.value * (W / item.weight)
            break
    return total_value

# Example usage
items = [Item(60, 10), Item(100, 20), Item(120, 30)]
W = 50
print(f"Maximum value in Knapsack = {fractional_knapsack(W, items)}")

```

LC 1710: Maximum Units on a Truck
 → Fractional Knapsack variant (take max units with capacity).



 
 
 

LC 1833: Maximum Ice Cream Bars
 → Similar greedy idea.

[LC 1353: Maximum Number of Events That Can Be Attended] → Scheduling variant.

# Trees

# 🌳 Binary Trees in Python (Patterns & Problems)

This document covers **core tree patterns** with both **theory and code**:  
Traversals → Easy Structural Problems → DFS/BFS Applications → BST Logic → Advanced Problems.  

---

## 🔹 1. Traversals

Traversal means **visiting all nodes** in a tree in some order.

- **Preorder** → Root → Left → Right  
- **Inorder** → Left → Root → Right  
- **Postorder** → Left → Right → Root  
- **Level Order** → Level by level (BFS)

---

### Preorder (Root → Left → Right)
```python
def preorder(root):
    return [] if not root else [root.val] + preorder(root.left) + preorder(root.right)
```

📌 Use-case: Copying the tree, serialization, prefix expressions.

---

### Inorder (Left → Root → Right)
```python
def inorder(root):
    return [] if not root else inorder(root.left) + [root.val] + inorder(root.right)
```

📌 Use-case: In a BST, inorder traversal gives **sorted order**.

---

### Postorder (Left → Right → Root)
```python
def postorder(root):
    return [] if not root else postorder(root.left) + postorder(root.right) + [root.val]
```

📌 Use-case: Deleting/freeing nodes, postfix expressions.

---

### Level Order (BFS)
```python
from collections import deque
def level_order(root):
    if not root: return []
    q, res = deque([root]), []
    while q:
        level = []
        for _ in range(len(q)):
            node = q.popleft()
            level.append(node.val)
            if node.left: q.append(node.left)
            if node.right: q.append(node.right)
        res.append(level)
    return res
```

📌 Use-case: Shortest path in an unweighted tree, zigzag traversals, etc.  
✅ Practice: LC 94, 144, 145, 102

---

## 🔹 2. Easy Structural Problems

These problems focus on **shape and symmetry** of trees.

---

### Max Depth (LC 104)
*Depth = longest path from root to a leaf.*
```python
def maxDepth(root):
    return 0 if not root else 1 + max(maxDepth(root.left), maxDepth(root.right))
```

---

### Symmetric Tree (LC 101)
*A tree is symmetric if left subtree is a mirror of the right.*
```python
def isSymmetric(root):
    def isMirror(a, b):
        if not a and not b: return True
        if not a or not b: return False
        return a.val == b.val and isMirror(a.left, b.right) and isMirror(a.right, b.left)
    return isMirror(root.left, root.right)
```

---

### Invert Tree (LC 226)
*Swap left and right children recursively.*
```python
def invertTree(root):
    if not root: return None
    root.left, root.right = invertTree(root.right), invertTree(root.left)
    return root
```

---

### Path Sum (LC 112)
*Check if there is a root-to-leaf path whose sum = target.*
```python
def hasPathSum(root, s):
    if not root: return False
    if not root.left and not root.right: return s == root.val
    return hasPathSum(root.left, s-root.val) or hasPathSum(root.right, s-root.val)
```

---

## 🔹 3. DFS/BFS Applications

These problems require **exploring deeper properties** of trees.

---

### Diameter of Binary Tree (LC 543)
*Diameter = longest path between any two nodes.*
```python
def diameterOfBinaryTree(root):
    dia = 0
    def dfs(node):
        nonlocal dia
        if not node: return 0
        l, r = dfs(node.left), dfs(node.right)
        dia = max(dia, l+r)
        return 1+max(l,r)
    dfs(root)
    return dia
```

---

### Sum Root-to-Leaf Numbers (LC 129)
*Treat path as number → sum them all.*
```python
def sumNumbers(root):
    def dfs(node, s):
        if not node: return 0
        s = s*10 + node.val
        if not node.left and not node.right: return s
        return dfs(node.left, s) + dfs(node.right, s)
    return dfs(root, 0)
```

---

### Path Sum II (LC 113)
*Find all paths whose sum = target.*
```python
def pathSum(root, target):
    res = []
    def dfs(node, path, s):
        if not node: return
        path.append(node.val)
        if not node.left and not node.right and s+node.val == target:
            res.append(list(path))
        dfs(node.left, path, s+node.val)
        dfs(node.right, path, s+node.val)
        path.pop()
    dfs(root, [], 0)
    return res
```

---

## 🔹 4. BST Problems

Binary Search Tree (BST) → Left < Root < Right  
Problems test **ordering properties**.

---

### Validate BST (LC 98)
*Check if tree follows BST rules.*
```python
def isValidBST(root):
    def check(node, low, high):
        if not node: return True
        if not (low < node.val < high): return False
        return check(node.left, low, node.val) and check(node.right, node.val, high)
    return check(root, float("-inf"), float("inf"))
```

---

### LCA of BST (LC 235)
*Lowest Common Ancestor using BST property.*
```python
def lowestCommonAncestor(root, p, q):
    while root:
        if p.val < root.val and q.val < root.val: root = root.left
        elif p.val > root.val and q.val > root.val: root = root.right
        else: return root
```

---

### BST Iterator (LC 173)
*Flatten BST into sorted iterator using inorder.*
```python
class BSTIterator:
    def __init__(self, root):
        self.stack = []
        self.pushLeft(root)

    def pushLeft(self, node):
        while node:
            self.stack.append(node)
            node = node.left

    def next(self):
        node = self.stack.pop()
        if node.right: self.pushLeft(node.right)
        return node.val

    def hasNext(self):
        return len(self.stack) > 0
```

---

## 🔹 5. Advanced Structural Problems

Harder problems requiring **serialization and transformation**.

---

### Serialize & Deserialize (LC 297)
*Convert tree ↔ string using preorder.*
```python
from collections import deque
class Codec:
    def serialize(self, root):
        if not root: return "N"
        return f"{root.val},{self.serialize(root.left)},{self.serialize(root.right)}"

    def deserialize(self, data):
        def helper(nodes):
            val = nodes.popleft()
            if val == "N": return None
            node = TreeNode(int(val))
            node.left, node.right = helper(nodes), helper(nodes)
            return node
        return helper(deque(data.split(",")))
```

---

### Flatten to Linked List (LC 114)
*Turn tree into right-skewed linked list.*
```python
def flatten(root):
    def dfs(node):
        if not node: return None
        left_tail, right_tail = dfs(node.left), dfs(node.right)
        if left_tail:
            left_tail.right = node.right
            node.right, node.left = node.left, None
        return right_tail or left_tail or node
    dfs(root)
```

---

## 🔑 Key Takeaways

* **Traversals** → Core visiting strategies.  
* **Structural** → Shape-based problems (depth, symmetry, invert).  
* **DFS/BFS Apps** → Deeper properties (diameter, path sums).  
* **BST** → Ordering-based problems.  
* **Advanced** → Serialization + flattening.  

📌 Master these → You’ll cover 80% of tree interview questions.



