# Naver-movie-reviews-classification(네이버 영화 리뷰 감정 분류)

## 💬프로젝트 내용
1. **주제** : **네이버 영화 리뷰 감정 분류**
2. **구성원** : **이종원(개인 프로젝트)**
3. **진행기간** : **2023.01.18~2023.01.24(진행중)**


## 👻프로젝트 목적
1. 한글 텍스트 분류를 다양하게 진행함으로서 Word Representaion과 Text Classifiction에 대한 이해 함양.
2. scikit-learn의 다양한 모델과 기술을 활용하여 scikit-learn 라이브러리에 대한 이해 함양.
3. 다양한 word representation model, classification model, stacking모델을 사용하여 정확도를 높히는 일련의 과정 경험.

## 😎프로젝트에서 사용할 기술들
* **Preprocessing Method**
  - **KoNLPy Okt** : 형태소 추출
  - **regex** : 정규 표현식, 특수문자 처리
  - **stop word** : 불용어 처리

* **Word Representation**
  - **TD-IDF**
  - **Word2Vec**
  - **Tokenizer + Padding**

* **Classifiction Model**
  - **ML Model** : Logisic Regression, Random Forest, Decision Tree, XGBoost
  - **DL Model** : RNN, CNN(Convolution Neural Network for Sentence Classifiction - Yoon Kim(2014))
  - **stacking** : 과적합 방지를 위한 CV 기반의 stacking 모델

* **Search Parameter**
  - **Bayesian optimization** : 베이지안 네트워크 최적화를 통한 최적 hyperparameter 탐색.
  - **Grid Search** : Grid Search CV를 통한 최적 hyperparameter 탐색

* **train/test split**
  - **KFold Cross Validation** : 과적합 방지를 위한 KFold train/test Split 사용. 

* **Metric**
  - **Accuracy** : 평가 지표로는 정확도만 사용하였습니다.

## 🤑**Model Accuracy Result**

|Word Representation|Model|Eval Accuracy(%)|Predict Accuracy(%)|
|--|--|--|--|
|**Word2Vec**|**LogisticRegression**|$0.8002$|$0.8029$|
|**Word2Vec**|**RandomForestClassifier**|$0.8017$|$0.8064$|
|**Word2Vec**|**XGBClassifier**|$0.8062$|$0.8035$|
|**Word2Vec**|**DecisionTreeClassifier**|$0.7164$|$0.7281$|
|**Word2Vec**|**CNN**|||
|**Word2Vec**|**RNN**|||
|**TF-IDF**|**LogisticRegression**|$0.8501$|$0.8620$|
|**TF-IDF**|**RandomForestClassifier**|$0.8106$|$0.7949$|
|**TF-IDF**|**XGBClassifier**|$0.7831$|$0.7282$|
|**TF-IDF**|**DecisionTreeClassifier**|$0.7308$|$0.6700$|
|**TD-IDF**|**DNN**|||
|**Tokenizer + Padding**|**LogisticRegression**|$0.5154$|$-$|
|**Tokenizer + Padding**|**RandomForestClassifier**|$0.6353$|$-$|
|**Tokenizer + Padding**|**XGBClassifier**|$0.6961$|$-$|
|**Tokenizer + Padding**|**DecisionTreeClassifier**|$0.6054$|$-$|
|**TD-IDF**|**DNN**|||
|**Tokenizer + Padding**|**CNN**|||
