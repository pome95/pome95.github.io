---
title:  "재귀 호출"  
excerpt: "Algorithm"
toc:  true
toc_sticky:  true
toc_label:  바로가기
header:
        # teaser:  /assets/img/data/datastructure.png

 
categories:
  - Computer Engineering
tags:
  - Algorithm

use_math: true

---

## 재귀 호출 이란?  
> 함수 내부에서 함수가 자기 자신을 또 다시 호출하는 행위를 의미  
>> 함수를 호출한 후 그 함수가 끝날때까지 다음의 명령이 실행되지 않고,  
>> 종료조건이 꼭 포함이 되어야한다.  
>> 함수 => 하나의 작업을 수행하기 위해 독립적으로 설계된 프로그램 코드의 집합 

---

## 형태
재귀 호출을 하는 함수는 2가지의 일반적인 형태를 가진다.

1. 
```python
def function(입력):
    if 입력 > 일정값:
        return function(입력보다 작은값)
    else:
        return 일정값, 입력값, 또는 특정값 (종료)
```

2. 
```python
def function(입력):
    if 입력 <= 일정값:
        return 일정값, 입력값, 또는 특정값 (종료)
    function(입력보다 작은값)
    return 결과값
```

---

### 예시
10개의 숫자를 변수 num에 넣고 각각의 숫자를 팩토리얼 계산해보았다.  

```python
def factorial(num):
    if num <= 1:
        return num

    return num * factorial(num-1)

for num in range(10):
    print (factorial(num))
```

Result => 0 1 2 6 24 120 720 5040 40320 362880

---