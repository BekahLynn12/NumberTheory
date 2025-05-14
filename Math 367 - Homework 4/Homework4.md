```python
def abund(n): 
    sigma_n = sigma(n,1)
    if sigma_n > 2*n: 
        return True
    else: 
        return False
    
abundant_nums_10 = []

n=1 
while len(abundant_nums_10)<10: 
    test = abund(n)
    if test == True: 
        abundant_nums_10.append(n) 
        n+= 1
    else: 
        n+= 1

print(f'The first 10 abundant numbers are {abundant_nums_10}.')
```

    The first 10 abundant numbers are [12, 18, 20, 24, 30, 36, 40, 42, 48, 54].



```python
def abund(n): 
    sigma_n = sigma(n,1)
    if sigma_n > 2*n: 
        return True
    else: 
        return False

def frequency(upper):
    a = 1 
    abundant_nums = []
    while a <= upper: 
        test = abund(a)
        if test == True: 
            abundant_nums.append(a) 
            a+= 1
        else: 
            a+= 1
    freq = len(abundant_nums) 
    return freq



for n in [100,1000,10000,100000]:
    freq_n = frequency(n)
    print(f'The frequency of abundant numbers in the first {n} integers is {freq_n} integers out of {n}.')
```

    The frequency of abundant numbers in the first 100 integers is 22 integers out of 100.
    The frequency of abundant numbers in the first 1000 integers is 246 integers out of 1000.
    The frequency of abundant numbers in the first 10000 integers is 2488 integers out of 10000.
    The frequency of abundant numbers in the first 100000 integers is 24795 integers out of 100000.

