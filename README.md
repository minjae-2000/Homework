# **리눅스 명령어**


  > ## 1) top 명령어
  >> ### 1-1 ) 개념
  >>        top 명령어는 현재 OS의 상태를 나타내주는 명령어 입니다. 
  >>        메모리 사용량, CPU 사용량 등을 나타내주며 top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여줍니다. 
  >>        이를 통하여 리눅스를 사용하는 디바이스의 성능이나 리눅스 서버의 성능을 체크할 때 매우 유용합니다.
  >> <p align="center"> <img src="https://user-images.githubusercontent.com/80958395/172034056-07b2679c-f21f-4e9e-8619-38281783cf69.PNG"  alt="top 명령어 실행 시"  width="600" height="300"/> 
  
   <p align="center"> top 명령어 실행 결과
                                                                                                                                         
 >> ### 1-2) 구성      
 >>         top은 크게 요약영역 과 세부영역으로 나눠어져있습니다.
 >>> ### - 요약영역 
 >>> <p align="center"> <img src="https://user-images.githubusercontent.com/80958395/172034799-e976ab49-8800-4eec-9a2c-916951029081.png"  alt=" 요약영역"  width="600" height="100"/>
 >>>   
 >>>        요약 영역은 top에서 상단에 위치하고 있습니다.
 >>>        이 부분은 전체 프로세스가 OS에 대해서 리소스를 어느정도 차지하고 있는지를 알려줍니다. 
 >>>        
 >>>        첫 부분 부터 설명드리자면
 >>>
 >>>            12:41:13 : 현재 시간 
 >>>            0 user : 한명의 사용자가 접속
 >>>            load average : 부하율
 >>>            tasks 에:10 total은 10개의 프로세스가 가동중
 >>>            1 running 1개의 프로세스가 실행중 
 >>>            9 sleeping : 9개의 프로세스가 대기중
 >>>            0 stopped : 0개의 프로세스가 멈춤
 >>>            0 zombie : 0개의 프로세스가 좀비상태
 >>>
 >>>            ---- CPU ----
 >>>            %us  : 유저 레벨에서 사용하고 있는 CPU의 비중
 >>>            %sy : 시스템 레벨에서 사용하고 있는 CPU비중
 >>>            %id : 유휴 상태의 CPU 비중
 >>>            %wa : 시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중
 >>>
 >>>            ---- Memory ----
 >>>            Mem:   12736.9 total, 11117.5 free, 559.2 used,  1027.2 buffers 
 >>>            전체 물리적인 메모리, 사용되지 않는 여유 메모리(free), , 사용중인 메모리(used) 버퍼된 메모리(buffers)
 >>>            Swap:  4096 total,    0 used,  4096 free,  11532.1 cached 
 >>>            전체 스왑 메모리, 사용중인 스왑 메모리, 남아있는 스왑메모리, 캐싱메모리
 >>>
 >>> ### - 세부영역 
 >>> <p align="center"> <img src="https://user-images.githubusercontent.com/80958395/172035144-776c32ca-3e45-4116-a5bc-2c1261adf02b.png"  alt=" 세부영역"  width="600" height="200"/>
 >>>
 >>>            PID : 프로세스 ID 
 >>>            (PID)USER : 프로세스를 실행시킨 사용자 
 >>>            IDPRI : 프로세스의 우선순위 (priority)
 >>>            NI : NICE 값. 일의 nice value값이다. 마이너스를 가지는 nice value는 우선순위가 높음.
 >>>            VIRT : 가상 메모리의 사용량(SWAP+RES)RES : 현재 페이지가 상주하고 있는 크기(Resident Size)
 >>>            SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합
 >>>            S : 프로세스의 상태 [ S(sleeping), R(running), W(swapped out process), 
 >>>            Z(zombies) ]%CPU : 프로세스가 사용하는 CPU의 사용율
 >>>            %MEM : 프로세스가 사용하는 메모리의 사용율
 >>>            COMMAND : 실행된 명령어
 >>>  
 >> ### 1-3) 옵션
 >>>
 >>> |옵션|설명|
 >>> |------|---|
 >>> | - k|프로세스  kill|
 >>> | - a|메모리 사용량에 따라 정렬|
 >>> | - b| Batch 모드 작동|
 >>> | - c|명령행/프로그램 이름 토글|
 >>> | - d|지연 시간 간격|
 >>> | - H |스레드 토글|
 >>> | - i |유휴 프로세스 토글|
 >>> | - m | VIRT/USED 토글|
 >>> | - M | 메모리 유닛 탐지|
 >>> | - n |반복 횟수 제한|
 >>> | - p |PID를 모니터|
 >>> | - s |보안 모드 작동|
 >>> | - S |누적 시간 모드 토글|
 >>> | - u |사용자별 모니터링 : -u somebody|
 >>> | - U |사용자별 모니터링 : -U somebody|
 >>> | - v |version|
 >>>
 > ## 2) kill 명령어
