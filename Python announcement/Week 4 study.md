# 파이썬의 입출력

---

## 📌 1. 함수

- `def`  함수를 만들 때 사용하는 예약어

```python
def 함수_이름(매개변수):
    수행할_문장1
    수행할_문장2
    ...
```

- `return`  함수 실행 결과를 밖으로 전달할 때 사용

```python
def add(a, b):
    return a + b
print(add(4, 5))     # 9

def kkk(a,b):
    return a + b
print(kkk(4, 5))     # 9
```

- 여러 개의 입력값을 받는 함수는  `*매개변수`  사용

```python
def add(*a):
    result = 0
    for b in a:
         result += b
    return result
print(add(1, 2, 3, 4, 5, 6, 7, 8, 9, 10))       # 55
```

**⭐ 문제: 마지막 줄에 `range` 를 써서 결과값 55를 만들어라.**

- 키워드 매개변수, `kwargs`
- `**매개변수` **→ 딕셔너리 (Key=Value)**

```python
def aaa(**kwargs):
    print(kwargs)
aaa(name='hwan', age=24)    # {'name': 'hwan', 'age': 24}
```

- `lambda` 예약어

```python
add=lambda a, b: a + b
result = add(4, 5)
print(result)                # 9

def add(a, b):
    return a + b
print(add(4, 5))             # 9
```

**문제 221**

입력된 문자열을 역순으로 출력하는 print_reverse 함수를 정의하라.

```python
def print_reverse(string):
    print(string[::-1])
print_reverse("python")       # nohtyp
```

---

## 📌 2. 사용자 입출력

- `input` 함수

```python
a=input("숫자를 입력하세요: ")    # 숫자를 입력하세요: 5 ⭠ 5 입력
print(a)                         # 5
```

- `print` 알아보기

```python
print("H" "i")        # Hi   ⭠ 큰따옴표로 둘러싸인 문자열은 + 연산과 동일

print("H", "i")       # H i  ⭠ 문자열 띄어쓰기는 쉼표
```

- 한 줄에 결과값 출력

```python
for i in range(100):
    print(i, end=' ')   # 0 1 2 3 ... 97 98 99
```

---

**⭐ 문제**

**숫자를 여러 개 입력받아서, 짝수만 제곱해서 리스트로 반환하는 함수**를 만들어보자.

- 함수는 이름이 `process_numbers`여야 함
- 입력은 **갯수 제한 없이 정수들을 여러 개 받을 수 있어야 함**
- 홀수는 무시하고, **짝수만 제곱해서** 결과 리스트에 담아야 함
- 결과 리스트는 **오름차순으로 정렬**해서 반환

🧠 힌트

- `*args` 사용해서 여러 개 숫자 받기
- `for` 반복문으로 순회
- `if` 조건문으로 짝수 판별 (`x % 2 == 0`)
- `sorted()` 함수로 정렬

---