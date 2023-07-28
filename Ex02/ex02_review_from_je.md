# AIFFEL Campus Online 4th Code Peer Review Templete
- 코더 : 코더 1인의 이름을 작성하세요.
- 리뷰어 : 본인의 이름을 작성하세요.


# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.
- [x] 1.코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
- [x] 2.주석을 보고 작성자의 코드가 이해되었나요?
  > 각 단계마다 코드 역할에 대한 주석이 잘 적혀 있어서 이해하기 편했습니다.
- [x] 3.코드가 에러를 유발할 가능성이 있나요?
  > 
- [ ] 4.코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 깔끔한 코드인데 리뷰 시간에 코드 자랑을 덜 해주셔서 아쉬웠습니다... 평가지표 ROUGE점수까지 사용하신 점이 인상 깊었는데, ROUGE 점수에 대해서 더 알아보고 이해할 수 있었으면 더 좋은 피어리뷰 시간이었을 것 같습니다 
- [x] 5.코드가 간결한가요?
  > 짧고 효율적인 방법이었습니다!

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 정수 인코딩하고 패딩 부분에서, 
X_train_pad = pad_sequences(X_train_seq, maxlen=30, padding='post')
X_test_pad = pad_sequences(X_test_seq, maxlen=30, padding='post')
Y_train_input = pad_sequences(Y_train_seq, maxlen=8, padding='post')
Y_test_input = pad_sequences(Y_test_seq, maxlen=8, padding='post')
# maxlen을 각각 30, 8로 잡은 게 성능이 안나오는 원인 중 하나가 아니었나 생각이 듭니다! 전처리 과정이 조금 달라서 문장 길이가 조금 다를 수는 있지만 저는 문장 길이 평균이 35정도 나오던데, 30으로 제한하면서 많은 내용이 날라가지 않았을까하는 아쉬움이 있네요. 헤드라인 길이도 마찬가지로 조금 더 길게 설정하면 더 많은 정보를 가지고 학습할 수 있었을 것 같습니다

# 모델 평가 부분에서 핵심 단어 포함되어 있는지 확인하는 부분 코드를 확인하니
    # 요약문에 핵심 단어가 포함되어 있는지 확인
    contains_key_phrases_abstract = contains_key_phrases(abstract_summary, keywords)
    contains_key_phrases_extractive = contains_key_phrases(extractive_summary, keywords)
# 대충 문장안에 keywords에 속한 단어가 얼마나 들어가는지 확인하는 것 같은데, 각 기사마다 keywords를 실제로 추출해서 확인하는 과정이 있었으면 더 정확했을 것 같습니다!
```

# 참고 링크 및 코드 개선
ROUGE score에 관한 블로그 두가지
[Rouge score - Summarization의 평가 Metric](https://velog.io/@crosstar1228/NLPRouge-score-Summarization%EC%9D%98-%ED%8F%89%EA%B0%80-Metric)
[ROUGE score: Recall-Oriented Understudy for Gisting Evaluation](https://supkoon.tistory.com/26)