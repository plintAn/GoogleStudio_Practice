# 구글 스튜디오 연습


안녕하세요 여러분! 오늘은 구글 스튜디오를 이용하여 데이터 시각화를 연습해보는 시간을 갖도록 할게요. 시작하기 앞서, 준비된 데이터 파일 이름은 Data.csv이며, 이 파일은 아래와 같은 열을 포함하고 있습니다

## 1. 구글 스튜디오

1)구글 스프레드시트 데이터 로드
우선, 구글 스프레드시트에 Data.csv 파일을 업로드 한다. 파일 > 파일 가져오기를 통해 데이터를 로드할 수 있다

## 2) 구글 데이터 스튜디오 연결
* 구글 데이터 스튜디오에 접속하여 '새 보고서'를 클릭하면 됩니다
* 데이터 추가 > 구글 스프레드시트를 선택하시고, 방금 업로드한 Data.csv 파일을 선택하여 연결
* 이렇게 하면 구글 데이터 스튜디오와 스프레드시트의 연결이 완료

Data.csv는 열은 다음과 같다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e510eaa7-4984-4518-9c76-ce0a862f0dcc)




## 2. 테이블

1) 테이블 만들기
* 보고서 페이지 내에서 '테이블' 위젯을 선택하여 드래그&드롭으로 페이지에 추가
* 오른쪽 '데이터' 탭을 통해 원하는 열을 테이블에 추가

![Google_Studio_Table1](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8d08d7d5-73bd-4266-95b0-2541e9f7e649)

  
2) 표 서식 지정 및 정렬
* 테이블의 각 열의 제목을 클릭하면 정렬 옵션을 볼 수 있다 원하는 방식대로 오름차순 또는 내림차순으로 정렬할 수 있다.

![Google_Studio_Table2](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2fe9c3f9-dcf1-4b21-8fd3-cde9186b3070)


3) 다중 서식 조치(교차 포함)
* 테이블에서 다중 서식을 적용하려면, 원하는 셀이나 열을 선택 후 서식 메뉴에서 '다중 서식' 옵션을 선택합니다. 교차되는 부분에 대한 서식도 동시에 조절할 수 있습니다.

  ![Google_Studio_Table3](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/ecd02f73-1627-4f99-9d10-6eb839c57d9d)

4) 조건부 서식
* 조건부 서식을 통해 특정 조건에 맞는 데이터에 대해 다른 스타일을 적용할 수 있습니다. 예를 들면, 수익이 특정 금액 이상일 때 셀의 배경색을 변경하는 것과 같은 작업입니다.

![Google_Studio_Table4](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e0e3fbeb-91b8-4934-8975-53546210931c)

   
5) 실무 활동 연습

1.매출이 가장 높은 제조업체는 어디입니까?
- 답변 - Fabrikam – 12,054,281

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9838ad10-3619-4ac6-b9e5-2cc33d99ca9f)

  
2.이익 값이 가장 낮은 제품 범주는 무엇입니까?
- 답변 - 오디오 – 577,270

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/7ee06038-7d78-4784-abfc-72c2cdf9d9cb)

  
3.어느 제조업체가 가장 높은 이익을 얻었습니까?
- 답변 - Fabrikam – 7,158,977

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c0dff7be-6080-4e88-9a57-96b3eee02f0b)

  
4.판매 비용이 가장 높은 채널은 무엇입니까?
- 답변 - 매장 – 13,671,368

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e7b6b34b-5b74-430a-aeec-17630cda42dc)

  
5.매출이 가장 높은 프로모션 이름은 무엇입니까?
- 답변 - 할인 없음 – 18,329,360

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/b5fd68fb-7e95-4424-a577-05deb23b9d10)

  
6.이익이 가장 높은 제품 하위 범주는 무엇입니까?
- 답변 - 캠코더 – 4,972,853


![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8800c56f-6b67-4d7a-a743-844d1ab84830)



### 3. 집계 방법

1번째 테이블

* 측정기준 : Manufactors
* 측정항목 : Salses

* SUM : Total Sales
* AVG : Avg Sales
* MIN : Lowest Sales
* MAX : Highest Sales

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/336dc3f9-b910-4781-9969-f1b0c64496bd)



2번테이블

* 측정기준 : Product sub category
* 측정항목 : Product Name

* CT : No of Trans
* CTS : No of Products

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/865e1a7d-ba65-47f2-b526-b741f7520bb4)


2) 실무 집계 연습




1. 제품 이름별 총 매출을 보여주는 새 테이블 만들기

- 가장 높은 판매에서 가장 낮은 판매로 표를 정렬합니다. 가장 많이 팔린 제품은?

- 답변 - Contoso 프로젝터 1080 P X980 검정 – 445,115

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/a1541996-7a73-4658-86a0-99ddf81500b6)

2. 가장 낮은 매출에서 가장 높은 매출 순으로 표를 정렬합니다. 판매량이 가장 적은 제품은 무엇입니까?

- Answer - SV USB 데이터 케이블 E 600 그레이 - 46

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c84b6d11-b183-4d57-96dc-a28143269899)


3. 가장 많은 도시에서 판매되는 제품은 무엇입니까?

- 답변 - Litware 홈 시어터 시스템 5.1 채널 M515 브라운 – 22

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/a95f6961-6359-4f77-b5b2-67ee8c259475)


4. 국가별 총 매출을 보여주는 새 테이블 만들기

- 요약 방법을 다음과 같이 변경합니다.

- 평균 – 평균 매출이 가장 높은 국가는 어디입니까?

- 답변 - 중국 – 4518

- Min – 최소 매출이 가장 낮은 국가는 어디입니까?

- 답변 - 중국, 싱가포르, 미국 - 5

- Max – 최대 매출이 가장 높은 국가는 어디입니까?

- 답변 - 미국 - 78312

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/91d02bb3-3df1-4d22-9919-42a41ac28cbd)


5. 도시별 이익을 표시하는 새 테이블을 만듭니다.

- 거래 건수가 가장 많은 도시는 어디입니까?

- 답변 - 베이징 - 1398

- 평균 이익이 가장 낮은 도시는 어디입니까?

- 답변 - 베네치아 - 438

- 가장 다양한 유형의 제품을 판매하는 도시

- 답변 - 베이징 - 924
  
![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/fc0a0e27-7f60-48e2-97a8-b1f535f17555)




3) 비교 계산



![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/48589610-e299-4a5d-a2ac-5a6f28ded3c1)



4) 누계 계산

총계 백분율

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/69f6fdd6-0258-434d-b805-289af72c03b4)

누계 백분율

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/826630e7-0052-4b50-a49e-e2463f0f1a66)

하위 범주 누적 백분율

![Google_Studio_Table5](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/6901b13c-1770-42b9-9690-d1ae8bd2b702)

최솟값 비교

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/edc9befc-fc2a-488e-a563-01bc5eab5655)

최댓값 비교

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d1f7183b-5a92-433f-a791-ec397326c533)

집계 비교

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9408ce4a-dd56-457c-9c45-df1cfb808930)

평균 비교

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/fdd0516c-80b5-48fb-91a4-ebd0fdc3bb8f)

델타 비교

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0256b15f-f418-4db8-9b92-6116ef50d97d)




5) 드릴 다운 ( 교차 )

Region >> County >> City

![Google_Studio_Table6](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2d3b3fcb-0765-47ef-82d6-8376a927bdaf)

Asia >> South Korea >> Seoul

![Google_Studio_Table7](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/1487db46-33a1-482a-85de-cd402eb9d371)



6) 날짜 작업 ( 교차 )

연도별, 분기별 정렬

월, 요일별 정렬

![Google_Studio_Table8](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/021a1d5c-7b70-4adc-a7d7-d3fb409a2a04)








