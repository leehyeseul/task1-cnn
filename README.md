# task1-cnn
[제5차] USG AI·데이터 제조혁신 경진대회 초급

https://aifactory.space/task/6685/data

I. 데이터 설명
불량 판별을 위한 아크용접 이미지에서 "Good"과 "Bad"를 판별하는 이진 분류 과제입니다.

 

1. 데이터 특성
이미지 개수 : Train 3500개 , Test : 1500개
이미지 크기 : 600x600
이미지 클래스 : 2개
 

Good	

<img width="499" height="469" alt="image" src="https://github.com/user-attachments/assets/674aa380-a50e-4f12-8c25-ca5c2e7c00c3" />



bad

 <img width="454" height="454" alt="image" src="https://github.com/user-attachments/assets/8ba133dc-a29d-409b-a912-3c643a24079e" />


 

 

2. 파일 구성
🗂️task1.zip
 ├── 📈answer_sample.csv  - 정답 샘플
 ├── 📈 train_labels.csv -  Train label
 ├──🗂️ train                        -  Train 폴더  
 │      └──🗒️ train0000.jpeg   -  Train 이미지
 │      └──🗒️ train00...jpeg
 ├──🗂️ test                            -  Test 폴더 
         └──🗒️ test0000.jpeg    -  Train 이미지
         └──🗒️ test00...jpeg

 

 

 

3. 평가 지표
본 과제의 평가에는 weighted 방식의 F1-Score가 사용됩니다.

<img width="623" height="182" alt="image" src="https://github.com/user-attachments/assets/5bac57ca-a4ea-4489-bb96-7a8f8f10f5fd" />

 
blog image
실제 평가 스크립트는 scikit-learn의 f1_score 함수를 활용합니다. 파라미터가 적용된 해당 함수의 명령은 다음과 같습니다.
from sklearn.metrics import f1_score
score = f1_score(y_true, y_pred, average='weighted')
점수는 Public:Private 1:1로 분할 평가되며, 대회기간중에는 Public Score만 제공됩니다.
Private Score를 포함한 Total Score는 대회 종료 시점에 공개되며, 최종 순위는 Total Score를 바탕으로 산출됩니다.
 
