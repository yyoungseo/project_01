# 👩🏻‍💻 공유 오피스 무료 체험 사용자의 결제 전환 예측 모델 개발
<div align="center">
  
![보고서 pptx](https://github.com/user-attachments/assets/25e45e21-ce63-4921-b159-9ef6c0ae43ea)
</div>

## ✅ Key Project Details
- 데이터: 2021년 5월부터 2023년 12월까지 2년 8개월간의 공유 오피스 서비스 이용 데이터 활용
- 분석 및 전처리: 체험 신청, 방문 기록, 결제 여부 등 다양한 테이블을 통합하여 머신러닝에 적합한 피처 생성
- 모델링: RandomForest모델과 하이퍼파라미터 튜닝을 통해 결제 전환 예측 성능 극대화 (최종 F1-Score 0.56)
- 핵심 변수: 체류 시간, 입실 및 퇴실 시간, 방문 빈도, 이벤트 참여 횟수 등 사용자 행동 패턴이 결제 전환에 큰 영향
- 활용 방안: 예측 모델을 통해 결제 가능성이 높은 사용자 타겟팅 및 맞춤형 마케팅 전략 수립 가능

<br />

## 📖 Table of Contents
- [📨 Project Overview](#📨-Project-Overview)
- [Selected Machine Learning Model & Evaluation Metrics](#Selected-Machine-Learning-Model-&-Evaluation-Metrics)
  - [RandomForest](#RandomForest)
  - [F1-Score](#F1-Score)
- [Project Tree](#Project-Tree)

<br />

## 📨 Project Overview
2023년 3월부터 공유 오피스 무료 체험 방문자는 꾸준히 증가했으나, 결제 전환율은 오히려 감소하는 현상이 관찰되었습니다. 이에 체험 신청부터 방문 행동 데이터를 기반으로 결제 전환 가능성을 예측하는 머신러닝 모델을 개발하여, 사용자 맞춤형 마케팅 전략 수립과 실질적인 결제 전환율 향상을 목표로 하였습니다.

<br />

## Selected Machine Learning Model & Evaluation Metrics
### RandomForest
- 앙상블 학습 기법(배깅) 기반
  - Random Forest는 여러 개의 독립적인 결정 트리(Dicision Tree)를 학습시킨 후 그 결과를 종합해 최종 예측을 수행하는 앙상블 기법 중 배깅(Bagging) 방식을 사용합니다.
  - 이는 단일 결정 트리가 가질 수 있는 과적합(Overfitting) 문제를 효과적으로 줄여주며, 모델의 예측 성능과 안정성을 높여줍니다
- 비선형 관계 학습 능력
  - 사용자의 3일 체험 행동 패턴(방문 시간, 체류 시간, 방문 순서 등)은 결제 여부와 복잡하고 비선형적인 관계입니다.
  - 트리 기반 모델인 RandomForest는 이러한 비선형적인 패턴과 피처 간의 상호작용을 잘 학습하는 능력이 뛰어납니다.

<br />

### F1-Score
- 정밀도와 재현율의 평균
  - F1-Score는 재현율과 정밀도, 두 지표의 균형을 중요하게 평가합니다.
  - F1-Score를 개선한다는 것은 정밀도와 재현율 모두를 합리적인 수준으로 높인다는 의미입니다.
  - 모델이 ‘긍정’을 예측하는 정확도와 실제 ‘긍정’을 찾아내는 능력을 동시에 향상시키는 것을 쉽게 파악할 수 있습니다.
- 클래스 불균형 데이터에서의 유용성
  - 정확도는 클래스 불균형이 심한 데이터에서 다수 클래스를 잘 맞추는 것만으로도 높게 나올 수 있어 모델 성능을 정확히 판단하기 어렵습니다.
  - F1-Score는 소수 클래스에 대한 정밀도와 재현율을 기반으로 계산되므로, 클래스 불균형 데이터에서 모델 실제 성능, 특히 소수 클래스를 얼마나 잘 예측하는지를 더 잘 반영합니다.
  - 현 데이터에서 결제 예측 클래스의 불균형 비율이 1.63입니다.
  - 이런 경우, F1-Score를 개선하는 것은 모델이 실제 결제 사용자를 얼마나 효과적으로 식별하는지를 나타내는 중요한 지표입니다.
- 단일 지표로 성능 비교 용이
  - 정밀도와 재현율 두 지표를 동시에 고려해야 할 때, F1-Score는 이 둘을 종합한 단일 지표로서 모델 간 성능을 비교하거나 하이퍼파라미터 튜닝 시 최적화 목표로 설정하기 편리합니다.
- 비즈니스 목표와의 연관성
  - 많은 실제 문제에서 정밀도와 재현율 모두 중요합니다.
  -  결제 예측의 경우
      - 높은 정밀도: ‘결제할 것이다’라고 예측된 사용자에게 마케팅 비용이나 리소스를 투입했을 때, 실제로 결제로 이어질 확률이 높다는 의미 (비용 효율성)
      -  높은 재현율: 실제 결제할 가능성이 있는 사용자를 최대한 많이 찾아내어 놓치지 않는다는 의미 (잠재 고객 확보)
  - F1-Score 개선은 이 두 가지 측면을 동시에 고려해 모델의 실용적인 가치를 높이는 데 기여합니다.

<br />

## 예측 모델 활용 (비즈니스 마케팅)

<br />

## Project Tree

<br />

## 🛠️ Development Environment and Tools
- Data Analysis: 	<img src="https://img.shields.io/badge/python-%233776AB.svg?&style=for-the-badge&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/mysql-%234479A1.svg?&style=for-the-badge&logo=mysql&logoColor=white" />
- Data Visualization: 	<img src="https://img.shields.io/badge/python-%233776AB.svg?&style=for-the-badge&logo=python&logoColor=white" /> <img src="https://img.shields.io/badge/tableau-%23E97627.svg?&style=for-the-badge&logo=tableau&logoColor=white" />
- Collaboration Tools: <img src="https://img.shields.io/badge/discord-%237289DA.svg?&style=for-the-badge&logo=discord&logoColor=white" />	<img src="https://img.shields.io/badge/notion-%23000000.svg?&style=for-the-badge&logo=notion&logoColor=white" />

## 🍀 Team Members
#### 🐻 윤영서
#### 🦊 심태윤
#### 🐶 강주희

## ✈️ Project Duration
- 2025.06.09 - 2025.06.18

## ⛓️ Project Collaboration
- Google Colab을 통해 ipynb 파일로 code를 공유했습니다.
- Discord를 통해 일간화의를 진행하며 작업 순서와 진행 사항을 파악하였으며, Notion에 회의 내용을 기록했습니다. 
