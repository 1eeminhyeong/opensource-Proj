# 메신저 대화로그 기반 MBTI 분석 시스템
## How to Install?
```
sudo apt-get install git
git clone https://github.com/Alsguddd/Opensource-Project.git
```
## Summary
#### 대화를 통해서 MBTI를 예측하고 이를 알고리즘 사용자에게 제공. 기존의 MBTI 검사는 많은 양의 질문에 응답해야 하므로 시간이 많이 소요되고, 모든 질의에 집중해서 답변하지 못할 가능성이 있음. 
#### 이를 개선하고자 보편적으로 소유하고 있는 개인정보 중 하나인 메신저 대화로그를 이용하여 MBTI를 예측하는 시스템을 제안함.
## How to Run?
### ◀대화 내역 전처리▶
##### 대화창->설정->대화 내용->대화 내보내기
<img src = "https://user-images.githubusercontent.com/106859397/204077923-81834624-1381-4c89-bdfe-7ccf2bb4a600.jpg" width="30%" height="10%">
<br/>
clone한 ipynb에 코드 사용자의 카카오톡 대화 내역 파일로 경로 변경이 필요.
<br/>
*본 프로젝트에서는 Google Colab에 내장된 API 중 하나인 drive를 이용했음.
<img src = "https://user-images.githubusercontent.com/112086285/204618373-1ba54008-6cc7-48a6-8b70-c004d4692216.png" width="50%" height="30%">
<br/>
사용자의 이름과 상대방의 이름을 입력<br/>
이름에 대괄호를 추가한 형태로 입력해야 함. (예: 홍길동 -> [홍길동])
<img src = "https://user-images.githubusercontent.com/112086285/204621098-d25c1551-4abe-478f-9007-fb41bc73fb16.png" width="30%" height="10%">
<br/><br/>

### ◀Classification Algorithm 학습▶
##### Data 폴더 안에 있는 Data set으로 알고리즘을 학습, mbti_svm_v2.sav 파일을 추출
##### Data set은 Kaggle에서 가져온 파일을 축소시킨 파일임.
##### (https://www.kaggle.com/datasets/zeyadkhalid/mbti-personality-types-500-dataset)
<br/><br/>

### ◀전처리한 대화를 Algorithm에 대입, 결과확인▶
##### 전처리가 완료된 대화 내역은 result.txt로 저장됨.
##### result.txt를 Algorithm에 대입해 결과를 확인
<img src = "https://user-images.githubusercontent.com/112086285/204620406-238e73f2-58ff-4cee-b8cc-6bc49e9177b3.png" width="50%" height="30%">
