![그래프](https://github.com/mkyoung24/Algorithm/assets/103173521/1416c023-88bb-4cc1-8eab-35acc38e2e36)


# 깊이 우선 탐색(DFS, Depth First Search)
- 자기 자신을 호출하는 순환 알고리즘의 형태를 지님(재귀 or 스택)
- 모든 노드를 방문하고자 할때, 사용
- 미로를 탐색할 때, 해당 분기에서 갈 수 있을 때까지 계속 가다가 더 이상 갈 수 없게 되면 다시 가장 가까운 갈림길(새로운 분기)로 돌아와서 다른 방향으로 다시 탐색을 진행하는 방법과 유사함
- 너비우선탐색(BFS)보다 더 간단함
- 검색 속도 자체는 너비우선탐색(BFS)에 디해서 느림
- 깊게 탐색

## DFS 수행 과정
1. 1번 노드에서 시작
2. 2, 5번 노드로 갈 수 있음
3. 숫자가 더 작은 2번 노드로 감(전략은 마음대로 설정)
4. 3,4번 노드로 갈 수 있음
5. 3번 노드로 감
6. 3번 노드에서 갈 수 있는 곳이 없음
7. 2번 노드로 돌아감
8. 4번 노드로 감
9. 4번 노드에서 갈 수 있는 곳이 없음
10. 2번 노드로 돌아감
11. 2번 노드에서도 더 이상 갈 수 있는 곳이 없음
12. 1번 노드로 감
13. ...
`결과 : 1 -> 2-> 3 -> 4 -> 5 -> 6 -> 7 -> 8 -> 9`

## :scroll: 문제
<https://github.com/mkyoung24/Baekjoon/tree/main/DFS>


## 너비 우선 탐색(BFS, Bread First Search)
- BFS는 재귀적으로 동작하지 않음
- BFS는 방문한 노드들을 차례로 저장한 후 꺼낼 수 있는 자료 구조인 큐를 사용함
- 시작 정점으로 부터 가까운 정점을 먼저 방문하고 멀리 떨어져 있는 정점을 나중에 방문하는 순회 방법
- 두 노드 사이의 최단 경로 혹은 임의의 경로를 찾고 싶을 때 이 방법을 사용함
- 넓게 탐색

## BFS 수행 과정
1. 1번 노드에서 시작
2. 2, 5번 노드로 갈 수 있음
3. 갈 수 있는 모든 경로를 큐에 삽입
4. 2번 노드에서 갈 수 있는 모든 경로를 큐에 삽입
5. 5번 노드에서 갈 수 있는 모든 경로를 큐에 삽입
6. 3, 4, 6, 9 노드에서 갈 수 있는 모든 경로를 순서대로 큐에 삽입
7. ....
`결과 : 1 -> 2 -> 5 -> 3 -> 4 -> 6 -> 9 -> 7 -> 8`

## :scroll: 문제
<https://github.com/mkyoung24/Baekjoon/tree/main/BFS>


>
- 시간 복잡도는 DFS, BFS 둘 다 O로 같음
- 일반적으로 BFS가 조금 더 빠름
- 일반적으로 경로의 특징을 저장해야 하는 경우에는 DFS, 최단 경로를 구하는데에는 BFS를 사용


***
## :file_folder: 출처
- <https://chb2005.tistory.com/76>
- <https://bbangson.tistory.com/42>
