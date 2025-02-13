```python
def f(x): 
    return x^2+x+41 

def prime_check(a): 
    if a.is_prime() == True: 
        return "Prime" 
    else: 
        return "Composite"

print(f'The solutions for f(x) when x is between 1 and 10 are as follows')

for a in range(1,11): 
    answer = f(a)
    a_prime = prime_check(answer)
    if a< 10: 
        if answer<100: 
            print(f'x={a}  : f(x)={answer}  |{answer}  is {a_prime}')
        else: 
            print(f'x={a}  : f(x)={answer} |{answer} is {a_prime}')

    else: 
        if answer<100: 
            print(f'x={a} : f(x)={answer}  |{answer}  is {a_prime}')
        else: 
            print(f'x={a} : f(x)={answer} |{answer} is {a_prime}')
```

    The solutions for f(x) when x is between 1 and 10 are as follows
    x=1  : f(x)=43  |43  is Prime
    x=2  : f(x)=47  |47  is Prime
    x=3  : f(x)=53  |53  is Prime
    x=4  : f(x)=61  |61  is Prime
    x=5  : f(x)=71  |71  is Prime
    x=6  : f(x)=83  |83  is Prime
    x=7  : f(x)=97  |97  is Prime
    x=8  : f(x)=113 |113 is Prime
    x=9  : f(x)=131 |131 is Prime
    x=10 : f(x)=151 |151 is Prime



```python
def f(x): 
    return x^2+x+41 

upper = 100

for a in range(1,upper+1): 
    an = f(a) 
    if an.is_prime() == False: 
        counter = an
        break
    else: 
        counter = "none"
        continue 

if counter == "none": 
    print(f'There are no f(x) that are composite up to f({a}).')
else: 
    print(f'There is f({a})={counter} that is composite.')
```

    There is f(40)=1681 that is composite.

