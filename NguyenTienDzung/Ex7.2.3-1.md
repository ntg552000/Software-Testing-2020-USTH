## Ex 7.2.3-1
```
a)
(1): start
(6): end
Graph:
(1) --> (2)
(2) --> (3)
(3) --> (4)
(3) --> (5)
(4) --> (5)
(5) --> (2)
(2) --> (6)
(6) --> (1)
b)
- dup1: [1, 2, 8]
- dup2: [1, 2, 3, 5, 6]
- dup3: [4, 3, 5, 6]
- dup4: [4, 3, 5, 7, 2, 8]
- dup5: [4, 3, 5, 6, 7, 2, 8]
```

c)
||direct|with sidetrip|
|---|---|---|
|t1|dup1||
|t2||dup1|
|t3|dup2|dup1|
|t4|dup4||
|t5|dup3, dup5||
|t6||dup3, dup4, dup5|

```
d)
- dup1 (for def(1))
- dup4 (for def(4))
e)
dup1, dup3, dup5.
f)
dup1, dup3, dup4, dup5.
```
