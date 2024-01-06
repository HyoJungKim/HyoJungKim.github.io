---
title:  "PostgreSQL과 pgAdmin설치" 
excerpt: "PostgreSQL과 pgAdmin설치"

categories:
  - PostgreSQL
tags:
  - [PostgreSQL]

toc: true
toc_sticky: true
 
date: 2024-01-06
last_modified_at: 2024-01-06

---

SQL practice를 위해서 다음 선행이 필요하다.

1) DBMS 설치
2) DBMS에 맞는 GUI 설치
3) DBMS connetction 설정

1)은 MySQL이냐 MSSQL이냐, postgreSQL이냐, Oracle이냐 하는 등의 소위 DB server를 말하는 것이고,

2)는 server에 직접 붙어서 커맨드창으로 SQL을 수행할 수도 있지만 관리/생산성향상을 위해 널리 쓰이는 다양한 GUI들이 있는데 그 중에 하나를 선택해서 설치하는 것이다. 1)에 따라 대표적인 GUI는 대개 정해져 있으며, 이는 개인의 취향에 따라 선택하면 된다.
예를 들면 MySQL은 workbench, MS SQL Server는 SQL Server Managenet Studio(SSMS), PostgreSQL은 paAdmin등이 있다.

3)은 local(SQL구문을 보내고 결과를 받을)과 server간의 연결을 만들어 주는 것으로, 일반적으로 host, port, database, user(ID), password 정도의 정보를 필요로 한다.


이 글에서는 SQL practice를 위해서 PostgreSQL 과 pgAdmin설치를 진행한다.

PostgreSQL은 open source DBMS로서, 학계 및 공공/산업계에서 고르게 쓰인다.
![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/a4f0550b-f1d4-4f0d-81fd-88e07ef4481e)
(출처: DB engines.com https://db-engines.com/en/ranking_trend)

OMOP CDM이 PostgreSQL과 SQL server script를 주로 지원하면서, 상용 DBMS(oracle, SQL server 등)을 쓰는 것이 아니라면 mySQL보다 postgreSQL으로 연습/사용하는 경우가 자주 있어 우선 PostgreSQL을 선택하였다. 
(PostgreSQL에서 사용하는 SQL은 PL/pgSQL이라고 한다.)   


### PostgreSQL server 설치
이 글에서는 클라우드 환경(AWS, GCP), local PC환경에서의 설치를 각각 설명한다. 

각자 본인의 컴퓨팅 환경에 맞게 시행하면 되는데, **"이게 무슨 말인지 모르겠다! 가장 기본인 내 PC설치를 해보겠다!"** 하면 
**2.2. install file download** 부분을 따라하면 된다. 클라우드 환경에서의 설치는 당연히 클라우드 비용이 발생하는 것이 default고 그때그때, 또는 경우에 따라 무료 티어/ 첫 사용자 크레딧 등에 따라 달라지기 때문에 아직 클라우드가 낯설고 SQL연습이 목적이라면 내 PC에 설치해서 진행하는 것을 강력히 권장한다.

#### 1. 클라우드 환경 
AWS, GCP등 클라우드 환경에서는 RDS 서비스를 통해서 몇 번의 클릭으로 쉽게 설치를 할 수 있다.
pgAdmin등의 GUI는 당연히 로컬에 별도 설치를 해야하며, 이 연습에서는 pgAdmin을 사용할 것이므로 다음 경로에서 다운로드, 설치한다.
[https://www.pgadmin.org/download/](https://www.pgadmin.org/download/)

#### 2. local computer (데스크탑, 노트북, 서버 등)
##### 2.1. docker 사용
docker를 사용한다면 다음과 같이 간단히 설치를 할 수 있다.

```
$ docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

##### 2.2. install file download
install file은 공식 홈페이지에서 받을 수 있다.
[https://www.postgresql.org/download/](https://www.postgresql.org/download/)

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/12fd6c40-3529-4a67-bbed-27581af61dfd)

나의 OS환경에 맞는 file을 선택, 다운로드 받은 후 실행하여 install하면 된다.

download installer 링크를 클릭해서 들어가면 다음 페이지로 포워드 되어 버전별, OS별 다운로드가 가능하다.
https://www.enterprisedb.com/downloads/postgres-postgresql-downloads

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/6bbb3b09-2663-404f-bf78-613715ef8bf2)

위 이미지에서처럼 내가 받고 싶은 버전과 내가 설치할 PC의 OS에 맞는 file을 다운로드 받는다.
보통은 가장 최신 버전을 권장하지만, 필요에 따라 위 예시에서처럼 특정 버전을 선택해서 설치할 수도 있다.

클릭하고 나면 다음과 같은 창이 뜨지만, 당황하지말고 get started 버튼에 낚이지말고 기다리면 된다. 
이미 다운로드중이다. (붉은 화살표 참고)

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/37c1dad7-467c-4196-b2db-742a6f609197)

다운로드 완료 알림이 뜨면 exe file을 실행시킨다.
window 사용자이면서 특별히 download 폴더를 변경한 적이 없다면, 탐색기에서 download에 가면 찾을 수 있다.

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/ad71069b-a525-4231-86e2-ac9e58da5078)

이런 창이 뜨면 성공. 이제 특이사항이 없다면 next만 연타하면 된다.

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/7c57a8b3-2400-4259-9fb4-d7ea7c71f583)

어디에 저장할지 폴더를 선택하는 화면.

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/54a7e781-b794-4424-a6d7-7579250e6234)

PostgreSQL(DBMS, server역할)과 SQL 쿼리를 보내고 받는데 필요한 프로그램/기능을 같이 설치해준다.

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/4af809ac-5a30-42d1-9e2c-c2d4dcbee0da)

DBMS이므로 PostgreSQL에 앞으로 데이터를 올린다/저장한다면 이 데이터 file들이 어디에 생성될지 위치를 지정하는 것이다.
연습용으로 작게 까는 경우는 특이사항이 없으므로 next를 연타하지만, 만약에 큰 데이터셋을 올려서 돌릴 예정이라든지, 
지속적으로 데이터가 커질 것으로 예상되는 작업을 위해서 서버를 설치하는 것이라면 당연히 용량이 넉넉한 storage를 선택해야한다.

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/f422d635-fa09-4928-b959-1691929902c2)

데이터베이스 superuser (관리자, admin역할)의 비밀번호를 설정한다.
처음부터 잊어버리면 이후에 매우 곤란하니 잘 기억해두도록 하자. DBMS는 권한설정이 매우 중요하긴 하지만, SQL연습 목적으로 내 PC에 DBMS를 설치하는 중이므로 앞으로도 superuser(이 창에서 읽어보면 ID는 postgre로 되어 있다.) = user(나) 인 상황에서 사용하게 될 것이므로 초심자는 이 단계에서 내 로그인 아이디와 비밀번호다, 생각해도 무방하다.

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/6651f8d6-8973-4140-a3b8-b5873fcf1128)

PostgreSQL의 default port는 5432이다. **초심자는 절대로 바꾸지 않도록 한다....**

![image](https://github.com/HyoJungKim/HyoJungKim.github.io/assets/25048006/f7cc9a36-14c9-4b8d-b328-62d77916b558)

마지막으로 앞 단계에서 하나씩 선택한 설정을 모아서 확인시켜준다. 
잘못된 것이 있다면 back으로 돌아가서 수정할 수 있다. 

이제 next를 클릭하면 설치가 시작되며, PC사양에 따라 다르지만 수 분 이내에 종료된다.

cmd console(커맨드창)에서도 PostgreSQL을 실행시키고 SQL 쿼리를 ~~날릴 수~~ 실행할 수 있지만 편리한 GUI인 paAdmin4가 함께 설치되어있으므로, 다음 글에서는 pgAdmin4를 실행하여 SQL을 연습해보자.

