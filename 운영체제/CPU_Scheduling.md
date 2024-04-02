jihyeon-yu

# 비선점과 선점 스케줄링

## 비선점(Non-preemptive)

- 프로세스가 CPU 소유권을 스스로 포기하는 방식
- 프로세스를 강제로 중지시키지 않음
- 컨텍스트 스위칭 부하가 적음

## 선점(Preemptive)

- 운영체제가 프로세스를 강제로 중지시키고 CPU를 다른 프로세스에 할당하는 방식

# 스케줄링 알고리즘

## 선입 선처리 스케줄링 (FCFS: First Come First Served)

- 비선점
- 준비 큐에 들어온 순서대로 처리
- 프로세스 대기 시간이 길어질 수 있음

![Alt text](./img/jihyeon-yu-FCFS.jpg)

## 최단 작업 우선 스케줄링 (SJF: Shortest Job First)

- 비선점
- CPU 사용이 짧은 프로세스를 먼저 실행하여 호위 효과 방지

## 라운드 로빈 스케줄링 (RR: Round Robin)

- 선점
- 타임 슬라이스를 정하여 순서대로 CPU를 할당
- 타임 슬라이스가 크면 호위 효과 발생, 작으면 문맥교환 오버헤드 발생

![Alt text](./img/jihyeon-yu-RR.jpg)

## 최소 잔여 시간 우선 스케줄링 (SRF: Shortest Remaining Time First)

- 선점
- 최단 작업 우선 스케줄링과 라운드 로빈 스케줄링의 결합
- 남은 작업 시간이 가장 적은 프로세스를 먼저 실행

## 우선순위 스케줄링

- 비선점
- 프로세스에 우선순위를 부여하여 높은 우선순위의 프로세스를 먼저 실행
- 기아 문제를 유발할 수 있으며, 에이징 기법으로 해결 가능

## 다단계 큐 스케줄링 (Multilevel Queue)

- 선점
- 우선순위 별로 여러 개의 준비 큐를 사용하여 처리
- 큐 간의 이동이 불가능하여 기아 현상 발생 가능

## 다단계 피드백 큐 스케줄링 (Multilevel Feedback Queue)

- 선점
- 다단계 큐 스케줄링의 발전된 형태
- 큐 간의 이동이 가능하여 기아 현상을 완화
- CPU 스케줄링 방식으로 알려져있음

![Alt text](./img/jihyeon-yu-feedbackqueue.jpg)
