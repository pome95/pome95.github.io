---
title:  "삽입 정렬 (Insertion Sort)"  
excerpt: "Insertion Sort With Python"
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
지난 시간까지 [`선택 정렬`]({{ site.url }}{{ site.baseurl }}/computer%20engineering/selection/)에 대해 간단히 다루어 보았다.<br/>
이번에는 다양한 정렬 알고리즘 중 `삽입 정렬`에 대해 알아보도록 하자 <br/>

## 삽입 정렬 (Insertion Sort)
> 다음과 같은 순서를 반복하며 정렬하는 알고리즘
>   1. 두 번째 인덱스부터 시작한다.
>   2. 해당 인덱스 값보다 앞의 값과 비교한다. (처음엔 1개)
>   3. 해당 인덱스의 값이 큰 경우 그 뒤에 삽입한다.
>   4. 인덱스를 넘어가면서 반복하며 정렬한다.

---

### 핵심 코드
선택 정렬은 다음과 같은 코드를 베이스로 구현이 가능하다.

```python
for 반복횟수 in range(데이터 길이 -1):
    for 기준 데이터 in range(반복횟수 ,0, -1):
        if 기준 데이터 > 앞의 값:
            swap(기준 데이터, 앞의 값)
        else:
            반복문 끝(break)
```

### 구현
위의 코드를 베이스로 구현을 해보았다.  
```python
import random

def insertion_sort(data):
    for index in range(len(data)-1):
        for stand in range(index+1, 0,-1):
            if data[stand] < data[stand -1]:
                data[stand], data[stand-1] = data[stand-1], data[stand]
            else:
                break
    return data
```
* 변수
    * stand : 기준점(비교 기준)
    * index : 반복을 위한 변수
    <br/>  

* data에 랜덤값을 넣기위해 import random
* 2번째를 기준으로 시작하여 앞과 비교
    * 기준값이 앞보다 작을 경우 교체
    * 기준값이 더 클 경우 반복 해제
* 기준점을 바꾸고 위 과정을 반복하여 정렬

---

#### 임의의 데이터 추가
```python
data_list = random.sample(range(100),20)
data_list
insertion_sort(data_list)
```

#### 결과
0부터 99까지의 숫자 중에 랜덤으로 20개의 숫자를 뽑아  
data_list에 넣었고 삽입 정렬이 진행되었음을 확인할 수 있다. 

[47, 27, 13, 74, 31, 95, 16, 64, 96, 6, 39, 42, 17, 68, 45, 20, 44, 84, 87, 56]  

[6, 13, 16, 17, 20, 27, 31, 39, 42, 44, 45, 47, 56, 64, 68, 74, 84, 87, 95, 96]  

---