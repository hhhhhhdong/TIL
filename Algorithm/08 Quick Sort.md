# Quick Sort



## 풀이

```python
def partition(lis, s, e):
    f = s
    while s < e:
        while lis[s] <= lis[f] and s <= e:
            s += 1
        while lis[e] >= lis[f] and s <= e:
            e -= 1
        if s < e:
            lis[s], lis[e] = lis[e], lis[s]
    lis[e], lis[f] = lis[f], lis[e]
    return e


def qs(lis, l, r):
    if l >= r:
        return
    s = partition(lis, l, r)
    qs(lis, l, s-1)
    qs(lis, s+1, r)

a = [3, 4, 1, 57, 3, 5, 14, -1, 88]
qs(a, 0, len(a)-1)
print(a)
```
