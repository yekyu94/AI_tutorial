# MAP

 * r = map(func, seq)
 * 많은량의 데이터를 빠르게 처리할 수 있음

## MAP 예제
```python
def my_func(x):
	return x**2
	
my_list = [1,2,3,4,5,6,7,8,9,10]
F = map(my_func, my_list)
print(list(F))


# 실행결과
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
 * For loop를 돌리는 것과 동일한 결과를 출력하겠지만, 과정에 있어서 데이터를 병렬로 처리함으로 매우 빠른 속도로 처리가 가능

## MAP VS FOR Loop

1) MAP

```python
val = 100000
lst = [i for i in range(val)]

def abc(a):
    return a**2

%timeit map(abc, lst)


# 실행결과
154 ns ± 0.596 ns per loop (mean ± std. dev. of 7 runs, 10000000 loops each) 
```

2) For Loop

```python
val = 100000
lst = [i for i in range(val)]

def abc(a):
    tmp=[]
    for i in a:
        tmp.append(i)
    return tmp

%timeit abc(lst)


# 실행결과
6.72 ms ± 156 µs per loop (mean ± std. dev. of 7 runs, 100 loops each)
```

* 위에 결과와 같이 For 문을 수행 시켰을 때, 소요되는 시간이 압도적으로 큰것을 볼 수 있습니다.
* 따라서 처리할 데이터가 많아질수록 MAP을 이용해야합니다.