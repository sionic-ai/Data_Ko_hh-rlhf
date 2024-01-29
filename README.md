# Data_Ko_hh-rlhf

# Ko_hh-rlhf
https://github.com/anthropics/hh-rlhf 테스트 데이터 한국어 번역

- 번역은 DeepL을 사용하였고 일관성 없이 번역되는 용어들은 수정하였으나 일부 남아 있을 수 있음
- **데이터에 불쾌할 수 있는 내용이 포함되어 있으니 주의를 요함**


# 개관

- 불쾌한 언어 표현뿐만 아니라 미묘하게 해로운 비폭력, 비윤리적 출력까지 검증할 수 있는 데이터 세트   
-  유해한 출력을 줄이기 위한 공격 데이터 세트로구축      
- 거절(Reject)하는 대화 유형이 포함되어 있음
- 매개 변수 2.7B, 13B, 52B  와 4가지 모델 유형을 통해 검증, 인간 피드백(RLHF)를 통한 강화 학습에 사용하여 무해하도록 모델 훈련



인간과 인공지능 어시스턴트의 대화 시나리오로 인공지능을 공격하는 데 성공하였으면 4점, 실패하면 0점



## 방법

- 작업자 스트레스를 줄이기  위한 설계 : (1) 업계 전문가와의 인터뷰 진행  ,  (2) 민감한 콘텐츠에 노출될 수 있다는 경고를 명시화, 설문 조사와 비공식적 피드백을 통해 스트레스 정도 측정
- 과제 진행 프로세스 :  과제 동의> 인공지능 어시스턴트와 개방형 멀티턴 대화 진행
- 참가자: 두가지 가능한 응답을 제시하고 더 해로운 응답에 체크

## 데이터의 의의

- 응답을 두 가지 방향으로 제시했기 때문에 시스템의 취약점을 찾는 속도를 두 배로 높일 수 있음
- 선호도 모델을 사용하여 안전 개입을 구축
- 유해하다는 복잡하고 주관적인 개념을 정의하는 대신 대화쌍별 선호 선택을 통해 스스로 결정하도록 함

## 논의 사항

- 초기 비윤리 연구 또는 부적절 대화에 대한 연구와 데이터는 댓글 등에서 욕설이나 명시적으로 다른 사람을 공격하는 유해한 표현에 대한 검색이 주요 목적이었음.
- 최근의 연구에서는 비윤리적인 표현이 없지만 인공지능에게 물었을 때 적절한 답변을 얻을 수 없는 윤리적인 질문인가 자체에 논의의 초점이 맞춰지고 있는 추세임
- 이때 인공지능의 답변이 불편하게 느껴질 수 있도록 출력되는 것을 포괄하여 부적절 발화 데이터로 보고 이와 관련된 논문이나 데이터가 구축되고 있는 추세
- 생성 모델의 학습 데이터로 입력될 수 있는 질의응답 중 불편한 내용이 담겨 있는 데이터의 구축에서 뜨거운 감자와 같은 논의는 데이터 공개에 초점이 맞추어져 있음
- 지금은 주의가 필요하다는 경고성 문구를 추구하고 있는데 추가적인 논의가 필요함
- 이와 관련하여 이 논문에서 “궁극적으로 데이터 세트를 공개하는 것이 잠재적인 피해보다 연구 커뮤니티에 더 많은 이득을 가져다줄 것이라고 생각했지만, 이 결정은 진공 상태에서 내린 것”이라고 한 언급은 주목할 만함


- 데이터를 번역한 것과 관련하여 데이터의 의의 및 고려해야 할 점등에 대한 의견은 다음 블로그에도 제시하였음
https://blog.sionic.ai/red-teaming-language-models-to-reduce-harms

# 데이터 출처
```
@unknown{unknown,
author = {Ganguli, Deep and Lovitt, Liane and Kernion, Jackson and Askell, Amanda and Bai, Yuntao and Kadavath, Saurav and Mann, Ben and Perez, Ethan and Schiefer, Nicholas and Ndousse, Kamal and Jones, Andy and Bowman, Sam and Chen, Anna and Conerly, Tom and DasSarma, Nova and Drain, Dawn and Elhage, Nelson and El-Showk, Sheer and Fort, Stanislav and Clark, Jack},
year = {2022},
month = {08},
pages = {},
title = {Red Teaming Language Models to Reduce Harms: Methods, Scaling Behaviors, and Lessons Learned},
doi = {10.48550/arXiv.2209.07858}
}
```
