# 💳 Credit Card Fraud Detection System
> **딥러닝 기반 신용카드 이상거래(Fraud) 감지 프로젝트**


## 1. 프로젝트 개요 (Project Overview)
본 프로젝트는 약 28만 건의 신용카드 결제 트랜잭션 데이터를 분석하고, 딥러닝 모델을 활용하여 **정상 거래와 이상 거래(Fraud)를 분류해 내는 시스템**을 구축하는 것을 목표로 합니다. 

전체 트랜잭션 중 이상 거래의 비율이 극히 낮은 **불균형 데이터(Imbalanced Data)** 문제를 딥러닝 네트워크와 적절한 데이터 전처리 기법을 통해 어떻게 해결하고 모델의 예측 성능을 높였는지가 본 프로젝트의 핵심입니다.

## 2. 사용 데이터셋 (Dataset)
* **출처:** [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
* **데이터 크기:** 284,807건의 트랜잭션 데이터
* **특징:**
  * 고객의 개인정보 보호를 위해 대부분의 Feature(V1 ~ V28)가 PCA(주성분 분석)로 변환되어 있습니다.
  * 데이터 내 '정상 거래'와 '이상 거래'의 비율이 매우 불균형합니다 (이상 거래 비율 약 0.17%).

## 3. 기술 스택 (Tech Stack)
* **Language:** Python 3
* **Deep Learning Framework:** TensorFlow (Keras)
* **Data Analysis & ML:** Pandas, NumPy, Scikit-learn
* **Environment:** Google Colab Notebooks

## 4. 파이프라인 (Workflow)
1. **EDA (탐색적 데이터 분석):** 데이터 분포 및 변수 간 상관관계 파악
2. **Data Preprocessing (전처리):** * 결측치 및 이상치 처리
   * 시간(Time) 및 거래액(Amount) 피처 스케일링(Scaling)
   * 데이터 불균형 해소 (예: SMOTE, Undersampling 등 적용)
3. **Modeling (딥러닝 모델 구축):** * TensorFlow를 활용한 심층 신경망(DNN) 아키텍처 설계
4. **Evaluation (모델 평가):** * 불균형 데이터에 적합한 평가지표 사용 (정확도보다는 **Recall, Precision, F1-Score, AUC-ROC** 위주로 평가)

## 5. 실행 방법 (How to Run)
1. 본 저장소의 `credit_card_fraud_detection.ipynb` 파일을 다운로드합니다.
2. Google Colab 환경에 노트를 업로드합니다.
3. Kaggle에서 다운로드한 데이터셋(`creditcard.csv`)을 Colab 환경에 로드합니다.
4. 노트북의 모든 셀을 순차적으로 실행(Run All)하여 모델 학습 및 평가 결과를 확인합니다.
