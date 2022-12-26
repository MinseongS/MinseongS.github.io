---
title:  "[CS면접] 알고리즘"
search: true
categories: 
  - cs-interview
tag:
  - cs-interview
  - algorithm
comments: true
last_modified_at: 2022-12-26
toc: true
toc_sticky: true
toc_label: "[CS면접] 알고리즘"
---

## 3. 알고리즘

### 버블소트, 힙소트, 머지소트, 퀵소트
버블소트는 서로 인접한 두 원소를 비교하여 정렬하는 알고리즘입니다. 0번 인덱스부터 n-1번 인덱스까지 n번까지의 모든 인덱스를 비교하며 정렬합니다. 시간복잡도는 O(n2)O(n2)O(n^2) 입니다.
![image](https://user-images.githubusercontent.com/75301269/209518081-c3e47051-3b48-4a0b-a6d8-6776359ebf66.png)
힙소트는 주어진 데이터를 힙 자료구조로 만들어 최대값 또는 최소값부터 하나씩 꺼내서 정렬하는 알고리즘입니다. 힙소트가 가장 유용한 경우는 전체를 정렬하는 것이 아니라 가장 큰 값 몇개만을 필요로 하는 경우입니다. 시간복잡도는 O(nlog2n)O(nlog2n)O(nlog_2n) 입니다.
![image](https://user-images.githubusercontent.com/75301269/209518117-cc7c7cd3-4aea-423a-a164-bbccee52dd05.png)
머지소트는 주어진 배열을 크기가 1인 배열로 분할하고 합병하면서 정렬을 진행하는 분할/정복 알고리즘입니다. 시간복잡도는 O(nlog2n)O(nlog2n)O(nlog_2n) 입니다.
![image](https://user-images.githubusercontent.com/75301269/209518171-a448d96b-76c6-405a-b639-6cae9becb0a1.png)
퀵소트는 매우 빠른 정렬 속도를 자랑하는 분할 정복 알고리즘 중 하나로 합병정렬과 달리 리스트를 비균등하게 분할합니다. 피봇을 설정하고 피봇보다 큰값과 작은값으로 분할하여 정렬을 합니다. 시간복잡도는 O(nlog2n)O(nlog2n)O(nlog_2n) 이며 리스트가 계속해서 불균등하게 나눠지는 경우 시간복잡도가 O(n2)O(n2)O(n^2) 까지 나빠질 수 있습니다.
![image](https://user-images.githubusercontent.com/75301269/209518205-526df160-72a4-4116-b964-d7f0674cee21.png)
삽입정렬은 두 번째 값부터 시작하여 그 앞에 존재하는 원소들과 비교하여 삽입할 위치를 찾아 삽입하는 정렬 알고리즘입니다. 삽입 정렬의 평균 시간복잡도는 O(n2)O(n2)O(n^2) 이며, 가장 빠른 경우 O(n)O(n)O(n) 까지 높아질 수 있습니다.
![image](https://user-images.githubusercontent.com/75301269/209518244-fe972e78-7832-4e39-86e1-09b34c3aba30.png)

### 정렬알고리즘 시간복잡도 비교
![image](https://user-images.githubusercontent.com/75301269/209518284-b6605619-744c-40e4-a74a-26cc1e9f1989.png)