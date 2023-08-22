<퀘스트>
- 입원기간(목표변수)에 영향을 주는 설명변수들 찾기 
- 최소 설명변수 갯수 10개 
- 전통적인 통계 검증 방식을 통한 인사이트 도출 
- BMI 공통 사용 
- github: toy_data_analysis 
- readme - 합쳐서 얘기하는 부분 (어디할지 정하는부분/마지막 인사이트 도출) 
- 파일두개로 분리 EDA -> CDA는 따로 
- DDA에서 null삭제 및 이상치 제거한 상태로 EDA-> CDA 

10개 보다 많은 설명변수 정해서 둘이서 나누기  
EDA -> CDA 각적인 것 하고 나서 빼자 말자 정하기 
다변수 검증 거치기 
p-alue에 의해 영향 준다/준다 체크 
7개 정도 나와서 인사이트 정리 


apply 사용해서 변형하기 
(체중/신장과의 상충관계--BMI처럼 
두컬럼 연관되는거 검증) 
제3의 변수/컬럼 만들기 
변수 새로 만들거나 변수를 연속해서 범주형으로 만들기 


목표변수: 입원기간 
설명변수: (왜 이 변수들을 뽑았는지 이유를 리드미에 설명--분석스토리) 

수술의 종류와 복잡도
환자의 건강 상태



---상태 / 기저질환 -- 7-8개
Large Lymphocyte
가족력 
기저질환 - 당뇨여부/ 고혈압여부/ 신부전여부 / 심혈관질환 
우울증여부

지방축적도: 지방축적도가 높을 경우 회복이 느려질 수 있어 입원 기간에 영향을 미칠 수 있습니다.

과거수술횟수: 과거 수술 횟수가 많을 경우 조직 상태나 회복 속도에 영향을 줄 수 있어 입원 기간에 영향을 미칠 수 있습니다.

신장과 체중: 신장과 체중은 환자의 일반적인 건강 상태와 회복 속도에 영향을 줄 수 있으며, 따라서 입원 기간에 영향을 미칠 수 있습니다. -> BMI 

연령: 연령이 높을수록 회복 속도가 느려질 수 있어 입원 기간에 영향을 줄 수 있습니다.

성별: 성별은 생리적, 생물학적인 차이로 인해 회복 속도나 합병증 발생 가능성에 영향을 줄 수 있습니다.

헤모글로빈수치: 헤모글로빈 수치가 낮을 경우 빈혈로 인한 회복 지연 가능성이 있어 입원 기간에 영향을 줄 수 있습니다.



-- 수술 관련 -- 7-8개
Location of herniation (탈출부위): 디스크 탈출이 어느 부위에 발생했는지가 수술의 복잡성 및 회복 기간에 영향을 줄 수 있습니다.
ODI (Oswestry Disability Index): ODI 점수가 높을수록 통증 및 기능 장애 정도가 높아져 회복이 느려질 수 있어 입원 기간에 영향을 줄 수 있습니다.

수술 기법 
통증정도

통증기간: 높은 통증 정도나 긴 통증 기간이 입원 기간을 연장시킬 수 있습니다.

수술시간: 수술의 복잡성과 수술 시간은 입원 기간에 영향을 줄 수 있습니다.

수술실패여부: 수술 실패가 있을 경우 추가 조치나 재수술이 필요할 수 있어 입원 기간에 영향을 미칠 수 있습니다.

재발여부: 수술 후 재발이 있는 경우 추가 치료가 필요하며, 이는 입원 기간을 연장시킬 수 있습니다.

Instability: 척추의 불안정성이 있는 경우 추가 관리가 필요하여 입원 기간에 영향을 줄 수 있습니다.

디스크단면적