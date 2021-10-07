### Prime-Factors

* Useful for solving complex problem related to factors.
* Like Sieve of Eratosthenes for Prime no. T.C-- n*log(log n)
* The sieve of Eratosthenes is one of the most efficient ways to find all primes smaller than n when n is smaller than 10 million or so


###  Sieve Of Eratosthenes code :-
```
def SOE(n): 
    p=[True]*(n+1) 
    i=2
    while(i*i <= n): 
        if p[i] == True:      
            for j in range(i*i,n+1,i):
                p[j] = False
        i+=1
    l=[]
    for i in range(2,n): 
        if p[i]: 
            l.append(i)
    return l
x=SOE(100)
print(*x) 
```