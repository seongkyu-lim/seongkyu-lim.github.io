---
title: '알고리즘 문제를 풀 때, 파이썬에서 정수 입력값 받는 방법'
date: 2020-09-10
tags:
  - algorithms
  - python
---

#### Point

<b>첫번 째</b>로 input() 함수는 문자열로 입력받기 때문에 입력받을 때 정수로 자료형을 바꾸어주자.

<b>두번 째</b>로 많은 줄의 입력 데이터가 있을 시 빠르게 입력 받도록 하기위해 sys.stdin.readline을 사용하자.

입출력 속도 비교 : sys.stdin.readline > raw_input() > input()
<br>
<br>

### 첫번 째

#### 1. 한개 입력받는 방법

```python

a = int(input())

print(a)

#int()를 사용하여 input()으로 입력받은 입력값의 자료형을 string 에서 int로 바꾸어 줍니다.
```

#### 2. 여러개를 한줄에 입력받는 방법

```python

a, b = input().split()

#.split() 는 소괄호안의 문자를 기준으로 입력값을 나누어 받는다. 소괄호안에 아무 것도 없을 경우 공백을 기준으로 받는다.
# input().split()으로 받을 경우에는 int()를 사용하지 못한다. -> 해결법  : map method를 사용

a, b  = map(int, input().split())

# 입력받은 값들을 int로 형변환한다.

```

### 3. 2차원 배열 입력받는 방법.

```python

board = [[int(x) for x in input().split()] for y in range(n)]

#n 은 행의 개수를 의미한다. (세로줄)

```

<br>

### 두번 째

```python

from sys import\*

input = stdin.readline

# 위의 코드형식으로 선언하고 input() 사용하던대로 사용하면 빠르게 입력 받을 수 있다.

```
