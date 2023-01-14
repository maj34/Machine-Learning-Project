# 백화점 고객들의 인구 통계 예측 대회
Predicting Demographics Contest of Department Store Customers 

<br/>

## 1. 배경 & 목적

- 백화점 고객들의 정보를 가지고 정확한 연령을 예측하는 회귀 문제
- 평가지표 : RMSE

<br/>

## 2. 주최/주관 & 팀원

- 주최: 2021 Machine Learning Class
- 주관: Kaggle Inclass Competition
- 팀원: 전공생 2명

<br/>

## 3. 프로젝트 기간

- 2021.05. ~ 2021.06. (2개월)

<br/>

## 4. 프로젝트 설명

&nbsp;&nbsp;&nbsp;&nbsp; 백화점 고객들의 정보를 담고 있는 데이터 셋을 가지고 **사용자의 정확한 연령을 맞추는 회귀 문제**이다. 피처 엔지니어링을 하기 전 원본 데이터에서 **날짜와 시간을 처리**해주었고, **정규표현식**으로 특수기호를 제거해주었으며 **중복되는 상품을 하나의 이름으로 통일**해주는 전처리를 거쳤다. 피처 엔지니어링은 수치형 피처 1,498개, 범주형 피처 2,309개, W2V 피처 1,950개로 **총 5,757개의 피처**를 만들어냈다. 피처 핸들링 과정에서는 다양한 PCA와 이상치 처리 등을 시도했지만 결과적으로 모델링 결과 성능이 가장 좋았던 **Standardization과 Feature Selection 과정**만 거쳤다. 

&nbsp;&nbsp;&nbsp;&nbsp; 모델링은 **선형회귀 모델**(LinearRegression, Lidge, Lasso, ElasticNet, ARD, BayesianRidge), **트리 계열 모델**(DecisionTree, RandomForest, GradientBoosting, XGBoost, LGBM, Catboost), **KNN, SVR, MLP** 등 정말 많은 회귀 모델을 실험해보았다. 그 결과 **LGBMRegressor 모델을 Bayesian-Optimization으로 튜닝**한 결과가 성능이 가장 좋게 나왔다. 또한 Keras 라이브러리를 사용해서 Seed Ensemble을 한 DNN도 실험해보았다. 최종적으로는 **LGBM 모델과 DNN 모델을 weight 가중치를 두어 Soft-voting**한 것이 가장 성능이 좋아 최종 모델로 선정했다.

<br/>

## 5. 프로젝트 담당 역할

- 데이터 전처리 및 피처 엔지니어링
- 선형 회귀 모델, 트리 계열 모델 모델링 및 하이퍼 파라미터 튜닝
- Seed Ensemble, Soft-Voting, Submission Weight Ensemble

<br/>

## 6. Process

### ch.1 Preprocessing

- Hour/Date Data Handling
- Regular Expression
- Deduplication

---

### ch.2 Feature Generation

- Numeric Features
- Categorical Features
- Word2Vec Features

---

### ch.3 Feature Handling

- Standardization
- Feature Selection

---

### ch.4 Modeling

- Machine Learning Model Modeling
    - LinearRegression, Lidge, Lasso, ElasticNet, ARD, BayesianRidge
    - DecisionTree, RandomForest, GradientBoosting, XGBoost, LGBM, Catboost
    - KNN
    - SVR
    - MLP
- Machine Learning Model Tuning
    - Bayesian-Optimization
- Deep Learning Model Modeling
    - DNN

---

### ch.5 Ensemble

- Seed Ensemble
- Soft Voting
    - LGBM Bayesian-Optimization
    - DNN Model
- Submission Weight Ensemble

<br/>

## 7. 증빙자료

[Kaggle KML Challenge 2021S](https://www.kaggle.com/competitions/kml2021s/leaderboard)
