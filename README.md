# 마이크로 서비스 개발을 위한 API 우선 설계 및 API 구축하기

본 과정에서는 API Blueprint를 활용하여 API 문서를 만들어 보고, Microprofile 기반의 [Oracle Helidon](http://helidon.io)과 [Oracle Database의 REST Data Service](https://www.oracle.com/database/technologies/appdev/rest.html)로 마이크로 서비스를 구현하는 것을 보여줍니다. 
또한 API 문서와 구현된 서비스간의 비호환 (서비스에 대응하는 문서 호환 여부) 여부를 확인, 검증하는 [Dredd](https://github.com/apiaryio/dredd)와 CI 도구인 [Wercker](https://app.wercker.com/)를 통합하여 API 비호환 테스트를 지속적으로 자동화하는 것을 보여줍니다.
마지막으로 배포된 API에 대한 보안 및 다양한 정책을 적용해 보고, API Gateway에 배포하여 최종적으로 서비스와 문서를 애플리케이션 개발자에게 오픈하는 내용을 담고 있습니다.
본 과정을 통해 오라클 솔루션을 활용하여 마이크로 서비스 개발에 대한 전반적인 라이프사이클을 경험해 보실 수 있습니다.

## 데스크탑  설치 프로그램
* [Java SE Development Kit 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* [Node.js](https://nodejs.org/ko/download)
* [Apache Maven](https://maven.apache.org/download.cgi)
* [Git](https://git-scm.com/download/win)
* [Visual Studio Code](https://code.visualstudio.com/download)
* [SQL Developer](https://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html)
* [Insomnia](https://insomnia.rest/download)

## Oracle Cloud 환경
* [Oracle Compute Cloud Service](https://cloud.oracle.com/ko_KR/compute)
* [Oracle Database Cloud Service](https://cloud.oracle.com/ko_KR/database)
* [Oracle API Platform Cloud Service](https://cloud.oracle.com/ko_KR/api-platform)

## 시나리오
1. Apiary에서 API Blueprint 작성하기
2. Helidon (MP)과 ORDS를 사용하여 서비스 개발하고 Dredd를 사용하여 API Blueprint와 Helidon 서비스간 호환 여부 검증 및 테스트하기
3. Wercker와 Dredd, Github을 사용하여 지속적 통합 환경 구축하기
4. API 서비스에 보안 및 정책을 적용하고 API Gateway에 서비스 배포하기

![Scenario](images/api_first_design_scenario.png)

## Apiary 계정 생성하기
먼저 [Apiary(https://apiary.io)](https://apiary.io) 홈페이지에 접속한 후 우측 상단의 **Sign up** 버튼을 클릭합니다.
![apiary home](images/apiary_home.png)

**Continue with GitHub** 버튼을 클릭합니다.  
GitHub 계정이 필요합니다. 만약에 없을 경우 [GitHub(https://github.com)](https://github.com)에서 계정을 생성하세요.
![apiary_sign_up](images/apiary_sign_up.png)

GitHub 계정을 입력하고 **Sign In** 버튼을 클릭합니다.
![apiary_github_account1](images/apiary_github_account1.png)

verify를 위한 메일이 발송됩니다. 
![apiary_github_auth](images/apiary_github_auth.png)

등록한(로그인) 메일 계정으로 접속하여 verify 메일을 확인하고 **verify email address**를 클릭 합니다.
![apiary_email_auth](images/apiary_email_auth.png)

다시 Apiary 홈페이지로 접속하여 우측 상단의 **Sign In** 버튼을 클릭한 후 **Continue with GitHub** 버튼을 클릭 합니다.
![apiary_signin](images/apiary_signin.png)

다시 GitHub 계정을 입력하고 **Sign In** 버튼을 클릭합니다.
![apiary_github_signin](images/apiary_github_signin.png)

Apiary 계정을 생성하면 기본 API 하나를 생성해야 합니다. **Name your first API** 부분에 *myfirstapi* 혹은 *helloapiary* 와 같이 임의로 입력합니다.
![apiary_first_api](images/apiary_first_api.png)

축하합니다!! Apiary 계정을 성공적으로 생성하셨습니다. 아래 화면은 Apiary 에디터 화면으로 좌측이 에디터, 우측이 실시간으로 만들어지는 API 문서입니다.
![apiary_first_api_editor](images/apiary_first_api_editor.png)


