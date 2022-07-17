---
title:  "EHR의 단위구성요소들" 
excerpt: ""

categories:
  - [CI_introduction]
tags:
  - [Clinical informatics]

toc: true
toc_sticky: true
 
date: 2022-06-26
last_modified_at: 2022-06-26

---


### EHR, 용어의 모호함

오늘은 EHR의 component들을 살펴보겠습니다.

저는 정확히는 HIS(Hospital information system)이라고 호칭하는 것을 더 선호하는데요, 

<span style="color:gray"> *(물론 논문쓸때는 EHR이라고 씁니다. 다들 그거! 하는게 그거죠.)*</span>



왜냐하면 EHR이 

1) 전자의무기록(=병원정보시스템) 

2) 서식 기록(경과기록, 입원기록 등과 같은)을 입출력하는 모듈
등으로 의미가 혼용되기 때문입니다. 


이는 당연히 국내만의 문제는 아니며 혹자는 다음과 같은 그림으로 표현하기도 하였습니다.
![image](https://user-images.githubusercontent.com/25048006/175821266-352b0846-1f5b-4a2c-b986-5fe2262f8b26.png)

_image reference: Hoyt, R. E., Sutton, M., & Yoshihashi, A. (2008). *Medical Informatics: Practical Guide for the Healthcare Professional 2008*. Lulu. com._

위 그림의 저자들도 일종의 예로 그림을 보여준 것이지, "no universally accepted definition of an EHR" 이라고 합니다.  _record는 무엇인가, data와 무엇이 다른가, medical과 health의 영역은 어떻게 구분할 수 있는가, 턱과 목의 경계찾기 같은 재미난 논의거리들이 그득하지만_ +_+ '바닥까지 파는' 것은 blog에서 할 일은 아니고, 오늘은 component를 설명에 집중해 보겠습니다.

> 다만, 이하에 논의할 단어들은 앞으로도 그 의미나 지칭이 변할 수 있다는 것입니다. 
> 따라서 통상적인 수준에서 연대기적으로 설명하겠습니다.

-------

### 순차적 component들의 등장

#### 원무시스템

**처음 등장한 HIS의 component는 '원무시스템'입니다.** (1970년대 후반, 국내)

그 시절을 생생히 경험하신 선구자들의 말씀을 들어보면, 종이 카드에 펀칭하던 이야기부터 흥미진진한 에피소드들이 가득합니다. 다만, 당시의 원무시스템은 HIS라고 해서 OA(사무자동화)의 다른 분야와 두드러지는 특성이 크게 발현되지는 않았습니다. 

(현재는 EDI청구부터 자격확인 등 많은 healthcare분야만의 로지스틱들이 들어가야 합니다)

우리나라에서는 78년 경희의료원 원무전산프로그램을 그 시작으로, 79년 서울대학교병원이 시작했습니다. 이하 연대기는 국내 기준입니다. (미국 기준은 [The History of Medical Informatics in the United States](https://link.springer.com/book/10.1007/978-1-4471-6732-7)와 같은 서적이나 웹에서 찾으실 수 있습니다. )



#### CPOE(OCS)

그 다음으로 **처방정보시스템(OCS, = CPOE)** 가 등장합니다. (1990년대 중반)

OCS라는 단어가 먼저 사용되었고 (order communication system), 나중에 CPOE(computerized physician order entry)라는 단어로 정리되면서 둘 다 혼용되지만 후자를 영미권에서는 좀 더 사용하는 것 같습니다. 개인적으로는 OCS가 더 직관적이어서 선호하지만, CPOE로 범용하는 것이 소통에 편리합니다. <span color = "gray">~~입에 붙은 단어로 연식이 느껴지기도.. 저도 OCS세대에 살짝 가까운..~~ </span>

처방정보시스템은 단순히 의사가 처방을 입력하면, 그것이 원무시스템(청구)와 간호, 약무국 등 처방을 전달받아 수행해야 하는 부서에서 확인하고 실행 로그를 관리/상호 전송하는 모듈로 출발합니다. 

직관적인 의미의 'communication'이 가장 핵심 기능이나, 현재의 CPOE는 매-우 복잡하고 EHR의 대부분의 주요 기능이 앞단, 즉 처방을 발생시키는 쪽에 집중됨으로써 많은 기능을 탑재하고 있습니다. 병원정보의 workflow의 흐름의 시작이자 종료점, intellegence part인 CDSS를 부가하고 싶다면 대부분 여기에 넣게 됩니다.



#### PACS와 EMR(서식기록)

다음으로는 **2000년대 초중반에 걸쳐 filmless hospital, paperless hospital을 표방하며 PACS, EMR(협의의)이 하나씩 도입, 부가**되면서 현재 저희가 생각하는 <u>(comphehensive) EHR(이하 EHR은 이 의미로 사용)</u>의 형태를 갖추게 됩니다. 각 대형병원들에서는 이때 엄청난 IT프로젝트를 수행했고, 저는 이때는 한 병원의 현업에서 "오픈 할 수 있는건가?" 하던 베타테스터(=사용자) 쪽에 있었음을 고백(?)합니다. ~~(전산원 전직 당시 모 업체 대리님이  "내가 해도 이거보단 낫겠다 하고 왔나요?" 하시던 생각이 나네요 아하하하 아닙니다!! )~~

PACS는 기존의 X-ray등 영상이 film없이 처방-장비-PACS system을 통해 전달되는 변화로 vendor driven이라고도 할 수 있습니다. "GE PACS를 도입했다" 와 같이 특정 밴더에서 개발한 시스템을 '도입'하는 개념이었고 선택지가 많지도 않았으며, EHR에 비하면 복잡하다고 할 수 없는 workflow를 커버하기 때문에.. 이때는 고민이 크지 않았습니다.

EMR은 기존의 입/퇴원기록, 경과기록, 수술기록, 간호기록, 병리결과지와 같은 서식(인쇄된 종이 쌓아놓고 한장씩 꺼내서 작성하던)이 전산화 된 것으로, 서식생성기(주로 의무기록실에서 담당) - 입력 부분으로 기능적으로는 분리될 수 있으며, 입력부분도 각 practice별로 처방(의사용) 프로그램, 간호(병동/외래) 프로그램, 진료지원(진단검사/병리검사/영양 등등) 각 단위 프로그램에 맞게 연결, 띄워주게 되지요. 



### comprehensive EHR 

OCS와 EMR이 결합된 광의의 EHR(당시는 이것도 EMR이라고 불렀습니다 ㅎㅎ)이 등장하면서 IT업계도 병원들도 동공지진..을 맞게 됩니다. 특히 국내에서는 각 대형병원들이 in-house로 개발을 했기 때문에 구성과 기능의 상호비교도 어렵고, 국외라고 해도 software이기 떄문에 구성과 기능이 구체적으로 알려지면 설계도가 나간 것과 같지 않겠습니까..? 그래서 EHR은 현재까지도 막연한 단어로 남고, 그 자체는 '워드프로세서'와 같이 실체가 있는 단어는 아닌데 많은 사람들에게 혼동을 불러일으키게 됩니다. ~~"그래서 EHR을 도입 하라는거야 말라는거야" 같은 질문을 양산..~~

u-severance, smith(현재의 Darwin), AMIS, BESTCare, nU 등등.. = EHR = EPIC, Cerner... 응?? 이렇게..


따라서, 이렇게 이해하는 것이 가장 정확한 출발입니다.

> "EHR은 여러 component로 이루어져있으며 주요 구성요소는 CPOE, EMR, LIS, PACS, 원무시스템이다. "

CDSS는 주요 구성요소라고도 할 수 있지만 component보다는 기능 레이어에 위치하기 떄문에 별도로 논의하도록 하겠습니다. LIS(Laboratory information system, (진단)검사정보 시스템)은 장비 위주로 이미 독자적으로 발달된 것이 comphrehensive EHR의 시작에 당연하게 와서 연결된 부분이 강해서 따로 위에 시기별로 언급하지는 않았습니다.~~(이런 흐름을 볼 때 genomic data는 EHR에 GIS의 형태로 붙을 것이고, 그때 원천기술로 필요한 것은 지식표현이며, 그 데이터 모델을 제안해보겠다는게 [저의 논문](https://www.nature.com/articles/s41598-020-58088-2)의 인트로(Figure 1)가 됩니다. 꺄륵)~~

-------

### 마치며

EHR의 intellegence의 핵심인 ***CDSS(clinical decision support system, 임상의사결정시스템)***와 HIS의 주요 컴포넌트의 하나인 ***CDW(clinical data warehouse)*** 가 남았네요. 다음 2주에 걸쳐 각각에 대해서 별도의 글로 살펴보고, HIS와 상응되는 또 다른 큰 축인 ***PGHD(=PHR, 개인건강기록)*** 에 대해서도 다루어보겠습니다.
