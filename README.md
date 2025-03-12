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
        
