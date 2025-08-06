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

Linked List:

```
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

