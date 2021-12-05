# Merge Sort

## 풀이1

```python
def merge(left, right):
    res = []
    left_idx = 0
    right_idx = 0
    while len(left) > left_idx or len(right) > right_idx:
        if left[left_idx] < right[right_idx]:
            res.append(left[left_idx])
            left_idx += 1
        else:
            res.append(right[right_idx])
            right_idx += 1
        if left_idx == len(left):
            for i in range(right_idx, len(right)):
                res.append(right[i])
            break
        elif right_idx == len(right):
            for i in range(left_idx, len(left)):
                res.append(left[i])
            break
    return res

def divide(lis):
    s = 0
    e = len(lis)-1
    if s == e:
        return [lis[s]]
    mid = (s+e)//2
    a = divide(lis[s:mid+1])
    b = divide(lis[mid+1:e+1])
    return merge(a, b)


lis = [4, 7, 2, 1, 8, 5]
ans = divide(lis)
print(ans)
```

## 풀이2

```python
def merge(s, e, mid):
    res = []
    a = s
    b = mid+1
    while s <= mid or b <= e:
        if lis[s] < lis[b]:
            res.append(lis[s])
            s += 1
        else:
            res.append(lis[b])
            b += 1
        if s == mid+1:
            for i in range(b, e+1):
                res.append(lis[i])
            break
        elif b == e+1:
            for i in range(s, mid+1):
                res.append(lis[i])
            break
    t = 0
    for i in range(a, e+1):
        lis[i] = res[t]
        t += 1

def divide(s, e):
    if s == e:
        return
    mid = (s+e)//2
    divide(s, mid)
    divide(mid+1, e)
    merge(s, e, mid)


lis = [4, 7, 2, 1, 8, 5]
divide(0, len(lis)-1)
print(lis)
```

