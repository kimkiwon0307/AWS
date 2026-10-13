# AWS
<details>
   <summary><h2>1장 AWS란?</h2></summary>

### 클라우드 컴퓨팅이란?
1.  AWS는 클라우드 컴퓨팅을 인터넷을 통해 컴퓨팅, 스토리지, 데이터베이스 같은IT 리소스를 필요할 때 제공받고 사용량에 따라 비용을 지불하는 방식
2. 온프레미스는 서버를 직접 구매하고 운영
3. 클라우드는 필요한 IT 자원을 필요할 때 빌려 사용
4. 서버:EC2, 스토리지:S3, EBS, 데이터베이스:RDS, 네트워크:VPC

### 클라우드 컴퓨팅 이점
1. 초기 투자 비용을 줄일 수 있다.
2. 용량을 미리 정확하게 예측할 필요가 줄어든다. -> Auto Scaling 개념
3. 빠르게 구축할 수 있다.
4. 데이터센터 관리 부담이 줄어든다.
5. 확장성이 좋다.
6. 전 세계에 서비스를 배포하기 쉽다.

### 클라우드 컴퓨팅 서비스 유형
1. 어디까지 클라우드 사업자가 관리하고 어디부터 사용자가 관리하느냐
2. IaaS : Infrastructure as a Service : 인프라를 서비스로 제공 : AWS가 서버를 빌려주고, 서버 안의 많은 부분은 내가 관리한다.
3. PaaS : Platform as a Service : 플랫폼까지 제공해주는 방식 : IaaS보다 사용자가 관리할 영역이 줄어든다.
4. SaaS : Software as a Service : 완성된 소프트웨어를 서비스로 사용 : 사용자는 서버나 OS를 관리하지 않는다. 소프트웨어를 사용한다.

### 클라우드 구축 모델
1. 클라우드를 어디에 어떻게 구축하느냐에 따른 구분
2. Public Cloud : AWS, Azure, GCP 같은 클라우드 사업자의 인프라를 여러 고객이 사용하는 형태
3. Private Cloud : 특정 조직을 위해 전용으로 사용하는 클라우드 환경
4. Hybrid Cloud : 온프레미스 + Public Cloud를 함께 사용하는 방식

### AWS 소개
1. AWS = Amazon Web Services 이다.
2. Compute : EC2 : Elastic Compute Cloud : AWS에서 가장 대표적인 가상 서버 서비스
3. Lambda : 서버를 직접 만들어 관리하지 않고 코드를 실행할 수 있는 서비스 : Serverless
4. VPC : Virtual Private Cloud : AWS 안에 만드는 나만의 가상 네트워크
5. ELB : Elastic Load Balancing : 여러 서버에 요청을 분산
6. Route 53 : AWS의 DNS 서비스
7. EBS : Elastic Block Store : EC2에 연결해서 사용하는 가상 디스크
8. S3 : Simple Storage Service : 파일을 객체 형태로 저장하는 Object Storage
9. EFS : Elastic File System : 여러 EC2가 동시에 사용할 수 있는 공유 파일 시스템
10. RDS : Relational Database Service : AWS의 관리형 관계형 데이터베이스 서비스
11. IAM : Identity and Access Management : 누가 무엇을 할 수 있는가? 를 관리하는 서비스
12. CloudWatch : AWS 자원의 상태를 모니터링하는 서비스

### AWS 과금 체계
1. AWS의 기본적인 과금 철학은 Pay-as-you-go 사용한 만큼 지불이다.

### 확인문제
# AWS 1장 확인문제 + 정답

## 1. 클라우드 컴퓨팅이란 무엇인가요?

- **답:** 인터넷을 통해 서버, 스토리지, 네트워크, 데이터베이스 같은 IT 자원을 필요할 때 빌려 사용하고, 사용한 만큼 비용을 지불하는 방식입니다.

---

## 2. 온프레미스와 클라우드의 가장 큰 차이는 무엇인가요?

- **답:** 온프레미스는 회사가 서버와 네트워크 장비를 직접 구매하고 운영하지만, 클라우드는 AWS 같은 클라우드 사업자의 IT 자원을 빌려 사용합니다.

---

## 3. 클라우드에서 필요에 따라 서버를 늘리거나 줄일 수 있는 특징은 무엇인가요?

- **답:** 확장성(Scalability)과 탄력성(Elasticity)입니다. 트래픽 증가에 따라 자원을 늘리고, 감소하면 다시 줄일 수 있습니다.

---

## 4. IaaS, PaaS, SaaS는 무엇을 기준으로 구분하나요?

- **답:** 클라우드 사업자와 사용자가 각각 어디까지 관리하는지를 기준으로 구분합니다.

---

## 5. EC2는 IaaS, PaaS, SaaS 중 어디에 가장 가깝나요?

- **답:** IaaS입니다. AWS가 서버 인프라를 제공하고 사용자가 OS, 프로그램, 애플리케이션 등을 관리합니다.

---

## 6. IaaS → PaaS → SaaS로 갈수록 사용자가 관리하는 범위는 어떻게 되나요?

- **답:** 점점 줄어듭니다. SaaS로 갈수록 클라우드 사업자가 관리하는 영역이 많아집니다.

---

## 7. 회사 데이터센터와 AWS를 연결해서 함께 사용하는 형태를 무엇이라고 하나요?

- **답:** 하이브리드 클라우드(Hybrid Cloud)입니다.

---

## 8. 다음 AWS 서비스의 역할은 무엇인가요?

- **답:**
  - EC2 = 가상 서버
  - VPC = AWS의 가상 네트워크
  - EBS = EC2에 연결해서 사용하는 블록 스토리지
  - S3 = 객체 스토리지
  - RDS = 관리형 관계형 데이터베이스
  - ELB = 여러 서버에 트래픽을 분산하는 로드 밸런싱 서비스
  - IAM = 사용자, 역할, 권한 관리
  - CloudWatch = AWS 자원 모니터링, 로그, 알람

---

## 9. EBS와 S3의 가장 기본적인 차이는 무엇인가요?

- **답:** EBS는 EC2에 디스크처럼 연결해서 사용하는 블록 스토리지이고, S3는 사진, 로그, 백업 파일 같은 객체를 저장하는 독립적인 객체 스토리지입니다.

---

## 10. EC2에 MySQL을 직접 설치하는 것과 RDS MySQL을 사용하는 것의 차이는 무엇인가요?

- **답:** EC2에 MySQL을 설치하면 OS와 DB 설치 및 운영을 사용자가 직접 관리해야 합니다. RDS는 AWS가 기반 인프라, 백업, 패치 등의 많은 관리 작업을 대신해주는 관리형 DB 서비스입니다.

---

## 11. AWS의 Pay-as-you-go란 무엇인가요?

- **답:** 필요한 AWS 자원을 사용하고, 실제 사용량에 따라 비용을 지불하는 종량제 방식입니다.

---

## 12. EC2를 Stop하면 AWS 비용이 무조건 0원이 되나요?

- **답:** 아닙니다. EC2 컴퓨팅 비용은 중지될 수 있지만 EBS, Public IPv4 등 다른 리소스 비용은 계속 발생할 수 있습니다.

---

## 13. AWS Free Tier라면 모든 서비스를 무제한 무료로 사용할 수 있나요?

- **답:** 아닙니다. 서비스별로 무료 사용 범위나 크레딧 한도가 있고, 이를 초과하면 비용이 발생할 수 있습니다.

---

## 14. 서울 리전에서 EC2를 만들었는데 목록에서 보이지 않는다면 가장 먼저 무엇을 확인해야 하나요?

- **답:** 현재 AWS 콘솔에서 선택된 Region을 확인합니다. 다른 Region을 보고 있으면 해당 EC2가 보이지 않습니다.

---

## 15. AWS Management Console에서 앞으로 자주 사용할 서비스는 무엇인가요?

- **답:** 대표적으로 EC2, VPC, S3, RDS, IAM, CloudWatch, CloudFormation 등을 자주 사용합니다.

---

# AWS 1장 핵심 암기

- 클라우드 = 필요한 IT 자원을 빌려 사용
- EC2 = 서버
- VPC = 네트워크
- EBS = EC2 디스크
- S3 = 객체 저장소
- RDS = 관리형 DB
- ELB = 부하분산
- IAM = 권한
- CloudWatch = 모니터링
- Pay-as-you-go = 사용한 만큼 비용 지불
- Hybrid Cloud = 온프레미스 + 퍼블릭 클라우드
</details>


<details>
<summary><h2>2장 AWS 컴퓨팅 서비스</h2></summary>

## AWS 컴퓨팅 서비스
1. 컴퓨팅은 CPU와 메모리 같은 컴퓨터 자원을 사용해서 프로그램을 실행하고 데이터를 처리하는 것이다.
2. CPU, MEMORY, Stroage, Network, Operating System 자원이 필요하다.

## 온프레미스에서의 컴퓨팅
1. 서버 구매, 배송, 설치, 설정 과정이 필요하다.

## 클라우드에서의 컴퓨팅
1. 물리서버를 구매하지 않고 필요한 컴퓨팅 자원을 서비스로 사용할 수 있다.
2. 가상 서버를 제공하는 AWS의 대표적인 서비스가 EC2이다.

## AWS 컴퓨팅 서비스
1. EC2, Lambda, ECS, EKS, Elastic Beanstalk
2. 어떤 방식으로 프로그램을 실행하고 싶은지에 따라 선택한다.

## Amazon EC2
1. Elastic Compute Cloud
2. 일반적인 서버가 필요할 때 사용할 수 있다.

## AWS Lambda
1. 서버를 직접 생성하고 관리하지 않고 코드를 실행할 수 있는 서비스이다.
2. Serverless 서비스라고 한다.

## EC2와 Lambda 차이
1. EC2는 서버를 만들어서 지속적으로 운영
2. Lambda는 특정 상황에서 코드를 실행
3. EC2는 웹 서버, 24시간 실행, 사용자가 계속 접속
4. Lambda는 파일 업로드 발생 할 때 잠깐 코드 실행 하는 용도

## Amazon ECS
1. Elastic Container Service
2. AWS에서 Docker 같은 컨테이너를 여러 개 운영하고 관리할 때 사용할 수 있는 서비스
3. ECS = AWS의 컨테이너 관리 서비스

## Amazon EKS
1. Elastic Kubernetes Service
2. AWS에서 Kubernetes Cluster를 운영하기 위한 관리형 서비스
3. ECS는 AWS 자체 컨테이너 오케스트레이션
4. EKS는 Kubernetes 기반

## Elastic Beantalk
1. 애플리케이션을 올리면 AWS가 애플리케이션 실행 환경 구성을 상당 부분 자동으로 처리해주는 서비스이다.
2. EC2를 직접 구성하는 것보다 사용자가 관리해야 할 인프라 영역이 줄어든다.

## Amazon EC2 소개
1. EC2는 Elastic Compute Cloud의 약자이다.
2. AWS에서 필요할 때 만들어 사용하는 가상 서버

## Amazon EC2 인스턴스
1. EC2 : AWS의 가상 서버 서비스 이름
2. EC2 Instance : EC2 서비스를 이용해 실제로 만든 서버 한 대

## EC2를 만들 때 무엇을 정해야 하나?
1. 어떤 OS를 사용할까? AMI
2. CPU / RAM은 얼마나 필요할까? Instance Type
3. 어느 네트워크에 둘까? VPC/Subnet
4. 디스크는 얼마나 필요할까? EBS
5. 어떤 통신을 허용할까? Security Group
6. SSH 접속은 어떻게 인증할까?Key Pair

## Instance Type
1. EC2의 CPU, Memory, Network 성능 등의 사양을 결정한다.
2. T 계열 : 소규모 / 버스터블 범용
3. M 계열 : 범용
4. C 계열 : CPU 연산 중심
5. R 계열 : Memory 중심

## EC2 상태
1. 서버를 처음 만들면 Pending → Running
2. 서버를 중지하면 Running → Stopping → Stopped
3. 다시 시작하면 Stopped → Pending → Runnig
4. 완전히 삭제하면 Running → Shutting-down → Terminated

## Stop과 Terminate 차이
1. Stop
2. 전원 끄기
3. Terminate
4. 서버 자체를 제거

## AMI
1. Amazon Machine Image
2. EC2를 만들기 위한 서버 이미지
3. OS뿐 아니라 미리 설치한 프로그램이나 설정이 포함된 서버 이미지를 만들 수도 있다.
4. AMI는 서버 표준화와 반복 배포에 유용하다.

## Amazon EC2 스토리지
1. EBS

## EBS
1. Elastic Block Store
2. EC2에 연결해서 사용하는 가상 디스크

## Root Volume
1. EC2를 생성하면 일반적으로 OS가 들어 있는 기본 디스크가 필요하다. 이걸 Root Volume이라고 한다.
2. df -h : 파일시스템 사용량
3. lsblk : 서버에 연결된 블록 디바이스 확인
4. 추가 디스크를 연결한 다음 파일시스템 생성 → Mount → 사용
5. EC2는 컴퓨팅 자원이고 EBS는 스토리지 자원이다.

## Amazon EC2 네트워킹
1. VPC → Subnet → ENI → EC2
2. VPC : 회사 네트워크 전체
3. Subnet : 그 네트워크를 나눈 구역
4. ENI : EC2의 가상 랜카드
5. EC2 : 실제 서버

## VPC
1. Virtual Private Cloud
2. AWS 안에서 사용하는 논리적으로 격리된 가상 네트워크이다.
3. EC2는 어느 VPC의 어느 Subnet에 들어갈지 정해야 한다.

## ENI
1. Elastic Network Interface
2. EC2의 가상 NIC(랜카드)이다.
3. 온프레미스 : 서버 → NIC → Switch → Network
4. AWS : EC2 → ENI → Subnet → VPC
5. EC2의 IP 주소나 Security Group 같은 네트워크 관련 정보도 ENI와 연결되어 있다.

## Private IP
1. EC2는 Subnet 내부에서 Private IPv4 주소를 받는다.
2. 주로 AWS 내부 /VPC 내부 통신에 사용한다.

## Public IP
1. Public IP가 있다고 인터넷 통신이 무조건 되는 것은 아니다.
2. Internet Gateway
3. Route Table
4. Security Group
5. Network ACL 등이 제대로 설정되어야 한다.

## Elastic IP
1. 자동으로 할당되는 Public IP는 상황에 따라 바뀔 수 있다.
2. 특정 서버에 계속 같은 공인 IPv4가 필요하다면 EIP를 사용할 수있다.

## EC2 네트워크 
1. Internet → Internet Gateway → Route Table → Subnet → ENI → EC2

## Amazon EC2 보안
1. Security Group
2. Key Pair
3. IAM Role
4. OS 보안

## Security Group
1. EC2 앞에 있는 가상 방화벽
2. Internet → Security Group → EC2
3. 어떤 통신을 허용할지 결정한다.
4. Protocol, Port, Source
5. Inbound : 외부에서 EC2로 들어오는 통신
6. Outbound : EC2가 외부로 나가는 통신
7. Stateful : 상태를 기억해서 허용한다.

## Key Pair
1. EC2에 SSH로 접속할 때 사용할 수 있는 인증 수단이다.
2. Public Key 는 EC2에 저장, Private Keys는 내가 보관
3. Public Key와 Private Key로 구성되며, Linux 인스턴스에서는 Private Key로 SSH 접속시 본인임을 증명할 수 있다.

## IAM Role
1. 사람의 권한만 IAM으로 관리하는 것이 아니라 EC2같은 AWS 서비스에도 역할을 줄 수 있다.

## OS 보안
1. AWS에서 EC2를 쓰더라도 Linux 보안 패치와 계정 관리 등을 우리가 해야한다.

## Amazon EC2 모니터링
1. Amazon CloudWatch
2. EC2 관련 지표를 확인할 수 있다.
3. EC2 환경의 상태를 확인하는 기본 모니터링 수단이다.
4. CPUUtilization : CPU 사용률, top, ps aux --sort=%cpu

## Status Check
1. EC2에는 상태 검사가 있다.
2. 현재 EC2는 자동으로 System, Instance, Attached EBS 상태 검사를 수행하고, Application 상태 검사는 선택적으로 사용할 수 있다.
3. System Status Check
4. Instance Status Check

## System Status Check
1. EC2 아래쪽 AWS 기반 인프라에 문제가 있는지 확인한다.
2. 물리 호스트나 AWS 계층 문제를 감지한다.

## Instance Status Check
1. 개별 EC2 내부 문제를 확인한다.
2. OS 부팅 문제, 메모리 부족, 잘못된 네트워크 설정, 파일시스템 문제, Kernel 문제 등
3. System Status Check : AWS 인프라 문제
4. Instance Status Check : EC2 OS/설정 문제

## CloudWatch Alarm
1. Metric 확인 + Alarm + Log

## Amazon EC2 인스턴스 구입 옵션
1. On-Demand, Savings Plans, Reserved Instances, Spot, Dedicated Host/Instance, Capacity Reservations 등이 있다.

## On-Demand
1. 사용 시작 → EC2 실행 → 사용한 만큼 지불
2. 장점 : 유연함, 약정 없음, 언제든 생성/삭제
3. 단점 : 장기간 계속 사용할 경우 다른 할인 옵션보다 비쌀 수 있음

## Savings Plans
1. AWS 컴퓨팅 사용량을 1년 또는 3년 동안 일정 수준 사용하겠다고 약정하고 비용 할인을 받는 방식이다.
2. 특정 서버 한 대를 미리 사놓는 개념보다 일정 컴퓨팅 사용량에 대해 약정한다.

## Reserved Instances
1. 장기간 안정적으로 사용하는 경우 비용 절감을 위한 방법
2. 1년 또는 3년 약정을 사용

## Spot Instance
1. AWS에 남아 있는 여유 EC2 용량을 저렴하게 사용하는 방식
2. 장점 : 매우 저렴하게 사용
3. 단점 : 용량이 필요해지면 중단될 수 있다.

##  AWS 2장 확인문제 + 정답

## 1. 컴퓨팅이란 무엇인가요?

- **답:** CPU와 메모리 같은 컴퓨터 자원을 이용해서 프로그램을 실행하고 데이터를 처리하는 것을 말합니다.

---

## 2. AWS의 대표적인 컴퓨팅 서비스에는 무엇이 있나요?

- **답:**
  - EC2 = 가상 서버
  - Lambda = 서버 관리 없이 코드 실행
  - ECS = AWS의 컨테이너 오케스트레이션 서비스
  - EKS = AWS의 관리형 Kubernetes 서비스
  - Elastic Beanstalk = 애플리케이션 배포 환경을 관리해주는 서비스

---

## 3. EC2와 EC2 Instance의 차이는 무엇인가요?

- **답:** EC2는 AWS의 가상 서버 서비스 이름이고, EC2 Instance는 EC2를 이용해 실제로 생성한 가상 서버 한 대를 의미합니다.

---

## 4. EC2 Instance Type은 무엇을 결정하나요?

- **답:** EC2에 할당할 CPU, 메모리, 네트워크 성능 등의 서버 사양을 결정합니다.

---

## 5. T, M, C, R 계열의 특징은 무엇인가요?

- **답:**
  - T = 소규모 / 버스터블 범용
  - M = 범용
  - C = CPU 연산 중심
  - R = 메모리 중심

---

## 6. EC2의 Stop과 Terminate의 차이는 무엇인가요?

- **답:**
  - Stop = 인스턴스 실행만 중지하며 다시 Start할 수 있습니다.
  - Terminate = 인스턴스를 삭제하는 것이며 다시 Start할 수 없습니다.

---

## 7. AMI란 무엇인가요?

- **답:** Amazon Machine Image의 약자로, EC2 Instance를 생성하기 위한 서버 이미지입니다. OS뿐 아니라 소프트웨어와 설정을 포함할 수도 있습니다.

---

## 8. AMI와 EC2 Instance의 차이는 무엇인가요?

- **답:** AMI는 서버를 만들기 위한 이미지이고, EC2 Instance는 AMI를 이용해서 실제로 생성하고 실행하는 서버입니다.

---

## 9. AMI를 사용하는 장점은 무엇인가요?

- **답:** 동일한 OS, 프로그램, 설정을 가진 서버를 반복적으로 생성할 수 있어 서버 표준화와 반복 배포에 유리합니다.

---

## 10. EBS란 무엇인가요?

- **답:** Elastic Block Store의 약자로, EC2에 디스크처럼 연결해서 사용하는 블록 스토리지입니다.

---

## 11. Root Volume이란 무엇인가요?

- **답:** EC2의 운영체제가 설치되어 있는 기본 디스크입니다.

---

## 12. EC2와 EBS는 같은 자원인가요?

- **답:** 아닙니다. EC2는 컴퓨팅 자원이고 EBS는 스토리지 자원입니다. 따라서 EC2를 중지해도 EBS는 남아 있을 수 있습니다.

---

## 13. EC2는 AWS 네트워크에서 어떤 구조로 배치되나요?

- **답:**

```text
VPC
 └─ Subnet
     └─ ENI
         └─ EC2
```

EC2는 VPC의 특정 Subnet에 배치되고, ENI라는 가상 네트워크 인터페이스를 통해 통신합니다.

---

## 14. ENI란 무엇인가요?

- **답:** Elastic Network Interface의 약자로, EC2에 연결되는 가상 네트워크 인터페이스입니다. 쉽게 말하면 EC2의 가상 랜카드입니다.

---

## 15. Private IP와 Public IP의 차이는 무엇인가요?

- **답:**
  - Private IP = VPC 내부 통신에 사용하는 주소
  - Public IP = 인터넷과 통신할 때 사용할 수 있는 공인 주소

---

## 16. Public IP만 있으면 EC2가 무조건 인터넷 통신이 가능한가요?

- **답:** 아닙니다. Internet Gateway, Route Table, Security Group 등의 설정도 정상이어야 합니다.

---

## 17. Elastic IP란 무엇인가요?

- **답:** 사용자가 직접 할당하고 관리할 수 있는 고정 Public IPv4 주소입니다.

---

## 18. Security Group이란 무엇인가요?

- **답:** EC2와 같은 AWS 자원에 적용하는 가상 방화벽입니다. Inbound와 Outbound 규칙을 이용해서 허용할 통신을 설정합니다.

---

## 19. Security Group의 Inbound와 Outbound 차이는 무엇인가요?

- **답:**
  - Inbound = 외부에서 EC2로 들어오는 통신
  - Outbound = EC2에서 외부로 나가는 통신

---

## 20. Security Group은 Stateful인가요, Stateless인가요?

- **답:** Stateful입니다. 허용된 요청에 대한 응답 트래픽은 별도의 반대 방향 규칙이 없어도 허용됩니다.

---

## 21. Linux EC2에 SSH로 접속할 때 기본적으로 어떤 것이 필요한가요?

- **답:** Public IP, Security Group의 TCP 22 허용, 올바른 사용자 계정, Key Pair의 Private Key가 필요합니다.

---

## 22. Key Pair는 어떤 역할을 하나요?

- **답:** EC2에 SSH로 접속할 때 사용자의 신원을 확인하는 인증 수단입니다. Public Key는 EC2 쪽에 등록되고 Private Key는 사용자가 보관합니다.

---

## 23. EC2에서 S3 같은 AWS 서비스에 접근할 때 Access Key를 서버에 직접 저장하는 것보다 권장되는 방법은 무엇인가요?

- **답:** EC2에 IAM Role을 연결해서 필요한 권한을 부여하는 방식이 권장됩니다.

---

## 24. AWS 공동 책임 모델에서 EC2 사용자가 관리해야 하는 것은 무엇인가요?

- **답:** EC2 내부의 OS, 계정, 패치, 애플리케이션, 미들웨어, Security Group 설정 등은 사용자가 관리해야 합니다.

---

## 25. EC2 모니터링에 사용하는 대표적인 AWS 서비스는 무엇인가요?

- **답:** Amazon CloudWatch입니다.

---

## 26. CloudWatch에서 EC2의 대표적인 지표는 무엇인가요?

- **답:**
  - CPUUtilization
  - NetworkIn
  - NetworkOut
  - StatusCheckFailed

---

## 27. CloudWatch와 Linux 명령어는 어떻게 같이 사용하나요?

- **답:** CloudWatch로 서버의 이상 징후를 발견하고, SSH로 접속해서 `top`, `free`, `df`, `ss`, `systemctl` 등의 명령어로 내부 원인을 분석합니다.

---

## 28. System Status Check와 Instance Status Check의 차이는 무엇인가요?

- **답:**
  - System Status Check = AWS 물리 호스트나 기반 인프라 문제 확인
  - Instance Status Check = EC2 내부 OS나 네트워크 설정 등의 문제 확인

---

## 29. On-Demand Instance란 무엇인가요?

- **답:** 장기 약정 없이 필요한 만큼 EC2를 사용하고 사용량에 따라 비용을 지불하는 방식입니다.

---

## 30. Spot Instance란 무엇인가요?

- **답:** AWS의 남는 EC2 용량을 저렴하게 사용하는 방식입니다. 비용은 저렴하지만 AWS의 용량 상황에 따라 인스턴스가 중단될 수 있습니다.

---

## 31. Spot Instance는 어떤 작업에 적합한가요?

- **답:** 중단되어도 다시 실행할 수 있는 배치 작업, 데이터 처리, 테스트 작업 등에 적합합니다.

---

## 32. Savings Plans와 Reserved Instances의 공통 목적은 무엇인가요?

- **답:** 장기간 AWS 컴퓨팅 자원을 사용할 것을 전제로 약정하여 On-Demand보다 비용을 절감하는 것이 주요 목적입니다.

---

## 33. Capacity Reservation의 주요 목적은 무엇인가요?

- **답:** 특정 Availability Zone에서 필요할 때 EC2 Instance를 생성할 수 있도록 컴퓨팅 용량을 미리 확보하는 것입니다.

---

## 34. EC2에 SSH 접속은 되지만 웹 페이지가 열리지 않을 때 확인할 항목은 무엇인가요?

- **답:**
  - Apache/Nginx 서비스가 실행 중인지 확인
  - TCP 80번 포트를 Listen 중인지 확인
  - Security Group에서 HTTP 80을 허용했는지 확인
  - Public IP가 있는지 확인
  - Route Table과 Internet Gateway가 정상인지 확인

---

## 35. 현재 로그인한 Linux 사용자를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
whoami
```

---

## 36. 서버의 Hostname을 확인하는 명령어는 무엇인가요?

- **답:**

```bash
hostname
```

---

## 37. CPU 정보를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
lscpu
```

---

## 38. 메모리 사용량을 확인하는 명령어는 무엇인가요?

- **답:**

```bash
free -h
```

---

## 39. 파일시스템의 디스크 사용량을 확인하는 명령어는 무엇인가요?

- **답:**

```bash
df -h
```

---

## 40. 서버에 연결된 디스크 장치를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
lsblk
```

---

## 41. EC2의 IP 주소와 네트워크 인터페이스 정보를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
ip addr
```

---

## 42. Linux 서버의 라우팅 정보를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
ip route
```

---

## 43. 현재 서버에서 Listen 중인 포트를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
sudo ss -tulnp
```

80번 포트만 확인하려면:

```bash
sudo ss -ltnp | grep :80
```

---

## 44. Apache 서비스 상태를 확인하는 명령어는 무엇인가요?

- **답:**

```bash
sudo systemctl status apache2
```

---

## 45. 서버 내부에서 HTTP 서비스가 실제로 응답하는지 확인하는 명령어는 무엇인가요?

- **답:**

```bash
curl -I http://localhost
```

---

# AWS 2장 핵심 암기

```text
EC2 = AWS 가상 서버

EC2 Instance = 실제 생성된 서버 한 대

AMI = EC2를 만들기 위한 서버 이미지

Instance Type = CPU / Memory 등의 서버 사양

EBS = EC2에 연결하는 블록 스토리지

ENI = EC2의 가상 랜카드

Private IP = VPC 내부 통신

Public IP = 인터넷 통신

Security Group = 가상 방화벽

Key Pair = SSH 인증

IAM Role = EC2에 AWS 서비스 접근 권한 부여

CloudWatch = AWS 모니터링

System Status Check = AWS 기반 인프라 문제

Instance Status Check = EC2 내부 문제

On-Demand = 약정 없이 사용

Spot = 저렴하지만 중단 가능
```














</details>








