# Review - Online

## List
List는 C언어에서 배열을 대신하는 개념일 수 있습니다.<br>


<strong>1. 리스트 생성</strong>
```python
# 리스트는 여러가지 방법으로 생성할 수 있습니다.
a = list()
b = []
c = [1,2,3]

# 위의 어떤 방법도 가능합니다.
```

<strong>2. 리스트의 특징</strong>
* 리스트는 중복을 허용합니다.
* 중간에 하나를 지울 경우 자동으로 빈칸을 채우게 됩니다.
* 리스트 변수는 데이터가 아닌 리스트의 주소를 갖고있습니다.

<strong>3. 리스트 함수</strong>
>
> <strong>1) 정렬(sort)  </strong>
> ```python
> a = [4,8,3,1,10,7,6,2,9,5]   # 리스트 생성
> a.sort()
> print(a)
>
> # 실행결과
> [1,2,3,4,5,6,7,8,9,10]
> ```
>
> <strong>2) 삽입(append)  </strong>
> ```python
> a = [1,2,3,4,5]
> a.appent(3)
> print(a)
> 
> # 실행결과
> [1,2,3,4,5,3]   # 제일 마지막에 추가됩니다.
> ```
> 
> <strong>3) 뒤집기(reverse)  </strong>
> ```python
> a = [1,2,3,4,5]
> a.reverse()
> print(a)
> 
> # 실행결과
> [5,4,3,2,1]
> ```
> 
> <strong>4) 위치 검색(index)  </strong>
> ```python
> a = [1,3,5,7,9]
> print(a.index(5))   # index함수 괄호 안에있는 값의 위치를 반환합니다.
> 
> # 실행결과
> 2
> 
> # 만약 리스트에 찾고자하는 값이 없다면 애러
> ```
> 
> <strong>5) 삽입(insert)  </strong>
> ```python
> a = [1,2,3,4,5]
> a.insert(1,10)   # 1번 자리에 10의 값을 넣습니다. 나머지 값은 뒤로 밀리게 됩니다.
> print(a)
> 
> # 실행결과
> [1,10,2,3,4,5]
> ```
> 
> <strong>6) 삭제(remove)  </strong>
> ```python
> a = [3,3,1,2,3,4,5]
> a.remove(3)   # remove함수의 괄호 안에있는 값을 제거합니다. 중복이 있는경우 가장 앞에있는 값을 제거합니다.
> print(a)
> 
> # 실행결과
> [3,1,2,3,4,5]
> ```
> 
> <strong>7) POP  </strong>
> ```python
> a = [1,2,3,4,5]
> print(a.pop())   # pop함수는 리스트의 가장 마지막 값을 리턴합니다. 리스트에서 가장 마지막 값은 제거됩니다.
> 
> # 실행결과
> 5
> 
> # 만약 리스트가 비어있는 상태로 pop을 하게되면 애러
> ```
> ---
> 
<br><br><br>
# Tuple
리스트의 '상수'같은 개념으로 생각해보면 좋을꺼 같습니다.

<strong>1. 튜플(Tuple) 생성</strong>
```python
# 튜플(tuple)은 여러가지 방법으로 생성할 수 있습니다.
a = tuple()
b = ()
c = (1,2,3)
d = 1,2,3
e = 1,   # 원소가 하나인 튜플(tuple)은 꼭 ',(쉼표)'를 붙여야합니다.

# 위의 어떤 방법도 가능합니다.
```

<strong>2. 튜플(Tuple) 특징</strong>
 * Tuple은 리스트와 유사하지만, Immutable(수정 불가)의 특징을 갖습니다.
 * 수정이 불가능하기 때문에 리스트에서 사용했던 함수들 대부분이 사용 불가능합니다.


<br><br><br>
# Set
집합(set)은 중복을 허용하지 않는 리스트라고 볼 수 있습니다.

<strong>1. 집합(Set) 생성</strong>
```python
# 집합(Set)은 여러가지 방법으로 생성할 수 있습니다. 그러나 주의해야합니다.
a = set()
b = {1,2,3}
c = set([1,2,3,4,5])   # 리스트를 집합으로 변경하여 넣을 수 있습니다.
# <주의> d = {}로 생성이 불가능합니다. 내용이 없는 {}은 dict를 의미합니다.
```

<strong>2. 집합(Set) 특징</strong>
 * 집합(Set)은 중복을 허용하지 않습니다.

<strong>3. 집합(Set) 응용</strong>
```python
# Set을 이용하여 리스트를 제거할 수 있습니다.
a = [1,1,2,2,3,3,4,4,5,5]
a = set(a)
print(a)

# 실행결과
[1,2,3,4,5]
```

<br><br><br>
# Dict
자료형에 있어서 가장 중요한 개념입니다.

<strong>1. 사전(Dict) 생성</strong>
```python
a = dict()
b = {}
c = {1:'a', 2:'b'}   # 앞에 숫자가 key, 뒤의 영어가 value가 됩니다.
d =	dict(apple="green", banana="yellow", cherry="red")

d["damson"] = "purple"
# 이미 생성된 dict에 위와 같이 'damson'이라는 key와 'purple'이라는 value를 추가할 수 있습니다.
# 'damson'이라는 Key가 존재할 경우 기존의 damson의 Value값을 'purple'로 덮어쓰게됩니다.
```

<strong>2. 사전(Dict) 특징</strong>
 * 사전(Dictionary)이 이름과 의미로 구성되어 있듯이 Key와 Value로 구성되어있습니다.
 * Key는 중복된 값을 허용하지 않습니다.
 * Value의 값으로는 값 뿐만아니라, 리스트와 같은 다른 자료형들이 올 수 있습니다.
 * 해시를 이용하기 때문에 Key에 대한 Value를 바로 알 수 있습니다.


