# Python Часть 3

## Задание 1

```py
n = int(input())
m = (n + 24) // 25
print(m, n // m)
```

## Задание 2

```py
t = int(input())

for m in range(t):
    n = int(input())
    p, q = map(int, input().split())
    
    s = "0."
    for k in range(n):
        p *= 2
        s += str(p // q)
        p %= q
        
    print(s)
```

## Задание 3

```py
t = int(input())

for m in range(t):
    p1, q1, p2, q2, p3, q3, p4, q4 = map(int, input().split())
    
    a = (p1 * q2 + p2 * q1) * q3 * q4
    b = (p3 * q4 + p4 * q3) * q1 * q2
    
    if a == b:
        print(0, end=" ")
    elif a < b:
        print(-1, end=" ")
    else:
        print(1, end=" ")
```

## Задание 4

```py
n = int(input())
a = list(map(int, input().split()))

s = ""
for x in a:
    bx = bin(x)[2:]
    y = len(bx)
    by = bin(y)[2:]
    z = len(by)
    s += "0" * (z - 1) + by + bx[1:]

print(s)
```

## Задание 5

```py
s = input()
a = []
i = 0

while i < len(s):
    z = 1
    while s[i] == "0":
        z += 1
        i += 1
        
    y = int(s[i : i + z], 2)
    i += z
    
    x = int("1" + s[i : i + y - 1], 2)
    i += y - 1
    a.append(x)

n = len(a)
print(n)
print(*a)
```