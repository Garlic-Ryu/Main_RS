## 최종 프로젝트 목표
### 네이버 영화리뷰 감정 분석 문제에 SentencePiece 적용해 보기
- SentencePiece: 구글의 오픈소스 문장 토크나이저
    - 바이트 페어 인코딩(BPE), 유니그램의 2가지 서브워드 토크나이즈 모델 사용 가능
    - 단어 사전의 수를 고정시키는 것이 특징
    - 사전 토큰화 불필요함 (일본어나 중국어처럼 띄어쓰기 없어도 가능)


### 주요 개념
- 서브워드 토크나이저
- [﻿BPE ](https://ratsgo.github.io/nlpbook/docs/preprocess/bpe/) 
    - 왜 쓰는가?
    - 강점과 단점
- 유니그램
- 워드피스
- [﻿유니코드 정규화 방법](https://unicode.org/reports/tr15/) 


### 기초 개념
- 어절: 띄어쓰기 단위, 자연어 처리에서는 문자열 형태
- OOV: Out of Vocabulary Words, 임베딩 벡터로 처리되지 않은 단어나 단어 주머니 등 사전에 마련한 데이터 목록에 존재하지 않는 자연어 토큰

### 평가 문항
1. SentencePiece를 이용하여 모델을 만들기까지의 과정이 정상적으로 진행되었는가?
- [ ] 코퍼스 분석, 전처리, SentencePiece 적용, 토크나이저 구현 및 동작이 빠짐없이 진행되었는가?

2. SentencePiece를 통해 만든 Tokenizer가 자연어처리 모델과 결합하여 동작하는가?
- [ ] SentencePiece 토크나이저가 적용된 Text Classifier 모델이 정상적으로 수렴하여 80% 이상의 test accuracy가 확인되었다.
   
3. SentencePiece의 성능을 다각도로 비교분석하였는가?
- [ ] SentencePiece 토크나이저를 활용했을 때의 성능을 다른 토크나이저 혹은 SentencePiece의 다른 옵션의 경우와 비교하여 분석을 체계적으로 진행하였다.

https://github.com/Woodywarhol9/aiffel/blob/main/Exploration/project/%5BE7%5Dsentiment_classification_naver.ipynb 이 코드를 많이 참고하였습니다. 
아직 이해가 된 부분이 아니라 추가적으로 학습이 필요합니다.

