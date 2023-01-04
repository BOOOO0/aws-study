# EC2 리눅스 웹서버 생성하기

## EC2 원격접속

- SSH 프로토콜을 사용해 리눅스 인스턴스에 원격으로 연결하거나 RDP 프로토콜을 사용해 윈도우 인스턴스에 원격으로 연결할 수 있습니다.

- SSH는 터미널, 파워셸 등의 CLI를 통해 접속하고 RDP는 윈도우의 원격 데스크탑 연결 프로그램을 사용합니다.

- EC2 Instance Connect는 AWS에서 제공하는 소프트웨어이며 리눅스 인스턴스에 연결이 가능합니다.

- AWS Systems Manager Session Manager 기능을 사용해서 리눅스, 윈도우 인스턴스에 연결도 가능합니다. Session Manager를 사전에 별도로 구성을 해야 사용할 수 있습니다.

## 서버 생성하기

- EC2 Instance Connect를 사용해 접속을 하면 아마존 리눅스 AMI의 CLI가 나타납니다. EC2 인스턴스를 생성해서 실제로 서버를 구성하고 서버에 접속해보겠습니다.

- CLI에 루트 계정으로 변경하기 위한 명령어를 입력합니다. `sudo su`

- 먼저 패키지 매니저 yum의 업데이트를 해줍니다. `yum update -y`

- 그 후 httpd 서버를 설치해줍니다. httpd는 아파치 하이퍼텍스트 전송 프로토콜 (HTTP) 서버 프로그램입니다. `yum install httpd -y`

- 설치된 httpd 서버를 실행해줍니다. `service httpd start` `chkconfig httpd on`

- 그 후 인스턴스의 IP주소나 도메인 네임을 주소창에 쳐서 접속을 하면 서버가 생성된 기본 화면을 볼 수 있습니다.
