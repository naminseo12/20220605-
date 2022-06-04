# 20220605 오픈소스SW

## top 

**현재 OS의 상태를 나타내주는 CLI 어플리케이션**

시스템의 상태를 전반적으로 가장 빠르게 파악 가능

메모리 사용량, CPU 사용량 등을 나타내줌

### top 명령어

|옵션|설명| 
|----|----|
|shift + p|CPU 사용률 내림차순으로 정렬한다.|
|shift + m|메모리 사용률 내림차순으로 정렬한다.|
|shift + t|프로세스가 돌아가고 있는 시간 순으로 정렬한다.|
|-k|입력 후 PID 번호를 입력하면 kill한다.|
|-f|sort field 선택 화면, q를 누르면 원하는 순서대로 정렬한다.|
|-a|메모리 사용량에 따라 정렬한다.|
|-b|Batch 모드로 작동|
|-1|CPU 코어별로 사용량을 보여준다.|

![top명령어](https://user-images.githubusercontent.com/106607389/171990130-fd8d4f32-7b8d-4431-832b-872f2e796964.PNG)

## ps

**현재 실행중인 프로세스의 목록을 보여줌**

### 옵션

|옵션|설명| 
|----|----|
|-e|실행중인 모든 프로세스의 정보를 출력한다.|
|-f|프로세스에 대한 자세한 정보를 출력한다.|
|-u [사용자이름]|특정 사용자에 대한 모든 프로세스의 정보를 출력한다.|
|-p [pid]|pid(프로세스 아이디)로 지정한 프로세스의 정보를 출력한다.|
|-u|프로세스 소유자의 이름, cpu 사용량, 메모리 사용량 등 정보를 출력한다.|
|-a|터미널에서 실행한 프로레스의 정보를 출력한다.|
|-x|실행중인 모든 프로세스의 정보를 출력한다.|

![ps 명령어](https://user-images.githubusercontent.com/106607389/171991064-76b7348b-d991-49de-9ac6-fc5313fe4472.PNG)


> top과 ps의 차이점

top는 proc에서 일정 주기로 합산해서 cpu 사용량, ps는 ps한 시점에 proc에서 검색한 cpu 사용량을 출력한다. 

## jobs

**jobs는 작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경되었지만 보고되지 않은 상태 등을 표시**

### 백그라운드 작업 상태

|작업 상태|설명| 
|----|----|
|Running|작업이 계속 진행중임|
|Done|작업이 완료되어 0을 반환함|
|Done(code)|작업이 종료되었으며 0이 아닌 코드를 반환함|
|Stopped|작업이 일시 중단|

### 옵션

|옵션|설명| 
|----|----|
|-l|프로세스 그룹 id를 state 필드 앞에 출력한다.|
|-n|프로세스 그룹 중에 대표 프로세스 id를 출력한다.|
|-p|각 프로세스 id에 대해 한 행씩 출력한다.|
|command|지정한 명령어를 실행한다.|

## kill

**대기 프로세스를 종료시키는 명령어**

### 옵션

|옵션|설명| 
|----|----|
|[pid]|pid가 [pid]인 프로세스를 종료한다.|
|-s [pid]|전달할 시그널의 종류를 지정한다.|
|-l|시그널로 사용할 수 있는 시그널 이름들을 보여준다.|
|-1(숫자 1) [pid]|-HUP 프로세스를 재활성화한다.|
|-9 [pid]|프로세스를 강제로 종료시킨다.|

## 매크로 사용 방법

1. q + <알파벳> : 기록 시작

2. 반복을 원하는 동작 실행

3. q : 기록 종료

|---|설명| 
|----|----|
|@<알파벳>|매크로 실행|
|@@|방금 실행한 매크로 실행|
|<숫자>@|<숫자>만큼 매크로 실행|


