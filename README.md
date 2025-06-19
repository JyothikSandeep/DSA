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


