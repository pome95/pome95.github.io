---
title:  "해시 충돌(Hash_Collision) (1)"  
excerpt: "Hash Collision With Python"
toc:  true
toc_sticky:  true
toc_label:  바로가기
header:
        teaser:  /assets/img/data/hash_collision.png


categories:
  - Computer Engineering
tags:
  - Data Structure
---
<br/>

저번에는 [`해시 테이블 기본 구현`](https://pome95.github.io/computer%20engineering/hashtable(2)/)에 대해 간단히 다루어 보았다.<br/>
이번에는 `해시 충돌`에 대해 알아보도록 하자 <br/>


## 해시 충돌 (Hash Collision)
> 해시 충돌이란 해시 함수가 `서로 다른 두개의 입력 값`에 대해  
> `동일한 출력 값`이 한 주소에 매핑이 되는 상황을 말한다.

---

## 충돌 해결 (Collision Resolution)
여러가지 충돌 해결 기법이 있지만 그중 2가지를 다뤄보려한다.  
<br/>

1. [체이닝 (Chaining) 기법](https://pome95.github.io/computer%20engineering/chaining/)
>저장 공간 내에 데이터를 삽입시 같은 값에 의해 충돌이 발생할 경우   
연결 리스트를 생성하여 데이터를 뒤에 연결해주는 방식.
>>복잡한 계산식이 필요없고 삭제, 삽입이 간단하나  
>>연결 리스트 자체의 오버헤드가 있다.

2. 선형 탐색 (Linear Probing) 기법
>개방 주소법(Open Addressing)의 하나로 해시 충돌이 일어날 경우  
>다음 저장 공간에 데이터를 삽입하는 방식.
>>체이닝처럼 연결 리스트가 없기에 포인터가 필요없지만  
>>특정 위치에만 데이터가 몰리는 현상이 생길수 있다.