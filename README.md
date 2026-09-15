# AWS

<details>
<summary><h2>1장 AWS란?</h2></summary>

---

### 1.1 클라우드 컴퓨팅

* **1.1.1 클라우드 컴퓨팅이란?**
  * 과거에는 서비스를 운영하려면 직접 장비를 구매해야 했음
  * 클라우드 방식은 직접 서버를 구매하지 않음
  * 인터넷을 통해 서버, 스토리지, 데이터베이스, 네트워크 등의 컴퓨팅 자원을 필요할 때 제공받아 사용하는 방식

* **1.1.2 클라우드 컴퓨팅 이점**
  * **초기 비용 감소:** 장비를 직접 구매하지 않아도 됨
  * **빠른 서버 구축:** 온프레미스에 비해 압도시적으로 빠른 구축 가능
  * **확장성:** 트래픽 증가나 이벤트 시 클라우드에서 유연하게 서버 확장 가능
  * **고가용성:** 서버를 여러 대 운영하여 장애에 효과적으로 대응
  * **글로벌 서비스:** AWS가 보유한 다양한 지역의 인프라 활용 가능

* **1.1.3 클라우드 컴퓨팅 서비스 유형**
  * **IaaS (Infrastructure as a Service):** 
    * 인프라를 제공하는 서비스
    * 사용자는 운영체제와 애플리케이션을 관리함 (예: AWS EC2)
  * **PaaS (Platform as a Service):** 
    * 애플리케이션을 실행할 수 있는 플랫폼을 제공
    * 사용자는 주로 애플리케이션과 데이터에 집중함
  * **SaaS (Software as a Service):** 
    * 완성된 소프트웨어를 인터넷을 통해 사용하는 방식

* **1.1.4 클라우드 구축 모델**
  * **Public Cloud:** 클라우드 서비스 제공자의 인프라를 사용하는 방식 (AWS, Azure, Google Cloud 등). 빠른 사용, 적은 초기 비용, 쉬운 확장
  * **Private Cloud:** 회사가 자체적으로 클라우드 환경(서버, 스토리지, 네트워크, 가상화)을 내부에 구축. 높은 통제력과 보안 관리의 장점이 있으나 비용 증가 및 직접 관리 부담 존재
  * **Hybrid Cloud:** Public Cloud와 Private Cloud를 함께 사용하는 방식

---

### 1.2 AWS 서비스

* **1.2.1 AWS 소개**
  * **AWS란?** Amazon Web Services의 약자로, 인터넷을 통해 다양한 IT 서비스를 제공하는 클라우드 컴퓨팅 플랫폼
  * **AWS 글로벌 인프라:**
    * **Region(리전):** AWS의 지리적인 서비스 지역
    * **Availability Zone(AZ):** 하나의 리전 내에 존재하는 여러 개의 가용 구역 (서버를 여러 AZ에 분산하여 장애 대응력 강화)

* **1.2.2 AWS 서비스 라인업**
  * **컴퓨팅 서비스:** EC2(가상서버), Lambda(서버리스 방식, 코드만 실행), ECS/EKS(컨테이너 운영)
  * **스토리지 서비스:** EBS(EC2 디스크), EFS(공유 파일 시스템), S3(파일 저장소)
  * **네트워킹 서비스:** VPC(가상 네트워크), ELB(로드 밸런서), Route 53(DNS), CloudFront(CDN)
  * **데이터베이스 서비스:** RDS(관계형 DB), DynamoDB(NoSQL)
  * **보안 서비스:** IAM, Security Group, KMS 등

* **1.2.3 AWS 과금 체계**
  * **Pay-as-you-go:** 사용한 만큼 비용을 지불하는 구조
  * **AWS 주요 가격 모델:**
    * **On-Demand:** 실습이나 단기 프로젝트에 적합
    * **Savings Plans:** 약정을 통해 비용을 절감하는 모델
    * **Spot Instance:** AWS의 유휴 컴퓨팅 자원을 할인된 가격으로 사용하는 방식

</details>


<details>
  <summary><b>2장 AWS 컴퓨팅 서비스</b></summary>
  
  <h3>2.1 AWS 컴퓨팅 서비스</h3>
  <h4>2.1.1 컴퓨팅 정의</h4>
  <ul>
    <li><b>컴퓨팅이란?</b>: 컴퓨터의 CPU와 메모리 등의 자원을 이용해서 데이터를 처리하고 프로그램을 실행하는 것</li>
    <li><b>서버에서 컴퓨팅 자원</b>: CPU, 메모리, 스토리지, 네트워크</li>
    <li><b>클라우드에서 컴퓨팅</b>: 클라우드에서는 필요한 컴퓨팅 자원을 클라우드 사업자로부터 제공받음</li>
  </ul>

  <h4>2.1.2 AWS 컴퓨팅 서비스</h4>
  <ul>
    <li><b>Amazon EC2</b>: AWS에서 원하는 사양의 가상 서버를 만들어 사용하는 서비스</li>
    <li><b>AWS Lambda</b>: 서버를 직접 관리하지 않고 함수 단위로 코드를 실행하는 서버리스(Serverless) 방식</li>
    <li><b>Amazon ECS (Elastic Container Service)</b>: 컨테이너를 실행하고 관리하기 위한 AWS 서비스</li>
    <li><b>Amazon EKS (Elastic Kubernetes Service)</b>: AWS에서 Kubernetes 클러스터를 운영할 수 있게 해주는 관리형 서비스</li>
    <li><b>AWS Elastic Beanstalk</b>: 애플리케이션을 AWS에 비교적 쉽게 배포할 수 있도록 해주는 서비스</li>
  </ul>

  <h3>2.2 Amazon EC2 소개</h3>
  <h4>2.2.1 Amazon EC2 인스턴스</h4>
  <ul>
    <li><b>EC2 인스턴스란?</b>: AWS에서 실행 중인 가상 서버 (EC2는 가상 서버를 제공하는 서비스, EC2 인스턴스는 그 안에서 실제로 실행되는 서버 하나)</li>
    <li><b>인스턴스 타입</b>: EC2 서버의 하드웨어 사양을 결정하는 것</li>
    <li><b>EC2 인스턴스의 상태</b>: 
      <ul>
        <li><code>Running</code> (서버 활성화)</li>
        <li><code>Stopped</code> (서버 중지)</li>
        <li><code>Terminated</code> (인스턴스 완전 종료)</li>
      </ul>
    </li>
  </ul>

  <h4>2.2.2 AMI (Amazon Machine Image)</h4>
  <ul>
    <li>EC2 인스턴스를 생성할 때 사용하는 서버 이미지 (OS와 기본적인 서버 환경 포함)</li>
    <li>AWS 제공 AMI 사용 가능 및 직접 만든 서버를 AMI로 만들어 재사용 가능</li>
    <li>여러 서버를 동일한 환경으로 배포할 때 유용하며, Auto Scaling 및 서버 표준화와 연결되는 중요한 개념</li>
  </ul>

  <h4>2.2.3 기타 EC2 핵심 요소</h4>
  <ul>
    <li><b>2.2.3 EC2 스토리지</b>: EC2의 대표적인 블록 스토리지는 EBS</li>
    <li><b>2.2.4 EC2 네트워킹</b>: ENI, Private IP, Public IP, VPC, Subnet, Security Group 등을 통해 네트워크 구성</li>
    <li><b>2.2.5 EC2 보안</b>: Key Pair + Security Group + OS 보안 등을 통해 서버 보호</li>
    <li><b>2.2.6 EC2 모니터링</b>: CloudWatch와 Linux 도구를 이용해 서버 상태 확인</li>
    <li><b>2.2.7 EC2 구입 옵션</b>: On-Demand / Savings Plans / Spot 등의 방식으로 비용 최적화</li>
  </ul>
</details>








