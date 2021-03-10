---
title:  "선택 정렬 (Selection Sort)"  
excerpt: "Selection Sort With Python"
toc:  true
toc_sticky:  true
toc_label:  바로가기
header:
        # teaser:  /assets/img/data/stack.png


categories:
  - Computer Engineering
tags:
  - Algorithm
---
<br/>
지난 시간까지 [`버블 정렬`]({{ site.url }}{{ site.baseurl }}/computer%20engineering/bubble/)에 대해 간단히 다루어 보았다.<br/>
이번에는 다양한 정렬 알고리즘 중 `선택 정렬`에 대해 알아보도록 하자 <br/>


## 선택 정렬 (Selection Sort)
> 다음과 같은 순서를 반복하며 정렬하는 알고리즘
>   1. 주어진 데이터 중, 최솟값을 찾는다.
>   2. 해당 최솟값을 데이터 맨 앞에 위치한 값과 교체한다.
>   3. 교체한 맨 앞을 제외한 그 다음부터 동일한 방법으로 반복한다.

---

### 핵심 코드
선택 정렬은 다음과 같은 코드를 베이스로 구현이 가능하다.

```python
for 고정 in range(데이터 길이 -1):
    lowest = stand
    for index in range(고정 index+1, 데이터 길이ㅣ):
        if data[lowest] > data[index]:
            lowest = index
    swap(앞 데이터, 뒤 데이터)
```

---

### 구현
위의 코드를 베이스로 구현을 해보았다.  
```python
import random

def selection_sort(data):
    for stand in range(len(data) - 1):
        lowest = stand
        for index in range(stand + 1, len(data)):
            if data[lowest] > data[index]:
                lowest = index
        data[lowest], data[stand] = data[stand], data[lowest]
    return data
```
* data에 랜덤값을 넣기위해 import random
* 작은 값을 찾아 앞과 바꾼다.
* 인덱스를 뒤로가며 교체를 바꿔가며 정렬

---

#### 임의의 데이터 추가
```python
data_list = random.sample(range(100),20)
data_list
selection_sort(data_list)
```

#### 결과
0부터 99까지의 숫자 중에 랜덤으로 20개의 숫자를 뽑아  
data_list에 넣었고 선택 정렬이 진행되었음을 확인할 수 있다. 

[39, 43, 63, 10, 97, 24, 96, 64, 59, 65, 93, 82, 44, 84, 0, 53, 88, 33, 98, 80]  

[0, 10, 24, 33, 39, 43, 44, 53, 59, 63, 64, 65, 80, 82, 84, 88, 93, 96, 97, 98]  

---
