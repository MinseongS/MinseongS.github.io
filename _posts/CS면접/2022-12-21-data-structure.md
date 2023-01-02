---
title:  "[CS면접] 자료구조"
search: true
categories: 
  - cs-interview
tag:
  - cs-interview
  - data-structure
comments: true
last_modified_at: 2022-12-21
toc: true
toc_sticky: true
toc_label: "[CS면접] 자료구조"
---

# 자료구조

## Array
- Array는 메모리에서 연속적이고 할당된 크기만큼 저장하는 자료구조입니다.
- 한 번 할당한 크기를 변경할 수 없습니다.
- 인덱스를 이용하여 접근하기 때문에 요소에 O(1)로 빠르게 접근할 수 있습니다.
- 중간 데이터 추가, 삭제를 하면 모든 데이터들을 옮겨줘야하기 때문에 시간복잡도가 O(n)입니다.


## Dynamic Array
- Array는 한 번 할당된 크기가 고정되어 있는 반면, Dynamic Array는 데이터가 들어오면 resize를 통해 유동적으로 size를 조절하는 데이터 자료구조입니다.
- Array와 유사하게 접근과 할당이 O(1)로 빠르고, append를 하면서 resize 하는 과정이 있기때문에 append의 시간복잡도는 amortized O(1)이라 부릅니다.
- java 의 ArrayList, python의 List 가 Dynamic Array에 해당됩니다.
  - <a href="https://sabarada.tistory.com/6" target="_blank">java ArrayList</a>
  - <a href="https://seoyeonhwng.medium.com/%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%A6%AC%EC%8A%A4%ED%8A%B8-%EB%82%B4%EB%B6%80-%EA%B5%AC%EC%A1%B0-f04847b58286" target="_blank">python List</a>


## LinkedList
- Node라는 구조체로 이루어져있고, Node에 데이터와 다음 Node의 주소를 저장합니다. Node의 리스트가 메모리에 물리적으로는 연속적이지 않지만, Node의 주소를 통해 논리적으로 연결된 형태의 자료구조입니다.
- 데이터를 찾기 위해 head node 부터 순차적으로 확인을 하기 때문에 데이터 접근 시간 복잡도는 O(n)입니다.
- 데이터 추가와 삭제의 경우 node의 앞뒤 주소만 변경하면 되기 때문에 O(1)로 가능합니다.

## Dynamic Array와 LinkedList차이
Dynamic Array는 데이터들이 메모리에서 물리적으로 연결된 배열의 형식을 취하고 있지만, LinkedList는 자료의 주소값으로 서로 연결된 형식을 가지고 있습니다. 이러한 구조에 의해 둘은 각각의 장단점을 가지고 있습니다.

- Dynamic Array
   - 원하는 데이터에 무작위로 접근할 수 있다.
   - 리스트의 크기가 제한되어 있으며, 리스트의 크기를 재조정하는 것은 많은 연산이 필요하다.
   - 데이터의 추가/삭제를 위해서는 임시 배열을 생성하여 복제하고 있어 시간이 오래 걸린다.
   
- LinkedList
   - 리스트의 크기에 영향 없이 데이터를 추가할 수 있다.
   - 데이터를 추가하기 위해 새로운 노드를 생성하여 연결하므로 추가/삭제 연산이 빠르다.
   - 무작위 접근이 불가능하며, 순차 접근만이 가능하다.

## Queue
- queue는 선입선출 FIFO(First In First Out)의 자료구조입니다.
- 데이터 추가, 삭제 시간복잡도는 O(1)입니다.
- cache 구현, 프로세스 관리, BFS(너비우선탐색) 등에 사용되는 자료구조입니다.


## Stack
- stack은 후입선출 LIFO(Last In First Out)의 자료구조입니다.
- 데이터 추가, 삭제 시간복잡도는 O(1)입니다.
- 방문기록 저장, DFS(깊이우선탐색) 등에 사용되는 자료구조입니다.

## Heap
- 완전 이진 트리로 구성된 자료구조입니다.
- 부모와 자식의 우선순위 비교를 통해 데이터를 정렬합니다.
- head node 에 우선순위가 가장 높은 데이터가 오게 됩니다.
- 데이터 추가, 삭제 시간 복잡도는 O(logn)입니다.
- priority queue, heap sort 등에 사용되는 자료구조입니다.


## Hash Table

- Hash Table은 (Key, Value)로 데이터를 저장하는 자료구조입니다.
- Key값에 해시함수를 적용해 고유한 index를 생성하여 그 index에 저장된 값을 꺼내오는 구조입니다.

![image](https://user-images.githubusercontent.com/75301269/208910462-2a72b95c-25b0-4a97-8196-930785ce5e80.png)

- hash function만 계산하면 데이터에 바로 접근할 수 있기 때문에 데이터 검색의 시간복잡도는 O(1)입니다. 
- 해시의 index값이 충돌이 발생한 경우 충돌된 index값에 대해 연결된 데이터들을 조회하여 원하는 값을 조회하기 때문에 O(N)까지 증가할 수 있습니다.

## Hash Table collision
해결 방법
- open addressing : 정해진 규칙에 따라 데이터가 비어있는 곳을 찾아서 해결합니다. linear probing, quadratic probing, double hashing 등이 있습니다.
- separate chaining : collision이 발생한 위치에 linked list에 노드를 추가하여 데이터를 저장합니다.