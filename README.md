###심장 질환 예측 모델

이 프로젝트는 심장 질환 예측을 위해 DNN을 사용한 모델을 구축한 것입니다. 
다양한 건강 지표를 기반으로 심장 질환 유무를 이진 분류하는 모델입니다. 
PyTorch 라이브러리를 사용하여 모델을 구현하였고, Dropout과 Batch Normalization을 통해 과적합을 방지하고 성능을 향상시켰습니다.

##데이터 출처 

https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset

## 데이터

'age': '나이',​</br>
'sex': '성별',​
'cp': '흉통 유형 (4가지 값)',​
1: 전형적인 협심증 (Typical angina)​
2: 비전형적인 협심증 (Atypical angina)​
3: 비협심증성 통증 (Non-anginal pain)​
4: 무증상 (Asymptomatic)​

'trestbps': '휴식 시 혈압',​
'chol': '혈청 콜레스테롤 (mg/dl)',​
'fbs': '공복 혈당 > 120 mg/dl',​
'restecg': '휴식 시 심전도 결과 (0, 1, 2)',​
'thalach': '최대 심박수',​
'exang': '운동 유발 협심증',​
'oldpeak': '운동 상대 안정시 ST 저하',​
'slope': '최대 운동 ST 세그먼트의 경사도',​
'ca': '형광투시법에 의해 색칠된 주요 혈관 수 (0-3)',​
0: 색칠된 혈관이 없음.​
1-3: 주요 혈관에 차단이 있는 수로, 1은 하나의 혈관, 2는 두 개의 혈관, 3은 세 개의 혈관에 차단이 있음을 의미​
'thal': '탈 (0=정상, 1=고정 결함, 2=가역적 결함)'

목표 변수(target): 심장 질환의 존재 여부 (1: 있음, 0: 없음)

모델 구조
입력층: 특징을 입력받는 부분
히든층: 두 개의 완전 연결층(Fully Connected Layer)과 ReLU 활성화 함수
배치 정규화: 각 층의 출력을 정규화하여 학습 안정성 및 속도 향상
드롭아웃: 과적합 방지를 위해 일부 뉴런을 무작위로 꺼서 네트워크의 일반화 능력 강화
출력층: 시그모이드 함수로 이진 분류 수행

라이브러리

PyTorch
NumPy
pandas
scikit-learn
imblearn


