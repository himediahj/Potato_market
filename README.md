# Potato Market
<pre>
java console + jdbc를 활용한 미니 프로젝트입니다.
작업자: <a href = "https://github.com/Seo-Aram">@Seo-Aram</a>, <a href = "https://github.com/savesoo">@savesoo</a>, <a href = "https://github.com/himediahj">@himediahj</a>, <a href = "https://github.com/himediabyul">@himediabyul</a>, <a href = "https://github.com/0808min">@0808min</a>
</pre>
-----
## 기술 구조
* JAVA
  * JAVA OOP
  * Collection
  * JDBC
  * MVC Pattern
  * JSON Parser
  * AES256 Encrypt
  * Serializable
* DBMS - MySQL
  * RDS
* SQL
----
## 개요
본 프로젝트는 중고 거래 플랫폼에서 볼 수 있는 기능들을 콘솔 창에서도 비슷하게 이용할 수 있습니다. JAVA-SE17, MySql-8을 이용하여 개발 되었으며, 주요 기능은 다음과 같습니다.   
* 회원
  * 로그인(유사 자동 로그인 기능을 포함합니다)
  * 회원 가입
  * 회원 정보 수정
  * 회원 정보 조회
* 판매내역
  * 현재 판매 중인 상품 내역 조회
  * 구매
  * 수정
  * 삭제
  * 내 판매(완료 및 판매 중) 내역 조회
* 구매
  * 구매 내역 조회
---
## 기능
* 로그인 이후에 정상적으로 프로그램이 종료될 경우, 로그아웃 여부를 확인합니다. 로그아웃을 하지 않을 경우 .ser 파일을 생성하여 데이터를 남기고, 추후에 프로그램을 실행할 때 자동으로 로그인 기능을 제공합니다.
* 회원 가입 및 회원 정보 수정시 비밀번호를 정확히 입력 하였는지 2차 입력을 받아 확인합니다. 1번 입력과 2번 입력이 동일할 경우 정상적으로 처리 합니다.
* 비밀번호는 AES256로 암호화 하며 별도로 복호화 하지 않습니다.
* DB 접속 데이터는 config.json을 참조하여 세팅합니다.
* Controller, Domain, DAO, Service로 구조를 구분하여 데이터를 처리할 수 있도록 합니다. 기본적인 MVC 표준을 지키고자 하였습니다.
* 전체 글 보기를 할 경우, 현재 판매 중인 게시글만 보여줍니다.
* 판매하고 싶은 상품을 등록할 수 있습니다.
* 현재 판매 중인 상품 명으로 검색이 가능합니다.
* 내가 쓴 글이면서 현재 판매 중(판매 완료 제외) 글만 수정 및 삭제할 수 있습니다.
* 다른 사람이 판매 중인 산품을 구매할 수 있습니다.
* 내가 판매한 내역, 내가 구매한 글의 목록을 화면에 표시해줍니다.
* 회원 정보를 조회하고, 내 정보를 수정할 수 있습니다.
---
## 테스트 방법
1. MySQL-8 / JAVA-SE 17 이상 세팅 환경 설정
2. config.json 파일에 DB 접속 설정 변경
3. sql폴더에 위치한 .sql 파일을 빠른 날짜부터 실행(테이블 / 테스트 데이터 세팅)
4. 프로그램 실행(src 하위의 Main.java) 후 로그인
   1. id: son / pw: 0000
   2. id: vip / pw: 1111
5. 콘솔 메뉴에 따라 테스트 진행
