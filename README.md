![자료구조](https://github.com/mkyoung24/Algorithm/assets/103173521/ff773e34-3ae8-4929-906f-2d07848a2d54)

# 선형 구조
- 데이터를 저장하기 위한 기본적인 형태로 데이터가 '일렬로 나열'되어 있을 뿐만 아니라 데이터 간에 순서가 있고 논리적으로 이어져 있는 구조


## 배열(Arrays)
![배열](https://github.com/mkyoung24/Algorithm/assets/103173521/6a3e2d96-565f-4b93-a2f5-5608779b607d)
- 동일한 자료형의 데이터들이 같은 크기로 나열되어 순서를 갖고 있는 집합
- 논리적 저장 순서와 물리적 저장 순서가 일치하기 때문에 인덱스로 해당 원소에 접근함
- 정해진 크기의 메모리를 먼저 할당 받아 사용하여, 정적인 자료 구조로 기억 장소의 추가가 어렵고
  데이터 삭제 시 데이터가 저장되어 있던 기억 장소는 빈 공간으로 남아 있어 메모리 낭비 발생


## 연결 리스트(Linked List)
![연결 리스트](https://github.com/mkyoung24/Algorithm/assets/103173521/b6ef2c8d-eb2f-49d2-8ede-3e77e9d04633)
- 자료를 연속적으로 배열 시키지 않고 자료가 추가될때마다 메모리를 할당 받음
- 각 원소들은 이전, 다음 위치를 기억하여 삽입, 삭제 하므로 동적인 크기를 가짐
- 논리적 위치와 물리적 위치가 다름
- index로 찾아가는 배열보다 순차적으로 위치를 찾아감으로써 소요되는 시간이 큼


### 연결 리스트와 배열의 차이점
||배열|연결 리스트|
|:---:|:---:|:---:|
|**장점**|값마다 인덱스를 가지기 때문에 탐색에 유리|데이터를 삽입 또는 삭제할때 노드만 바꿔서 연결해주면됨, 크기가 가변적|
|**단점**|값마다 인덱스를 가지기 때문에 삽입이나 삭제에 불리함, 크기가 정해져 있어 가득 차면 사용할 수 없음|데이터의 조회가 힘듬|

## 스택(Stack)
![스택1](https://github.com/mkyoung24/Algorithm/assets/103173521/dcbcdfd6-66d9-4ee5-a016-58af97cce731)
- 데이터를 일시적으로 쌓아두기 위한 자료구조 중 하나
- 후입선출(LIFO, Last-In-First-Out)

|주요 용어|설명|
|:---:|:---:|
|**Top**|삽입과 삭제가 일어나는 위치|
|**Push**|스택의 맨 위(top)에 데이터를 추가하는 연산|
|**Pop**|스택의 맨 위(top)에서 데이터를 삭제하고 반환하는 연산|
|**Peek**|스택의 맨 위에 있는 데이터를 조회하는 연산|


## 큐(Queue)
![큐1](https://github.com/mkyoung24/Algorithm/assets/103173521/0a12255e-7aca-4743-8331-5fa3794d9223)
- 선형 구조의 형태이며 데이터를 일시적으로 쌓아두기 위한 자료구조 중 하나
- 선입선출(FIFO, First-In-First-Out)

|연산|설명|Java 제공 메서드|
|:---:|:---:|:---:|
|**Enqueue**|큐의 맨 뒤(rear)에서 데이터를 추가하는 연산|add(E e), offer(E e)|
|**rear**|큐의 맨 뒤에 위치한 데이터를 가리키는 포인터|remove(), poll()|
|**front**|큐의 맨 앞에 위치한 데이터를 가리키는 포인터|element(), peek()|
|**Dequeue**|큐의 맨 앞에 위치한 데이터를 가리키는 포인터||


## 덱(Deque)
![덱5](https://github.com/mkyoung24/Algorithm/assets/103173521/2b9210c6-e0d2-4ac0-9ad1-e30d920c1683)
- 스택과 큐의 기능을 모두 가지고 있는 자료구조
- 양쪽 끝에서 삽입과 삭제가 가능함
- 선입선출(FIFO)과 후입선출(LIFO) 개념이 모두 적용됨
  

### 큐, 스택, 덱 요약
|분류|큐(Queue)|스택(Stack)|덱(Deque)|
|:---:|:---:|:---:|:---:|
|**정의**|FIFO|LIFO|양쪽 끝에서 삽입과 삭제가 가능한 자료구조|
|**삽입/삭제**|삽입은 enqueue, 삭제는 dequeue|삽입은 push, 삭제는 pop|addFirst, addLast, removeFirst, removeLast|
|**활용 예시**|대기열, 버퍼(Buffer)|함수 호출(call stack), 수식 계산|양방향 큐, 회문판별, 최대값/최솟값 검색|
|**장점**|데이터의 순서가 중요한 작업에 적합|구현이 쉽고, 메모리 관리가 용이|양쪽 끝에서 삽입과 삭제가 가능|
|**단점**|큐의 크기가 고정되어 있으면 데이터가 가득 차면 더 이상 삽입이 불가능|데이터 접근이 어렵고, 중간에 있는 데이터에 접근하려면 맨 위의 데이터부터 차례로 꺼내야 함|메모리 사용량이 큼|


***
## :file_folder: 출처
- <https://jinijana.tistory.com/32>
- <https://uni.rejoice-it.com/entry/JAVA-%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0-%EB%8B%A8%EC%88%9C%EA%B5%AC%EC%A1%B0-%EC%84%A0%ED%98%95%EA%B5%AC%EC%A1%B0-%EB%B9%84%EC%84%A0%ED%98%95%EA%B5%AC%EC%A1%B0-1>
- <https://adjh54.tistory.com/135>
