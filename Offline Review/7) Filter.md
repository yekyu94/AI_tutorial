# Filter
 * 필터 함수는 MAP과 동일하게 r = filter(func, seq) 형태를 갖습니다.
 * 함수의 출력이 True일 경우만을 구할때 사용합니다.


## Filter 예제

```python
seq = [1,2,3,4,5,6,7,8,9,10]

def my_func(x):
	if x < 5:
		return False
	else:
		return True

result = filter(my_func, seq)
print(list(result))


# 실행결과
[5, 6, 7, 8, 9, 10]
```


# ZIP
 * 두 개 이상의 리스트의 요소를 묶어, 하나의 리스트로 만들어 줍니다.

## ZIP 예제
```python
a = ("John", "Charles", "Mike")
b = ("Jenny", "Christy", "Monica", "Vicky")
c = ("감자", "고구마", "길동", "피클")
result = list(zip(a, b, c))

print(result)


# 실행결과
[('John', 'Jenny', '감자'),
 ('Charles', 'Christy', '고구마'),
 ('Mike', 'Monica', '길동')]
``` 