# LLM_Based_OTT_recommender
Experiment that using LLM as a reward function in recommender system

## End-To_End experiment process
단계,주요 태스크,출력물
1. 전처리 및 메타데이터,"ID 매핑(1~N), 유저 시퀀스 분할, 전이 행렬 생성","Train/Val/Test Set, Transition Matrix, Genre Dict"
2. SASRec 베이스라인 학습,SASRec 모델 정의 및 시퀀셜 학습 (Next Item Prediction),Model Weights (유저의 다음 선호도를 예측하는 엔진)
3. 리스트 생성 및 LLM 개입,SASRec으로 Top-100 후보 추출 → LLM이 LTV 관점에서 Top-10 재정렬,Vanilla List vs LLM-Re-ranked List
4. 종합 평가 (Evaluation),"우리가 짠 단기(Recall, NDCG) 및 장기(Diversity, LTV 관련) 지표 계산",최종 비교 수치 및 연구 결론
