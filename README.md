# PythonDT2
삼성멀티캠퍼스 데이터 분석 전공자반 심화과정

<p>
  
  3일차 : Feature Scale을 왜 해야할까? <br>
  
  1. Y = W1・X1 + W2・X2 인 상황에서 w1은 1~10 사이의  M 값, w2는 100~1000 사이의 값이 있을 때 w1과 w2의 관계가 동일하다면 스케일링을 해주어야 함.
  2. 만약 w1과 w2의 관계가 다르다면 (w2의 중요도가 더 높다면) 스케일링을 진행하지않고 원래 데이터를 살리자.
  
  - 그렇다면 왜? 우리는 스케일링을 무조건 해주라고 배우는가? 특성이 100개 정도가 있다고 할 때 우리는 이 100개의 특성을 다 파악해서 데이터에 맞게 스케일링을 진행하는 것은 불가능하다. <br>
  따라서 통째로 스케일링을 하여 맞춰주거나 아에 하지 않는 경우로 배운다.
  - 단. SGD 를 사용할 경우에는 스케일링을 진행 해주자. 왜? w2/x2 과 w1/x1을 가지고 경사하강법을 진행할 경우 w2/x2의 스케일과  w1/x1의 스케일이 다를경우 수렴하지 못하는 경우가 생길 수도 있음.
  - OLS , DecisionTree, RandomForest, GradientBoosting 은 스케일링 필요 없음.  

</p>

<p>
  
  3일차 : 측정 지표인 R2, Mean Absolute Error, Mean Squared Error, Mean Squared Log Error에 대해서 <br>
  
  1. R2_score는 가장 기본적인 지표
  2. MAE는 오차의 값을 있는 그대로 반영 , 오차의 크기를 확인하는 목적
  3. MSE는 오차의 값이 작은건 작게 큰건 더 크게 반영. 보통 MAE랑 MSE를 같이 씀. 로그 오차를 확인하는 목적.
  4. MAPE는 MAE의 퍼센트 , 즉 오차의 비율을 보고싶을 때 확인하는 목적이다.

</p>

---

<p>
  4일차 : 분류
  
  - 분류분석 : Confusion Matrix를 사용하여 기본적인 지표 확인.
    - Accuracy : Acc는 타겟값의 클래스 차이가 많이 날 경우 신뢰하기 힘든 지표!! 
      - 위스콘신 유방암 진단 -> 타겟값의 차이가 많이나기 때문에 Acc를 잘 쓰진않음.
    
    - 민감도 (Sensitivity) , 재현율 (Recall), TP / (TP+EN)
      - 전체 positive 중 맞힌 postive의 비율
      - 얼마나 잘 맞췄는지 확인해보기 위해서.
  
    - 특이도 ( Specificity) TN / (TN+FP) 
      - 전체 Negative 중 맞힌 Negative의 비율
  
    - 정밀도 Precision TP / (TP + FP)
      - 예측 positive 중 맞힌 positive 의 비율
      - 얼마나 덜 틀리고 맞췄냐.!!
      - predicion_score
      
</p>
  
  
  
  
  
