# 마이크로 서비스 개발을 위한 API 우선 설계 및 API 구축하기

본 문서는 Oracle Apiary에서 API Blueprint를 활용하여 API 설계 문서를 보고, 만들어진 문서를 토대로 [Oracle Helidon](http://helidon.io)과 [Oracle Database의 REST Data Service](https://www.oracle.com/database/technologies/appdev/rest.html)로 마이크로 서비스를 구현하는 방법을 보여줍니다. 
또한 API 문서와 구현된 서비스간의 일치 여부를 확인, 검증하는 [Dredd](https://github.com/apiaryio/dredd) 도구과 CI/CD 도구인 [Wercker](https://app.wercker.com/)를 통합하여 API 문서와 실제 동작하는 서비스간의 지속적인 검증 테스트를 실시하여 서비스에 대한 높은 신뢰와 퀄리티를 유지할 수 있는 방법을 보여줍니다.
배포된 서비스(ORDS)에 보안 및 다양한 정책을 적용해 보고, 마지막으로 API Gateway에 배치하여 API문서와 최적화된 API 앤드포인트를 애플리케이션 개발자에게 오픈하는 내용을 담고 있습니다.
본 문서를 통해 오라클 솔루션을 활용하여 마이크로 서비스 개발에 대한 통합된 개발 라이프사이클을 경험해 볼 수 있습니다.

***

### 실습을 위해 필요한 프로그램과 환경
#### 데스크탑 설치 프로그램
* [Java SE Development Kit 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* [Node.js](https://nodejs.org/ko/download)
* [Apache Maven](https://maven.apache.org/download.cgi)
* [Git](https://git-scm.com/download/win)
* [Visual Studio Code](https://code.visualstudio.com/download)
* [SQL Developer](https://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html)
* [Insomnia](https://insomnia.rest/download)

#### Oracle Cloud 환경
* [Oracle Apiary Cloud Service](https://apiary.io)
* [Oracle Compute Cloud Service](https://cloud.oracle.com/ko_KR/compute)
* [Oracle Database Cloud Service](https://cloud.oracle.com/ko_KR/database)
* [Oracle API Platform Cloud Service](https://cloud.oracle.com/ko_KR/api-platform)

#### GitHub 계정
* [GitHub](https://github.com)

***

### 실습 내용
![Scenario1](images/api_first_design_scenario_0.png)

![Scenario2](images/api_first_design_scenario.png)
#### [PART 1 실습하기](HOL-PART1.md)
##### API Blueprint 문서 설계와 Microprofile 기반 Helidon을 활용한 서비스 개발, 그리고 Wercker CI까지!!!
1. API 설계 문서 (API Blueprint) 작성하기  
   * Apiary 계정 생성하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ API Blueprint 설계 문서 작성하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ API Blueprint GitHub에 푸시하기  
2. Helidon을 활용하여 마이크로 서비스를 개발하고 API 설계 문서와 일치 여부 테스트하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ Helidon MP (MicroProfile) 프로젝트 생성 및 서비스 만들기  
&nbsp;&nbsp;&nbsp;&nbsp;■ Dredd를 활용하여 API 설계문서와 서비스간의 일치 여부 검증하기  
3. Wercker와 Dredd, Github을 사용하여 지속적 통합 테스트 환경 구축하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ Wercker 계정 생성하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ Continuous Integration 환경 구성 및 실행  

- [PART 1 실습으로 가기](HOL-PART1.md)

#### [PART 2 실습하기](HOL-PART2.md)
##### 오라클 데이터베이스와 SQL만 알아도 REST 서비스를 개발한다! 또한 라이프사이클 관리를 위한 차세대 API Platform 환경에 대한 경험까지!!!
1. ORDS를 활용하여 마이크로 서비스를 개발하고 배포하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ ORDS REST 서비스 만들고 배포하기  
2. ORDS 서비스에 보안 및 정책을 적용하고 API Gateway에 배포하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ 서비스 등록 및 API 정책 적용하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ 배치된 서비스 테스트 하기  
3. 애플리케이션 개발자를 위해 개발자 포탈에 API 퍼블리시 하기  
&nbsp;&nbsp;&nbsp;&nbsp;■ Apiary 연동 및 API 개발자 포탈에 게시 (실습X)  
&nbsp;&nbsp;&nbsp;&nbsp;■ 개발자 포탈에서 API 검색 및 문서 보기  

- [PART 2 실습으로 가기](HOL-PART2.md)
