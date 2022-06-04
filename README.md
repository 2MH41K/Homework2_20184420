# Homework2_20184420
homework2_20184420

+ 리눅스 명령어에서...
  + top
  > **top 명령어에 대한 설명**
  > 
  > top 명령어는 리눅스 시스템이 실행되고 난 후부터 지금까지의 시간과 시스템에 로그인된 사용자 수 그리고 시스템 부하율을 표시하는 명령어인 uptime의 결과를 가장 상단에 표시해주며, 그 아래로 프로세스 수치, CPU 정보, 메모리 정보를 보여주고, 각 프로세스 별 부하율과 상태를 표시해줍니다. 
  > 
  >> **사용예시**
  
  >>`top -b`
  >> -b옵션을 사용해 순간의 정보를 확인하는 모습
  
  >>`top -n 2`
  >> -n 옵션을 사용하여 top 실행 주기를 2번 하도록 하는 모습

  + ps
  > **ps 명령어에 대한 설명**
  > 
  > ps 명령어는 프로세스의 현재 상태를 출력합니다. 기본 필드 이외에도 다양한 옵션을 지원하고, top 명령어와의 가장 큰 차이점은
  > **ps는 ps한 시점에 proc에서 검색한 cpu 사용량을 출력하고, top은 proc에서 일정 주기로 합산해 cpu 사용률을 출력합니다.**

  >>**사용예시**
  
  >>`ps -e`
  >> 모든 프로세스를 출력

  >>`ps -f`
  >> 풀 포멧으로 출력 (uid, pid, ppid, TTY 등 정보를 보여줌)

  + jobs
  > **jobs 명령어에 대한 설명**
  > 
  > jobs 명령어는 작업이 중지된 상태, 백그라운드로 진행중인 작업 상태, 변경되었지만 보고되지 않은 상태 등을 표시합니다.
  >
  >>**사용예시**
  >
  >>`jobs -l`
  >> state 필드 앞에 프로세스 ID를 출력
  
  >>`jobs -p %v`
  >> v로 시작하는 모든 프로세스 ID


  + kill
  > **kill 명령어에 대한 설명**
  >
  > kill 명령어는 프로세스에 종료 시그널을 보낸다. 시스템이 예기치 않은 문제가 생긴 프로세스를 종료시킬 수 있다. **만일 kill 명령으로 종료되지 않는 프로세스는 -9 옵션을 사용해서 강제로 종료하면 됩니다.**
  >
  >>**사용예시**
  >
  >>`kill 2518`
  >> 2518의 PID를 가진 프로세스를 종료

  >>`kill -HUP 2518`
  >> 2518의 PID를 가진 프로세스를 종료 후 다시 재실행
  
  리눅스 명령어 요약
  
  
  |명령어|사용법|설명|
  |---|---|---|
  |top|top[옵션]|프로세스 상황|
  |ps|ps[옵션]|프로세스 상태 보기|
  |jobs|jobs[옵션]|현재 세션 작업 상태|
  |kill|kill[옵션]|프로세스 종료|
  
+ vim 에디터에서 매크로 사용방법
  >**사용방법**
  
  >`1.매크로 실행방법(명령모드에서) q[NAME]`

  >`2.등록된 매크로를 실행시키는 방법 @[NAME]`
  
  >**응용법**

  > @[NAME] 앞에 숫자@[NAME]을 하면 숫자에 들어간 만큼 매크로를 실행하게 됩니다.

  |사용법|설명|
  |---|---|
  |q[NAME]|매크로 시작|
  |...|매크로 입력|
  |q|매크로 종료|
  |@[NAME]|매크로 실행|
  |[number]@[NAME]|매크로 여러번 실행|
  |* :u|작업 되돌리기|
  |@@|방금 실행한 매크로 실행|
