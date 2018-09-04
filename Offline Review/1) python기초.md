# Review - Online

* 네덜란드의 [Guido van Rossum](https://en.wikipedia.org/wiki/Guido_van_Rossum)에 의해 만들어진 [python](https://namu.wiki/w/Python)
* Interpreter 방식 : script language

## python 기본 함수
* python3 기준으로 작성되었습니다.<br><br>

<strong>1. 출력함수</strong>
```python
# 출력함수
print("Hello, World!")
print("한글테스트")   #python3부터는 한글 인코딩 문제 X

# 실행결과
Hello, World!
한글테스트
```

<strong>2. 변수사용</strong>        
```python
# 변수 a, b를 지정하고 출력
a=3
b=4
print(a+b)

# 실행결과
7
```

<strong>3. 변수삭제</strong>        
```python
# 변수삭제
del a   # a라는 이름의 변수를 삭제
print(a)   # 삭제한 a를 출력할 경우

# 실행결과
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
<ipython-input-5-89e6c98d9288> in <module>()
----> 1 b

NameError: name 'a' is not defined
# a라는 변수가 정의되지 않았다는 오류가 발생하는 것을 볼 수 있음
```
<strong>4. 조건문</strong>        
```python
# 변수 정의
a = 30
b = 20
c = 10
# 조건문(if ~ (elif) ~ else 순서)
if a<b:    # 조건이 '참'일 경우 아래 들여쓰기 된 부분을 실행 틀리면 elif로 넘어감
print("a가 b보다 더 큰 값입니다.")
elif b<c:    # 마찬가지로 조건이 '참'일 경우 들어쓰기 된 부분이 실행
print("b가 c보다 더 큰 값입니다.")
else:    # 위의 모든 조건이 '거짓'일 경우 다음 부분이 실행됨
print("c가 가장 큰 값입니다.")

# 실행결과
c가 가장 큰 값입니다.
```

<strong>5. 주석</strong>        
```python
# 주석 사용하는 방법
# 한 줄을 주석처리하는 경우 '#'을 사용
# 여러줄을 주석처리하는 경우 """~"""을 사용
"""
주
석
처
리 
"""
# 주석처리된 부분은 실행되지 않습니다.
```


<strong>6. 문자열 변수</strong>        
```python
# 일반 숫자변수와 사용이 동일
str1 = "안녕"
str2 = "하세요"
print(str1 + str2)

# 실행결과
안녕하세요



# 문자 + 숫자(애러 상황)
str3 = "문자"
num = 10
print(str3 + num)

# 실행결과
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-12-47467449490f> in <module>()
1 str3 = "문자"
2 num = 10
----> 3 print(str3 + num)

TypeError: must be str, not int



# 문자 + 숫자(애러 해결)
print(str3 + str(num))    # 숫자변수를 문자열을 의미하는 str로 감싸줌으로썬 함수내에서 문자열처럼 인식하도록 만들어줌
# 위와같이 변수의 타입을 바꿔주는 것을 캐스팅이라고 함
# 실행결과
문자10
```

<strong>7. 변수 SWAP</strong>        
```python
# 다른 언어와 다르게, swap이 매우 간단
a = 10
b = 20
print(a, b)
a, b = b, a
print(a, b)

# 실행결과
10 20
20 10
```

<strong>8. 반복문</strong>        
```python
# 반복문은 크게 for과 while문이 있음
1) For문
# for 반복문은 일반적으로 반복 횟수가 정해져 있음
# 0~9까지를 출력
for i in range(10):    #range(10)이라는 것에 의해서 i라는 값에 0~9까지 값이 순서대로 들어감
print(i)

# 실행결과
0
1
2
3
4
5
6
7
8
9

# range 사용방식
* 0~x까지 반복할 경우
for i in range(x+1)

* x~y까지 반복할 경우
for i in range(x, y+1)



2) While문
# while문은 조건에 따라서 반복 횟수가 정해짐
# while(조건)의 형태로 사용됨
# 0~9까지를 출력
i = 0
while(i != 10):
print(i)
i = i+1    # i += 1로도 표현 가능

# 실행결과
0
1
2
3
4
5
6
7
8
9



3) while문 무한반복
# while문의 조건부분에 True(항상 '참')을 넣어줌
i = 0
while(True):
print(i)
i += 1

# 실행결과
0
1
2
3
...
강제 중단시까지 계속 출력



4) 반복문의 종료
# break함수 이용
i = 0
while(True):
if i==10:
break
print(i)
i += 1

# 실행결과
0
1
2
3
4
5
6
7
8
9
```


<strong>기타</strong>        
```python
1) 한글변수
# python은 한글변수를 지원함   ---> 그래도 가급적 사용하지 말자.
# 권장은 변수는 소문자로 시작
가 = "안녕"
나 = "하세요"
print(가+나)

# 실행결과
안녕하세요
```
