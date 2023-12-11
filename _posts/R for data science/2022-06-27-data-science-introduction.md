---
title:  "Data science: introduction" 
excerpt: "Data science, R과 python을 활용한 기초를 설명합니다."

categories:
  - R for data science
tags:
  - [Clinical informatics,Data Science,Concept]

toc: true
toc_sticky: true
 
date: 2023-12-11
last_modified_at: 2023-12-11
---

### 무작정 R 시작하기 
R을 재설치 할 기회가 있어 R, R studio 설치부터 설명해보려고 합니다.
Data science, R이냐 python이냐 하는 문제에 대해서는 나중에 별도의 글로 작성하겠습니다.

이 글에서는 **1) R을 설치**하고, **2)R studio를 설치**할 것입니다.
인터넷과 PC사양에 따라 다르겠지만, 5분~10분 컷 예상합니다.

R studio는 R의 사용자 편의를 증진시켜주는 대표적인 IDE(integrated development environment,통합개발환경)로 코드 이력관리나 변수조회, 그래프 출력/저장 등이 편리합니다. 
R studio를 꼭 써야 하느냐! 이건 사실 선택이고 R만 사용하는 분들도 꽤 계시지만 제 블로그의 기술 설명들은 초보 사용자부터 super user까지 user에 철저히 맞춰질 예정이므로, 편의성 증진은 매우 중요하므로 R studio까지 설치하고, 이것을 기본으로 사용하도록 할게요. 

### R 설치

포털 등에서 R download를 검색하면 다음 사이트를 찾을 수 있습니다.
https://cran.r-project.org/

여기서 각자 본인 컴퓨터의 OS에 맞는 링크를 클릭하여 들어갑니다. 
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/fb8ebe0a-67be-41f5-85a4-a8295412806f)

저는 windows 버전을 선택하였습니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/90553efc-515f-4ac3-b112-5b49c1e822b4)

다운로드 받은 exe file을 실행합니다.
(window OS의 경우 우클릭 -> 관리자권한으로 실행을 생활화하면 편리합니다.)

![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/198c8d8b-d96f-48ee-a159-eb9fa22aec4f)

설치는 한국어도 가능합니다. 저는 가끔 어색한 한영번역이 더 헷갈리는 경우도 있고, 소통을 위해서 영어 원어를 알아야 하는 경우도 있어서 영어를 선택했습니다.
(~~왠지 학기초에는 원서를 사면 공부할 것 같은 마음이죠~~)

Next를 한 번 눌러주고, 
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/f3c7d7fd-78d0-4f9b-8ba3-12e3b501d500)

설치폴더를 선택합니다. 
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/45746202-99ca-489a-a2d7-33c1e81277ca)

무작정 설치하기이니까 default 값으로 쭉쭉 넘겨줄 거에요. 추후 사용에 별 문제 없습니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/d6583f71-cbc6-41c6-9715-e7549d879802)
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/75f22656-758a-4c97-9469-9435fe2f4d7f)
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/b1f30fe2-b104-437e-a51d-305b6f45de43)
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/6855c888-cfdf-41e0-a986-86f4b4c560d4)
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/717bd144-343e-4493-9468-c83b79a86883)

끝났네요
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/41f5183d-3e76-4a8b-9993-38b2c1531696)


바탕화면에 예쁜 아이콘이 생겼을거에요.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/51e41fbd-b3ea-4b4e-bc41-1c5003fe391e)

더블클릭!
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/8c4369e2-2664-435e-a49a-103a7ebd0829)

저는 재설치라 맨 아래에 [이전에 저장한 작업공간을 복구하였습니다]
한 줄이 더 뜨네요. 

여기까지 오셨으면 설치 끝! 
그냥 나가기 서운하니까 모든 프로그래밍 입문 밈인 hello world를 한 번 쳐주고 모든 창을 닫아 종료하겠습니다. :) 

``` print("Hello world!") ```
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/1f49a2dc-a9db-460d-b26e-8c3da8c2f0ea)

( 창 닫을 때 "작업 공간 이미지를 저장하시겠습니까?" 물어보는데, 아니오 하고 나오시면 됩니다.)

### R stuido설치

공식사이트에서 다운받습니다. 
https://posit.co/downloads/

고맙게도 R studio desktop은 무료배포에요.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/2f7a09a9-dedb-4008-a4a5-50de84b6a75d)

https://posit.co/download/rstudio-desktop/

R은 설치했으니 2: Install RStudio를 클릭해줍니다.
저는 windows OS라서 바로 파란 버튼을 클릭했고, 다른 OS사용자분들은 아래 보라색 네모로 표시된 영역에서 본인 OS에 맞는 file을 다운로드 해주시면 됩니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/effd4e05-c926-4d65-a659-1553a74f6389)

다운로드 받은 실행 파일을 (파일명.exe) 실행합니다.
(윈도우 사용자여러분은 혹시 모를 에러 방지를 위해 우클릭 -> 관리자권한으로 실행 해주세요)
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/f3a7a211-8c4f-4238-91e2-2e009512b286)

다시 다음다음 Next Next 클릭할 시간이 돌아왔네요.
물론 원하시면 설치폴더를 바꿔줍니다. 전 게을러서 그냥 합니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/e314ba46-52b8-47f0-b723-c301f1b7b2bf)

바탕화면 아이콘 만들어줄지 물어보고
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/0d02cffd-d8fe-4700-a9cd-b1932be1e4f4)

쭉쭉 설치합니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/7695e3fa-5509-4e21-b9d4-c5f1e25b7d22)

스크린샷 붙여넣는 사이 끝났습니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/73d65069-7c9d-45bf-8bf8-ef7fc176c675)


### R studio 실행

R studio 아이콘은 이렇게 생겼습니다. 더블클릭해서 실행. 
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/77462c4f-5fb6-4b88-be95-031fcd229f12)

첫 실행이라서 이 R studio에서 어떤 R 버전을 쓸지 물어봅니다. 처음 까는 분들을 가정하고 말씀드리고 있으니, 여기선 바로 OK하시면 됩니다.
![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/226470a2-c468-4061-83e3-578ce2f25133)

조금 부연설명 드리면, 제 경우 스크린샷의 아래 회색글씨 부분에 [64-bit] C:\Programfiles\R\R-4.3.2 라고 나오는데요, 지금 이 PC에 설치된 R의 여러 버전들을 모두 보여줍니다. 현재 제 PC에는 4.3.2버전 R 하나만 깔려 있어서 한 줄만 보이고 있습니다. 과거 버전에서만 동작하는 패키지를 아직 써야 한다든가, 새 버전 R을 설치하긴 했지만 아직 메인으로 쓰고 싶진 않다거나 하면 과거 버전을 선택할 수도 있겠지요.

R stuido 화면이 나왔네요!

![image](https://github.com/HyoJungKim/FAERS_Data_for_Investigating-the-Safety-of-Fast-Track-COVID-19-Drugs/assets/25048006/2bad94d9-3cdc-4b2b-b1fa-7ca3e6e63dba)

네 개의 창으로 분할된 화면이 뜹니다. 여기 보시면 왼쪽 아래가 아까 실행했던 R과 같죠!
왼쪽 위가 주로 여러분이 스크립트를 작업하실 공간이고, 우측 상단은 만든 변수들과 거기 저장된 값의 요약을 보여줍니다. 우측 하단은 그래프 등을 보여주고 저장하는 등의 용도를 가지고 있어요.

모든 기능을 다 쓸 필요는 없고, 일단 하나하나 해봅시다. 
R은 통계 패키지인데, 통계... 자신 있으실까요?
통계 따로 R따로 하지 말고 같이 가르쳐주는 멋진 패키지가 있습니다. 

다음 글에서 이어서 따라해볼게요!
