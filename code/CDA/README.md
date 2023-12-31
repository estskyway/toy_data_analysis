### 분석 스토리
+ 분석 목적:
    - 입원기간에 따른 여러 요인들을 파악하고 분석하기위해 
+ 변수 선택 이유(표) :

|변수명 |변수타입 |설명 |이유|
| --- | --- | --- | --- |
| 입원기간(목표변수) | 연속형 | 입원한 기간을 나타내는 지표 | 강사님이 정해주셨음 |
| 연령 | 연속형 | 나이를 나타내는 지표 | 젋은 사람이 회복속도가 비해 빠르다는 지식에 의해 의문을 가짐 |
| Large Lymphocyte | 연속형 | 혈액 내 큰 림프구 수치를 나타내는 지표 | 면역력이 좋으면 회복력이 빠르다는 지식에 의해 의문을 가짐 |
| 당뇨여부 | 범주형 | 당뇨병 유무를 나타내는 지표 | 당뇨가 회복력에 영향을 준다는 지식에 의해 의문을 가짐 |
| 과거수술횟수 | 범주형 | 과거 수술을 받은 횟수를 나타내는 지표 | 수술횟수가 많을 수록 그 부위가 약해질거라는 가설에 의문을 가짐 |
| 비만도 | 범주형 | BMI지수를 토대로 비만도를 측정한 지표 | 비만이 여러 병들에 영향을 준다는 지식에 의해 의문을 가짐 |


+ 일부 시각화(EDA)
+ 분석 스토리(CDA 중심, 표) : 
- 연령에 따른 입원기간에 변화가 있는지 pearsonr 방식으로 검증을 해보았다. 
결과적으로 pvalue가 0.0772836이 나왔으므로 귀무가설에 의해 변화가 없는 것으로 나왔다.
따라서 입원기간은 연령과 무관한것으로 보인다.

- 림프구에 따른 입원기간에 변화를 pearsonr 방식으로 검증을 해보았다. 
결과적으로 pvalue가 0.134780이 나왔으므로 귀무가설에 의해 변화가 없는 것으로 나왔다.
따라서 면역체계를 담당하는 림프구와 입원기간은 무관한 것으로 보인다.

- 당뇨여부에 따른 입원기간의 변화를 ranksums 방식으로 검증을 해보았다.
결과적으로 pvalue가 4.738..... - 68이 나왔으므로 대립가설에 의해 변화가 있는 것으로 나왔다.
따라서 당뇨여부는 입원기간에 영향을 주는 것으로 보인다.

- 과거수술횟수에 따른 입원기간의 변화를 kruskal 방식으로 검증을 해보았다.
결과적으로 pvalue가 0으로 나왔기 때문에 대립가설이 참인것으로 나왔다.
따라서 과거수술횟수는 입원기간에 영향을 주는 것으로 보인다.

- 비만도에 따른 입원기간의 변화를 kruskal 방식으로 검증을 해보았다.
결과적으로 pvalue가 0이므로 대립가설에 의해 변화가 있는 것으로 나왔다.
따라서 비만도는 입원기간에 영향을 주는 것으로 보인다.



    - '통증기간(월)'(연속형): 상관 계수가 |-0.001668| < 0.5 작아서 관계성이 거의 없는 듯함 
    - '수술시간'(연속형): 상관 계수가 |-0.021077| < 0.5 작아서 관계성이 거의 없는 듯함 
    - '디스크단면적'(연속형): 상관 계수가 |0.010129| < 0.5 작아서 관계성이 거의 없는 듯함 
    
    - 'Instability'(범주형): 척추 불안정성이 있는 경우의 입원기간이 길지만 유의미한 차이로 보이지 않음
    - '수술기법'(범주형): IELD가 TELD보다 입원기간이 길지만 유의미한 차이로 보이지 않음
    - '수술실패여부'(범주형): 수술실패여부가 있는 경우의 입원기간이 길지만 유의미한 차이로 보이지 않음
    
    - '환자통증정도'(순서형): 환자통증정도가 5인 경우 입원기간이 가장 긴 것으로 보임 


    수술기법 및 환자통증정도에 따라 입원기간 분포에 차이가 있는 것으로 보인다. 
수술기법 및 환자통증정도는 입원기간(목표변수)에 대한 설명변수로써 적합하며 이를 통한 인사이트 도출이 가능해 보인다. 
IELD가 TELD보다 입원기간이 길며, 이를 통해 IELD 수술기법을 적용했을 때 회복기간이 오래 걸림을 유추해볼 수 있다. 
환자통증정도는 8일때 입원기간이 가장 길며, 그에 비해 9,10일때의 입원기간은 상대적으로 짧은 것을 볼 수 있다. 
약 46퍼센트의 환자들이 통증정도로 7을 택했다는 점, 상대적으로 다른 수치의 통증정도를 택한 환자의 데이터수가 현저히 낮다는 점을 고려해봤을때, 해당 데이터를 통해 환자통증정도와 입원기간의 연관성을 알아보기에는 한계성이 보인다. 

그 외, 통증기간, Instability, 수술시간, 수술실패여부, 디스크단면적과 입원기간과는 관계성이 없으며, 따라서 입원기간(목표변수)의 설명변수로써 적합하지 못하다. 
