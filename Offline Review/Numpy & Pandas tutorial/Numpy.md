# Numpy

 * Numpy는 과학적 계산을 위한 파이썬 패키지입니다.

> N차원 배열 계산<br>
> sophisticated (broadcastig) functions
> C/C++등과 통합가능<br>
> 선형대수학, 푸리에변환, 난수표현등이 가능합니다.

<br>
### 현재 설치된 numpy의 버전 확인
 
```python
import numpy as np

print(np.__version__)


# 실행결과
1.14.3
```

<br>
### numpy sample
```python
import numpy as np
x = np.array([1,2,3])

print(type(x))
print(x.dtype)
print(x)


# 실행결과
<class 'numpy.ndarray'>
int64
[1 2 3]
```
 * 리스트와 같이 보이지만, 타입을 찍어보면 numpy.ndarray 인것을 확인할 수 있습니다.
 * numpy에서는 datatype을 '변수'.dtype로 확인할 수 있습니다.

<br>
### DataType
```python
import numpy as np
x = np.array([1,2,3,4], dtype='float32')

print(x)


# 실행결과
[1. 2. 3. 4.]    # 쉼표가 아니라 .(dot)입니다.
```
 * numpy 배열을 만들때, 직접 데이터 타입을 적어줄 수 있습니다. 위에서는 float(실수형)으로 정해줬기 때문에, 실행결과에 수소점이 표시된 것을 볼 수 있습니다.

<br>
### 행과 열
```python
import numpy as np
x = np.ones((3,5), dtype=float)

print(x)


# 실행결과
[[1. 1. 1. 1. 1.]
 [1. 1. 1. 1. 1.]
 [1. 1. 1. 1. 1.]]
```
 * 행(row) + 열(column)
 * 행은 가로줄, 열은 새로줄을 의미합니다.
 * 위의 결과는 3행 5열이라고 할 수 있습니다.
 * 해설할 때에는 5개의 요소집합 3개가 묶여있다고 생각하면 됩니다.
 * 2차원 이상에서도 동일합니다.

<br>
### ArrayRange
 * 파이썬의 일반 range와 유사합니다.

```python
import numpy as np
a = np.arange(10)
print(a)

a = a[::-1]    # slicing 가능
print(a)


# 실행결과
[0 1 2 3 4 5 6 7 8 9]
[9 8 7 6 5 4 3 2 1 0]
```

<br>
### 기본 메소드

` x = np.ones((3, 5), dtype=float) `

   : 3x5 행렬을 모두 1로 채워라

` np.full((3, 5), 3.14) `

   : 3x5 행렬을 모두 3.14로 채워라

` np.linspace(0, 1, 5) `
   
   : 0~1까지 5개의 요소를 만들어라
   
<br>
### 난수(random number) 생성
 * 의사난수

1) 0~1사이의 난수

`np.random.random((3,3))    # 3x3`

2) 표준정규분포 ~N(0,1)    -> 평균 0, 분산 1
`np.random.normal(0, 1, (3, 3))    # 3x3`

3) 0~10사이의 난수(정수)
`np.random.randint(0, 10, (3, 3))    # 3x3`

4) 항등행렬

`np.eye(3)    # 3x3`

5) 초기화 안된 배열

`np.empty(3)    # 3x3`


<br>
### numpy reshape
 * 행렬의 모양을 바꿔줍니다.

```python
import numpy as np
N1 = np.arange(16)
N2 = N1.reshape(4,2,2)		# 만들고 싶은 행렬의 형태 입력
N3 = N1.reshape(4, -1)		# 행은 4로, 나머지는 자동으로

print("N1 \n", N1)
print("\nN2 \n", N2)
print("\nN3 \n", N3)


# 실행결과
N1 
 [ 0  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15]

N2 
 [[[ 0  1]
  [ 2  3]]

 [[ 4  5]
  [ 6  7]]

 [[ 8  9]
  [10 11]]

 [[12 13]
  [14 15]]]

N3 
 [[ 0  1  2  3]
 [ 4  5  6  7]
 [ 8  9 10 11]
 [12 13 14 15]]
```


<br>
### More
1) 행렬의 모양알기

```python
import numpy as np

a = np.array([[1,2,3],
				 [4,5,6]])		# 2x3행렬
print(a.shape)


# 실행결과
(2, 3)
``` 

2) Transpose

 * 행과 열의 위치를 바꿔줍니다.

```python
import numpy as np

a = np.array([[1,2,3],
				 [4,5,6]])		# 2x3행렬
print(a)
print(a.T)
print(a.transpose())


# 실행결과
[[1 2 3]
 [4 5 6]]	# 원래 모양

[[1 4]
 [2 5]
 [3 6]]		# transpose
 
[[1 4]
 [2 5]
 [3 6]]		# transpose
```

3) 기타 예제

```python
print(np.ones((2,3,4),dtype=np.int16))
print(np.ones((2,3,4),dtype=np.int16).shape)
print(len(np.ones((2,3,4),dtype=np.int16)))
print(np.ones((2,3,4),dtype=np.int16).ndim)
print(np.ones((2,3,4),dtype=np.int16).size)


# 실행결과
[[[1 1 1 1]
  [1 1 1 1]
  [1 1 1 1]]

 [[1 1 1 1]
  [1 1 1 1]
  [1 1 1 1]]] 
  
(2, 3, 4)

2

3

24
```

4) 연산 예제

```python
a = np.array([1,2,3])
b = np.array([(1.5,2,3), (4,5,6)], dtype = float)
print(a)
print(b)


# 실행결과
[1 2 3]
[[1.5 2.  3. ]
 [4.  5.  6. ]]
 
 
1) a - b
 
 array([[-0.5,  0. ,  0. ],
       [-3. , -3. , -3. ]])
  
       
2) a == b

 array([[False,  True,  True],
       [False, False, False]])
       
       
3) b.sum()

 21.5
 
 
4) b.sum(axis=0) 와 b.sum(axis=1)

 array([5.5, 7. , 9. ])		# 행단위 덧샘
 array([6.5, 15. ])			# 열단위 덧샘

5) b.cumsum(axis=1)

 array([[ 1.5,  3.5,  6.5],
       [ 4. ,  9. , 15. ]])


6) b.mean()
 
 3.5833333333333335
 
 
7) np.vstack((a,b))

 array([[1. , 2. , 3. ],
       [1.5, 2. , 3. ],
       [4. , 5. , 6. ]])


8) np.column_stack((a,d)) == np.c_[a,d]
 a = array([1, 2, 3])
 d = array([10, 15, 20]) 일때,
 
 결과
 : array([[ 1, 10],
       [ 2, 15],
       [ 3, 20]])
 
 
 9) np.row_stack((a,d)) == np.r_[[a,d]]
 결과
 : array([[ 1,  2,  3],
       [10, 15, 20]])

```