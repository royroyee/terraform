# 사전지식

참고자료 : 테라폼으로 시작하는 IaC (한빛미디어)

### VPN(Virtual Private Network)
- 가상 사설망
- 네트워크를 분리하고 싶을때 가상의 망 VPN 을 사용
    - 실제로 같은 네트워크 상에 있지만 서로 다른 네트워크인 것처럼 동작


## VPC(Virtual Private Cloud)
독립적인 가상의 네트워크 공간으로 사용자의 설정에 따라 자유롭게 구성할 수 있는 공간을 의미
- 사용자는 서브넷, 라우팅 테이블, 게이트웨이 구성 등을 통해 사용자가 원하는대로 네트워킹 환경을 제어할 수 있다.


## ACL(Access Control List)
허가되지 않은 이용자가 라우터나 네트워크의 특정 자원을 접근하려고 하는 것을 차단한다.
- 트래픽 필터링과 방화벽을 구축하는데 가장 중요한 요소
- 라우터 인터페이스에 적용함으로써 특정 패킷을 필터링할 수 있고 발신지/목적지 주소, TCP/UDP 포트 번호 같은 사항들을 기반으로 허락과 거부를 할 수 있다.

### ACL 의 기능
1. 특정 사용자의 접근을 제한하고자 하는 경우
   - 수신한 패킷의 출발지 주소를 확인하여 네트워크에 접근할 수 있는 사용자와 그렇지 않은 사용자의 구분을 해주기 위해서 사용한다.
2. 특정 서비스의 이용을 제한하고자 하는 경우
   - Web 서비스를 막거나 Telnet 사용을 제한하는 등, 네트워크 별로 제한하고자 하는 프로토콜의 종류를 표시하여 통신 패킷을 필터링할 수 있다.
3. 라우팅 경로의 조정이 필요한 경우
   - Dynamic 방식을 사용하여 라우팅을 한 경우, 관리자가 원하는 대로 경로 조정이 되지 않은 경우에는 Access-List 를 사용하여 추가적인 조정이 가능하다.


## IaC
> 컴퓨터에서 읽을 수 있는 정의파일을 사용해 인프라나 서비스를 관리하고 프로비저닝하는 프로세스
- "실행 가능한 문서"
- 기존에 수동으로 작업하거나 이전에 사용되던 자도오하 도구로는 지속적으로 변경 사항을 관리할 수 없었던 단점을 극복할 수 있게 해줌

