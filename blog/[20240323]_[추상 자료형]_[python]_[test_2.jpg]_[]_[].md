# Bag 추상 자료형
### 데이터: 중복된 항목을 허용하는 자료의 모임. 항목들 사이에 순서는 없지만 서로 비교할 수는 있어야 함.  
### 연산
* insert(e): 가방에 항목 e를 넣는다.
* remove(e): 가방에 e가 있는지 검사하여 있으면 이 항목을 꺼낸다.
* contains(e): e가 들어있으면 True를 없으면 False를 반환한다.
* count(): 가방에 들어 있는 항목들의 수를 반환한다.

### 코드 1.1: Bag의 주요 연산을 일반 함수로 구현 예


```python
def contains(bag, e):
    return e in bag
```

bag에 항목e가 있는지 검사하는 함수. 파이썬의 in 연산자를 이용했는데, e가 bag에 있으면 True를 없으면 False를 반환함


```python
def insert(bag, e):
    bag.append(e)
```

bag에 새로운 항목 e를 넣는 함수. 파이썬 리스트의 append() 연산을 이용해 리스트의 맨 뒤에 e를 추가함


```python
def remove(bag, e):
    bag.remove(e)
```

bag에서 항목 e를 삭제하는 함수. 파이썬 리스트의 remove() 연산을 이용해 구현함


```python
def count(bag):
    return len(bag)
```

bag에 들어 있는 항목의 수를 반환하는 함수. 파이썬 내 내장함수 len()을 이용함

* e in bag은 bag에 e가 있으면 True, 없으면 False를 반환한다.
* bag.append(e)은 리스트 bag의 맨 뒤으 항목 e를 추가한다.
* bag.remove(e)는 리스트 bag에서 항목 e를 삭제한다.
* len(e)은 리스트 bag에 들어있는 항목의 수를 반환한다.
* print()는 화면 출력 함수이다.

### 코드 1.2: Bag을 활용한 테스트 프로그램


```python
myBag = []
```

bag을 위한 새로운 배열을 만듦. 자료구조의 데이터를 저장하는 공간


```python
insert(myBag, '휴대폰')
insert(myBag, '지갑')
insert(myBag, '손수건')
insert(myBag, '빗')
insert(myBag, '자료구조')
insert(myBag, '야구공')
```

새로운 bag인 myBag에 '휴대폰', '지갑', '손수건', '빗', '자료구조', '야구공'을 순서대로 삽입함


```python
print('가방속의 물건:', myBag)
```

    가방속의 물건: ['휴대폰', '지갑', '손수건', '빗', '자료구조', '야구공']
    

현재의 myBag의 내용을 화면에 출력함


```python
insert(myBag, '빗')
remove(myBag, '손수건')
```

myBag에 '빗'을 추가로 삽입하고, '손수건'을 삭제함


```python
print('가방속의 물건:', myBag)
```

    가방속의 물건: ['휴대폰', '지갑', '빗', '자료구조', '야구공', '빗']
    

변경된 myBag 내용을 화면에 출력

### 도전 코딩!
1. Bag의 추상 자료형에 numOf(e) 연산을 추가하려고 한다. numOf(e)는 Bag에 들어 있는 항목 e의 수를 반환하는데, 만약 Bag에 e가 없다면 0을 반환한다. 일반함수로 추가할 이 연산을 구현하라


```python
def numOf(bag, e):
    if e in bag:
        return bag.count(e)
    else:
        return 0
```
