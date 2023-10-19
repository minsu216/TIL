# Data type 
- 1 -> 숫자 or 문자을 명시해야 컴퓨터한테 인식 가능?
- 숫자나 문자 or Boolean 등이 있다.(boolean은 T or F => if문에서 중요하다.)
- 정수는 2진수, 실수는 2진수 표현 x
- 특이한 방식으로 저장, 데이터를 다룰때 중요!
- 문자 -> ''안에 존재


비교 연산자

의미

<
미만 (작다)

<=
이하 (작거나 같다)

>
초과 (크다)

>=
이상 (크거나 같다)

==
같다

!=
같지 않다

```python
print(True and True)   # True
print(True and False)  # False
print(False and True)  # False
print(False and False) # False

print(True or True)    # True
print(True or False)   # True
print(False or True)   # True
print(False or False)  # False

print(not True)        # False
print(not False)       # True
```