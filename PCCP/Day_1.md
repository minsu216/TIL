# 문제를 해결하기 위한 해결방안

 어떻게 하면 아주 효율적으로 의견을 받을 수 있을까(문제)
 무언가를 가지고 문제를 푼다.? (알고리즘)
 데이터를 가지고 자료구조에 넣고 데이터를 깔끔하게 만들어 해결할거다 ( 미로찾기, 완전탐색 등등 ,체스도 포함)

 데이터를 통해 -> 자료 -> 엑셀에 정보를 저장( 이름 , 나이, 성별 등등 정보를 저장하게 된다.
 시각적인 정보로 파악 가능. 이름 나이 성별도 중요할 수도 있다. 변수 -> 어떤 데이터의 별명이라고 생각하면 된다. 어떤 데이터의 별명이라고 생각하면 된다. 변수는 Variable->바뀔 수 있는 것 별명
 변수를 가지고 저장할 것이다. Ex) Name -> 준이야 이름이 여러개 있으니까 name1 = Jun, name2 = Alex, name3 = ken -> 최적의 방법이다. 엄청 직관적이기 때문이다.

 Age1 -> 21, Age2 -> 28 .. 30 , Gender -> M or F 데이터의 사용 방법이라고 생각하면된다.
 Name1이라는 별명을 붙여서 첫번째 이름이라는 추상화된 별명을 Checking 
 방금까진 Jun 21나이 F라는 성별 ,Ken이라는 이름 존재 각각 따로 저장을 했다. 이 데이터에서 연관성 느낄 수 있다. (각 특징을 생각할 수 있다. or 집합)
 이름 나이 성별로 묶어보겠다.-> 이름이라는 공통적인 특징을 가짐, 변수 이름을 붙일 때는 고민을 많이 해야됨. Ex) name_1, name_2 이름이 여러개인걸 유추할 수 있다!!!

 names = [Jun, Ken, Alex] 등등 .. <- 여러개의 데이터를 저장할꺼야 라고 정한 것이 list라고 생각하면된다. 2단계의 과정을 거쳐야 될 것입니다.
 list는 순서를 가지고 있다. -> set or list or 기타 등등 여러개 있다. -> 그중에서 list 특징을 살펴보게 된다면

# list
- 여러개의 데이터를 저장한다.
- 순서를 가지고 있다.index -> 0, 1, 2, 3 ..

```python
names = ['jun','Alex','Ken']
names[0] #jun이된다.
```
```
사람과 컴퓨터간의 소통을 돕기위한 것이 Programming.
python이 사람과 가까운 언어이다.
C는 파이썬 보다 속도가 빠르다.
-> 내 마음대로 처리가능하나 많은 것을 처리해야된다.

파이썬은 편하게 적용가능. (사람 친화적)
```
Person1, Person2, Person3 등등.. person은 이름 방식이 필요하다.-> 0번째는 이름, 1번째는 나이, 2번째는 성별이다. 등등


```python
person1 = ['j',18,'m']
#dictionary -> 데이터를 key와 value로 묶은 것을 의미
#이름 나이 성별이라는 것으로 지정되어있다.
#하나 하나 하나 명시하는 것이 딕셔너리라고 하는 자료
```
```python
person1 = ['j',18,'m']
print(person1[0])

person1={
    name : 'jun'
    age : 18
    gender : 'm'
}

print(person1['name']) # 결과는 'jun'
#를 하나의 변수에 저장해서 사용할 수 있다.
#딕셔너리는 key로써 가져올 수 있다.
#문제점 -> person1 , person2, person3 등등
name1 ='jun'
name2= 'alex
names=['jun','alex']
```
```python
people = [{ 
    "name" : 'jun'
    "age" : 18
    "gender" : 'm'
    "flag" : 
},{
    "name" : 'alex'
    'age' : 23
    "gender" : 'm'
}]

people = [person1, person2]
#리스트의 원소에는 딕셔너리가 들어갈 수 있다는 사실!!
#리스트안에 딕셔너리라고하는 거대한 무언가가 들어갈 수 있다!!
```

```python
people ={
    'jun'_: { 'age' :18,
    'gender':'m
    },

    'alex' : {
        'age':23,
        'gender' : 'f'
    }
}
```
알고리즘 문제를 풀땐 주어진 데이터를 통해 문제를 해결
그러나 실제 데이터에선 자신만의 방법으로 문제 푼다.

```
J 18 M
A 23 F
C 28 -

엑셀의 시각적인 메트릭스 정보를 파이썬도 가능하다.
how : x,y두개의 메트릭스에서 사용 하나의 정보가 있을때
위치를 명확하게 표현하는 방식이다!!!

Matrix의 원하는 값을 가져오고 싶을때 지정가능하다.
이름, 나이, 성별 등 -> 프로그래밍 언어로써 사용가능!
how? -> 데이터를 저장하는 이유는 꺼내서 쓰기위해서
list는 인덱스로 딕셔너리는 키로!, 행렬은 행렬도 접근 가능하다. 몇 번째라고 하는건 무엇의 데이터를 가져와?
리스트로!
```
딕셔너리기때문에 데이터를 가져올 수 있다.

행렬도 가져올 수 있다.
```
M=
-> J 18 M
-> A 23 F
-> K 28 -

M[0] = J 18 M
M[1] = A 23 F
M[2] = K 28 -
M[0][0] = J로 표시된다.-> 행 0, 열 0
리스트를 만들고 만들면 엑셀처럼 사용가능한 2차원 리스트!
```
```
논리적인 판단 등에서
계속해서 뭔갈 판단해 나가고 있다.
- string, numeric, T,F로 나타내고있다 -> 이걸 Data Type
- numeric ->(실수, 정수) -> 왜 나눠져있나 -> 1.1 이라는 것을 표현 가능하다 10진법이란 것으로 1 + 0.1 표현
15300 -> 1*10^4 + 5*10^3 +3*10^2

X2^n + ... 9 = 2^3 + 2^0이다.
생략된건 0*2^2 + 0*2^1이다.
3*10^-1 , 2^-1 등등
2진수는 정수범위에서는 1 2 3 4 ... 표현이 쉽다.
```

```
string 1+1 = 2죠
왜 2라고 했냐면 -> 1이랑 +라는 기호랑 1이랑 0이라는 기호
컴퓨터는 ""가 들어있으면 무조건 문자열 표시
따라서 

```