---
title:  "Clinical Informatics: Bridge to reality." 
excerpt: ""

categories:
  - Blog
tags:
  - [Clinical informatics]

toc: true
toc_sticky: true
 
date: 2022-06-19
last_modified_at: 2022-06-19

---


## *Clinical Informatics: Bridge to reality.*



health informatics, medical informatics는 한 마디로 <u>"working definition이 없는 동네"</u>(feat. 언제나 clear한 지도교수님) 이라고 할 수 있습니다.

한 분지인 clinical informatics도 여기서 자유롭지 않습니다. 잘 살펴보시면 대부분 단어의 부연 또는 component의 집합으로 medical informatics를 설명하고 있는 것을 알 수 있는데 현재가 정말로 학문으로서 '초기'(많은 논문에서 infancy라고 표현하는) 단계에 있기 때문입니다. 

------

“Clinical Informatics promotes the understanding, integration and application of information technology in health care settings.” Those working in clinical informatics careers “ (HIMSS)

"**Clinical Informatics** is the application of informatics and information technology to deliver healthcare services. It is also referred to as applied clinical informatics and operational informatics." (AMIA)

-------



물론 학문으로서 상대적으로 'infancy' 이므로 일반인이 생각하는것 보다는 훨씬 오래됐습니다. academia는 통계도 젊은학문인 무서운 동네이니까요. 통계가 '근대적 경험과학 방법론'이라면 informatics는 그보다 더 '현대'에 가깝다고 가늠해 볼 수 있겠습니다. (닭이 먼저냐 달걀이 먼저냐를 적용하거나 '만물근원 정보설'과 같은 요즘 트렌드에 따르면 또 엄청 거슬러올라갈수도 있긴 합니다...)



각설하고, 그래서 **clinical informatics는 무엇이냐.** 

조금 더 tangible하게 설명하기 위해 아래 3가지 특성을 나열해 보겠습니다.

1. 일단 **응용학문**입니다. (applied science)

   이는 정답은 없고(!) 어제보다 **현실을** **발전**시키는 것은 유의미할 수 있습니다.

   <u>(주의. 정답이 없다고 오답이 없는건 아니고, 방법적으로 엄밀하지 않아도 된다는건 아닙니다)</u>

2. **clinical practice 와 관련된 모든 정보활동을 대상**으로 합니다.

   * EHR(병원정보시스템, electronic health recored)

     <span style="color:gray">(EHR이라는 말이 낯선 분이 계시다면.. 어디든 병원가시면 의사선생님들이 보고계시는 모니터! 그 안에 돌아가는 프로그램이 EHR입니다. 전자 차트라는 표현이 직관적이겠네요) </span> 

   * CPOE(처방정보시스템, computerized physician order entry) 

   ​       = OCS (처방전달시스템, order communication system)

   * CDW(임상데이터웨어하우스, clinical data warehouse)

   * CDSS(임상의사결정지원시스템, clinical decision support system)

   * CDM(공통데이터모델, common data model)

   * system design, implementation, adoption, evaluation... etc.

     ( 기술셋은 뭐든지 쓰일 수 있습니다. NLP, ML, DB, web, cs, .... 

     도메인도 마찬가지. knowledge engineering, system engineering, data architecture, data science, knowledge representation, design theory, information theory... ) 

3. **health professionals이 1차 사용자(?!)**가 됩니다.

   physicians, nurses, dentists, pharmacists, etc... 

   하지만 사용자 단위로 custom된 system을 사용할 수는 없기 때문에, clinic을 포함한 hospital, medical institution, sets of institution (....)을 염두에 두고 설계/개발/운용 되는 것이 바람직합니다. 



사실상 **health informatics분야에서 실질적으로 지속가능하게 돌아가고 있는 실체가 뭐냐! **했을 때 십중팔구 **EHR(!)**이 떠오르실 것입니다. <span style="color:gray">~~(그래서 BM으로 EHR을 잡고 테크쪽에서 진입하는 눈물없이 못볼 경우가 왕왕... 역사는 반복된다 급으로.. )~~ </span> 아마도 다음으로는 (3초 쉬고)  apple health와 같은 트래킹 앱이 생각나실 것이고.. 최근 디지털 치료제/혹은 중재로 제안되는 몇몇 앱들이 회자되지 않을까 싶네요. <span style="color:gray"><u>(보험, 제약, 정부기관 등등 까지 생각나셨다면 당신은 준프로이상!)</u></span>

이것이 health informatics에서 clinical informatics의, 그리고 또 다시 clinical informatics에서 EHR의 현실세계에서의 비중입니다. 

그런데 EHR은 그 단어가 우리와 친숙한 것과는 별개로 '워드프로세서' 같은 추상적인 상위 개념입니다. 우리는 '한글', 'MS word'는 직접 실체가 있고 구구절절한 기능을 서로 비교할 수 있지만, '워드프로세서' 는 그렇지 않죠. 그래서 **"우리병원에 'EHR' 도입이 진료에 도움이 되느냐!"** 같은 질문이 아니라 **"우리 병원에 '어떤' EHR이 도입되어야 목표를 달성할 것인가"**를 고민하고 구체적으로 물어야 합니다. 



예를 들어 "우리병원에 'EHR'도입이 진료에 도움이 될지"를 vendor에 물으면 답변이 돌아올 것이나 그것이야말로 답정너 아니겠습니까.. 그런데 병원종사자들은 일반적으로 안되는걸 된다고 말하는걸 상상해본 적도 없는 본인도 몰랐던 직업병을 가지고 있어 이런 안타까운 상황이 현실에서 종종 일어납니다.. 

*(그래서 한창 외주로 전환 트렌드였지만, 개인적으로는 IT와 관련된 의사결정조직정도라도 기관에 내재화되어있는 것이 이득이다!라고 생각합니다.)*



#### "대부분 우리는 아직 small data의 방식으로 big data를 다루고 있습니다."



일례로, NGS시대 이후 정밀의료, 맞춤의학은 어떻게 구현될까요?

진료의가 진료실에 들어오기 전 예진에서 잰 **혈압값 하나를 모니터에서 확인하듯이** 약 2만개의 알려진 유전자 중에 수백~수천개의 **actionable variant들을 눈으로 리뷰**하면서 환자의 주호소와 진찰 결과를 종합해서 진료를 보게 될까요? 오늘의 actionable variant guideline과 다음달의 그것은 심지어 다를수도 있습니다. 

정밀의료로 나아간다는 것은, 몇 개의 군으로 나누어서 해당되는 군에는 같은 치료를 한다. 는 방향에서 그 군의 크기를 개인의 수준까지 낮추고 정보의 범위를 유전체에까지 확장한다는 것으로, 의사결정에 고려하게 되는 정보의 총량이 폭발적으로 증가한다는 것을 의미합니다. 이 지점에서 IT기술의 활용은 선택이 아니라 필수가 되는 임계점이 있음을 확신할 수 있으며, **IT기술과 임상의 접점의 모든 장이 바로 clinical informatics입니다.**

<img scr="assets/images/이미지 18.jpg">

  <center> *"우리는 예전과 같은 일을 예전과 다른 방식으로 하게 될 것입니다" (feat. i-pad 광고)*</center>



**고로, clinical informatics는 미래의학에 대해 상상할 수 있는 거의 모든 것을 현실로 실현하는 장이자 방법에 관한 것이라고도 할 수 있겠습니다. **

**<span style="color:gray">*(~~학문으로서의 장래성과는 또 별개지만요 아하하하~~)*</span>**



그럼 다시 돌아와서 EHR이 다 같은 것이 아니라면 어떻게 요리조리 뜯어볼 수 있느냐!

이것을 다음주 쯤 작성할 다음글에서 살펴보도록 하겠습니다. :)


---
