resursions:

dividing the problem into subproblem and finding the solution until we find a base condition.
If we are unable to find the base condition then it will run the loop recursively.

```python
def find_pow(val1):
    if val1==0:
        return 1
    else:
        pow1=find_pow(val1-1)
        return 2*pow1
find_pow(3)

```
