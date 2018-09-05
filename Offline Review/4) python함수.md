# Python 함수
*  사용자가 원하는 경우, 새로운 함수를 정의하여 사용할 수 있습니다.


## Lambda Function

* 인수는 여러개가 들어갈 수 있지만, 실행문은 단 하나뿐

```python
x = lambda a : a + 10    
   # x(a) = a + 10 이라는 의미로 사용되며, x(a)는 수학에서 f(a)와 동일하게 생각
print(type(x))
print(x(5))
   # x(5) = 5 + 10 = 15

# 실행결과
<class 'function'>
15
```

```python
x = lambda a, b : a * b
   # x(a,b) = a * b
print(type(x))
print(x(3,5)

# 실행결과
<class 'function'>
15
```



## 함수(Function)
 * 함수는 'def + 함수명'로 정의

1) 기본

```python
-------전역-------
def my_func():
	print("function")

-------메인-------
print(my_func())
my_func()


# 실행결과
function
```

2) Parameter

```python
-------전역-------
def my_func(parameter):
    print(parameter)

-------메인-------
my_func("안녕하세요")


# 실행결과
안녕하세요.
```

3) Default Parameter

```python
-------전역-------
def my_func(parameter = "안녕"):
	print(parameter)
	
-------메인-------
my_func("안녕하세요")
my_func()


# 실행결과
안녕하세요
안녕
```

* Default와 필수입력이 같이있는 경우<br>
필수 입력 영역을 앞에 적어 주는것이 기본
 
```python
-------전역-------
def my_func(para1, para2, para3 = "한국 ", para4 = "서울")
	print(para1 + para2 + para3 + para4)

-------메인-------
my_func("미국 ", "워싱턴 ", "중국 ", "베이징")
my_func("미국 ", "워싱턴 ", "대한민국 ")
my_func("미국 ", "워싱턴 ")


# 실행결과
미국 워싱턴 중국 베이징
미국 워싱턴 대한민국 서울
미국 워싱턴 한국 서울
```

4) 함수의 반환(return)

 * 함수에 전달된 파라미터에 의해서 계산된 결과를 출력하는 것이 아니라 반환해주는 것

```python
-------함수-------
def func(x, y):
	return x + y

-------메인-------
sum = func(5,10)
print(sum)


# 실행결과
15
```