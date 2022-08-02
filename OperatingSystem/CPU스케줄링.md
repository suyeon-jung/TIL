# CPU 스케줄링

## 방식

1. **비선점형 스케줄링** : 일단 CPU를 할당받으면 프로세스가 종료되거나 I/O 등의 이벤트가 있을 때까지 CPU를 반환하지 않는다. 
2. **선점형 스케줄링** : 현재 수행중인 프로세스의 남은 burst time보다 더 짧은 CPU burst time을 가지는 프로세스가 CPU를 할당받는 방식

<br>

## 비선점형 스케줄링
1. **FCFS(First Come First Served)**
   <br>먼저 온 순서대로 처리 → convoy effect(소요시간이 긴 프로세스가 먼저 도착하여 효율 낮추기)

2. **SJF(Shortest Job First)**
   <br>CPU burst time이 짧은 프로세스에 먼저 할당 → starvation(소요시간이 긴 프로세스는 영원히 할당받지 못할 수 있음)

3. **Priority Scheduling**
   <br>우선순위가 가장 높은 프로세스에 CPU 할당

<br>

## 선점형 스케줄링
1. **SRTF(Shortest Remaining Time First)**
   <br>새로운 프로세스가 도착할 때마다 새로운 스케줄링

2. **Priority Scheduling**
   <br>우선순위가 가장 높은 프로세스에 CPU 할당

3. **Round Robin**
   <br>각 프로세스는 동일한 길이의 할당 시간(`Time Quantum`)을 갖게 된다. 적당한 time quantum을 설정하는 것이 중요하다.