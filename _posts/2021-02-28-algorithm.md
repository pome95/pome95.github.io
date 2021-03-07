---
title:  "알고리즘"  
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

## 알고리즘 이란?  
> 수학, 컴퓨터 과학, 언어학등 관련 분야에서 `어떠한 문제를 해결`하기 위해   
> `정해진 일련의 절차나 방법을 공식화한 형태`로 표현한 것  
>> 계산을 실행하기 위한 `단계적 절차`를 의미

---

## 조건
<br/>
좋은 알고리즘을 만들기위해서 아래와 같은 `조건`들이 필요하다.
* **입력**
  * 알고리즘은 0 또는 그 이상의 외부에서 제공된 자료가 존재한다.
* **출력**
  * 알고리즘은 최소 1개 이상의 결과를 가진다.
* **명확성**
  * 알고리즘의 각 단계는 명확하게 해서 애매함이 없어야한다.
* **유한성**
  * 알고리즘은 유한의 횟수로 실행되고 종료해야 한다.
* **효과성**
  * 알고리즘의 모든 연산은 유한한 시간에 수행할 수 있을 정도로 단순해야한다.

---
<br/>


## 성능 분석
<br/>

* **시간 복잡도**  
문제를 해결하는데 걸리는 `시간과 입력의 함수 관계`를 나타낸다.
  * $Big-O$ 표기법을 통해 `자료의 수 n`이 증가할 때 시간이 증가하는 패턴을 나타낸다.
  * $O(1) < O(log n) < O(n) < O(n log n) < O (n^2) < O(2^n) < O(n!)$  
  <br/>  
* **공간 복잡도**  
문제를 해결하는데 사용하는 `메모리의 크기`를 의미한다.
  * 총 공간 요구 = 고정 공간 요구 + 가변 공간 요구로 나타낸다.
  * $S(P) = c + Sp(n)$
    * 고정 공간 : 코드 저장, 변수,상수 등 알고리즘과 무관한 공간
    * 가변 공간 : 알고리즘 실행 중 동적으로 필요한 공간

---

## 표현
알고리즘을 표현 하는 4가지의 방법이 있다.
1. **자연어(natural language)**
  * 사람이 일상 생활에서 소통하기 위해 사용하는 언어  
  <br/>  
2. **프로그래밍 언어(programming language)**
  * 프로그램을 만들기 위해 작성하는 언어  
  <br/>  
3. **의사 코드(pseudo code)**
  * 프로그램 작성시 각 모듈이 작동하는 논리를 표현하는 언어  
  <br/>  
4. **순서도(flow language)**
  * 프로그램이나 작업의 진행 흐름을 순서에 따라 기호나 문자로 나타낸 도표
   
---