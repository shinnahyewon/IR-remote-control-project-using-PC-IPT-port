# IR-remote-control-project-using-PC-IPT-port
IR remote control project using PC IPT port


수행기간 : 2023.04.05. ~ 2023.04.09.
담당역할 : -적외선 센서를 이용하여 리모컨을 만들어 SonyTV를 조작
수행목표 : -적외선 센서의 펄스를 이해하고 실습
사용 기술 : C+, MFC
세부수행내용 :

■ 기능 설명
1) 리모컨 동작원리
 프린터 포트는 병렬 통신방식으로, 무선 통신 소자를 사용하는 경우 직렬 통신 기술
을 적용해야 한다. 모든 IR 리모컨에서 신호들은 리시버에 시그널을 전송하기 위해
IR의 펄스를 전송한다. 이 IR LED는 30kHz~40kHz의 주파수 범위에서 전송한다.
이 신호는 이진코드 형태로 IR LED를 통하여 time과 length를 사용하여 전송된다.

2) 회로 구성
 - LM555 타이머 : 적외선 통신 주파수 대역인 30~40㎑의 구형파를 발생하기 위한
기준 펄스 발생기로 약 68㎑의 신호를 발생
 - 7474 플립플롭 : 555타이머의 주파수를 2분주 시키는 기능과 펄스의 0과 1구간
을 통제하기 위한 회로로 1번 clear 단자를 프린터 포트의 D0에 연결하여 프로그
램의 제어를 받도록 구성
 - inverter 7405 : 작성된 펄스는 송신용 IR-LED에 연결되는데, 출력전류를 높이기
위하여 open collector 타입 사용

![image](https://github.com/shinnahyewon/IR-remote-control-project-using-PC-IPT-port/assets/161293023/3871176c-9f4a-4dba-8baa-60b921837f59)

