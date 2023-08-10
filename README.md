# 구글 스튜디오 연습


안녕하세요 여러분! 오늘은 구글 스튜디오를 이용하여 데이터 시각화를 연습해보는 시간을 갖도록 할게요. 시작하기 앞서, 준비된 데이터 파일 이름은 Data.csv이며, 이 파일은 아래와 같은 열을 포함하고 있습니다



<!-- 목차 -->
<ol>
    <li><a href="#intro">구글 스튜디오</a></li>
    <li><a href="#table">테이블</a></li>
    <li><a href="#data-aggregation">데이터 집계</a></li>
    <li><a href="#pivot-and-card">피벗 테이블 및 카드 시각화</a></li>
    <li><a href="#slider-and-filter">슬라이더 및 시각화 필터</a></li>
    <li><a href="#custom-calculation">맞춤 계산</a></li>
    <li><a href="#case-study">사례 연구</a></li>
    <li><a href="#time-series-graph">시계열 그래프</a></li>
    <li><a href="#other-visual">기타 시각화</a></li>
    <li><a href="#dashboard">대화형 대시보드 게시 및 공유</a></li>
    <li><a href="#case-study2">사례 연구2</a></li>
    <li><a href="#conclusion">결론</a></li>
</ol>

<!-- 각 섹션 -->
<div id="intro">

## 1. 구글 스튜디오

### 1) 구글 스프레드시트 데이터 로드
우선, 구글 스프레드시트에 Data.csv 파일을 업로드 한다. 파일 > 파일 가져오기를 통해 데이터를 로드할 수 있다

### 2) 구글 데이터 스튜디오 연결
* 구글 데이터 스튜디오에 접속하여 '새 보고서'를 클릭하면 됩니다
* 데이터 추가 > 구글 스프레드시트를 선택하시고, 방금 업로드한 Data.csv 파일을 선택하여 연결
* 이렇게 하면 구글 데이터 스튜디오와 스프레드시트의 연결이 완료

Data.csv는 열은 다음과 같다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e510eaa7-4984-4518-9c76-ce0a862f0dcc)

</div>

<div id="table">

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

</div>

<div id="data-aggregation">

### 3. 데이터 집계

집계는 데이터를 분석할 때 사용하는 기본적인 방법입니다. 여러분이 가지고 있는 데이터를 적절하게 분석하고 시각화하기 위해서는 다양한 집계 방법을 사용할 수 있습니다. 본 포스팅에서는 Google Studio의 기본적인 집계 방법에 대해 소개하겠습니다.

1번째 테이블

이 테이블에서는 제조사별 총 매출을 살펴볼 수 있습니다.

* 측정기준 : Manufactors
* 측정항목 : Salses

* SUM : Total Sales
* AVG : Avg Sales
* MIN : Lowest Sales
* MAX : Highest Sales

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/336dc3f9-b910-4781-9969-f1b0c64496bd)

이 이미지는 제조사별 매출을 다양한 측정항목으로 집계한 결과를 나타냅니다.


2번테이블

제품의 하위 카테고리와 제품 이름에 대한 집계 방법을 설명하고 있습니다.

* 측정기준 : Product sub category
* 측정항목 : Product Name

* CT : No of Trans
* CTS : No of Products

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/865e1a7d-ba65-47f2-b526-b741f7520bb4)

이 이미지는 제품 하위 카테고리별 제품 이름의 거래 횟수와 제품 수를 집계한 결과를 나타냅니다.

2) 실무 집계 연습

위 배운 방식으로 실무에서 쓰일 수 있는 테이블을 시각화 해보겠습니다.

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

이 섹션에서는 데이터의 특정 값을 서로 비교하여 통계적 또는 분석적 정보를 얻습니다. 그래프에 표시된 값들은 서로의 비교를 통해 특정 패턴이나 추세를 파악하는 데 도움을 줍니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/48589610-e299-4a5d-a2ac-5a6f28ded3c1)



4) 누계 계산

누계는 데이터를 순서대로 더하는 방식으로, 특정 기간 동안의 누적된 값을 보여줍니다.

* 총계 백분율:

전체 중 특정 항목의 비율을 표시합니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/69f6fdd6-0258-434d-b805-289af72c03b4)

* 누계 백분율:

누적된 백분율 값을 표시합니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/826630e7-0052-4b50-a49e-e2463f0f1a66)

* 하위 범주 누적 백분율:
  
하위 카테고리에 따른 누적 백분율 값을 보여줍니다.

![Google_Studio_Table5](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/6901b13c-1770-42b9-9690-d1ae8bd2b702)

* 최솟값 비교

데이터 집합에서 최솟값을 표시합니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/edc9befc-fc2a-488e-a563-01bc5eab5655)

* 최댓값 비교:
 
데이터 집합에서 최댓값을 표시합니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d1f7183b-5a92-433f-a791-ec397326c533)

* 집계 비교:

전체 집계된 값들의 비교를 보여줍니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9408ce4a-dd56-457c-9c45-df1cfb808930)

* 평균 비교:

전체 집계된 값들의 비교를 보여줍니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/fdd0516c-80b5-48fb-91a4-ebd0fdc3bb8f)

* 델타 비교: 

데이터의 변화량이나 차이를 나타내기 위해 사용됩니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0256b15f-f418-4db8-9b92-6116ef50d97d)




5) 드릴 다운 ( 교차 )

드릴 다운은 데이터를 상세하게 조사하기 위한 분석 기법입니다. 사용자는 더 상세한 수준의 데이터를 살펴볼 수 있습니다.

* Region >> County >> City:

지역, 국가, 도시 순으로 데이터의 세부 정보를 확인할 수 있습니다.

![Google_Studio_Table6](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2d3b3fcb-0765-47ef-82d6-8376a927bdaf)

* Asia >> South Korea >> Seoul: 

아시아 지역 내에서 대한민국의 서울까지의 데이터를 상세하게 살펴봅니다.

![Google_Studio_Table7](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/1487db46-33a1-482a-85de-cd402eb9d371)



6) 날짜 작업 ( 교차 )

이 섹션에서는 연도별, 분기별, 월별 및 요일별로 데이터를 정렬하고 분석합니다. 이러한 분석을 통해 시간에 따른 추세나 패턴을 파악할 수 있습니다.

연도별, 분기별 정렬

월, 요일별 정렬

![Google_Studio_Table8](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/021a1d5c-7b70-4adc-a7d7-d3fb409a2a04)

</div>

<div id="pivot-and-card">

## 4. 피벗 테이블 및 카드 시각화

1) 피벗 테이블 및 스코어카드 소개

피벗 테이블은 구글 스튜디오에서 데이터를 요약하고 분석하는 데 유용한 도구로, 여러 데이터 포인트를 쉽게 비교하고 파악할 수 있게 해준다 스코어카드는 구글 스튜디오의 시각화 도구 중 하나로, 중요한 통계나 정보를 강조해서 한 눈에 볼 수 있게 표시하는 역할을 한다 이렇게 해서, 둘 다 구글 스튜디오에서 데이터를 효과적으로 전달하고 분석하는 데 큰 도움이 됩니다


2) 피벗 테이블 만들기

![Google_Studio_Table11](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c713d30c-c5be-43a9-b538-c9baccfde474)

이 이미지는 피벗 테이블의 기본 구조를 보여줍니다. 행과 열을 기준으로 데이터가 어떻게 분류되고 집계되는지 한눈에 확인할 수 있

3) 비교 계산

![Google_Studio_Table9](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/99cf3474-ae6b-4070-a7c0-2a2d874a8ea7)

비교 계산은 데이터 간의 차이나 증감을 시각적으로 표현하여 데이터의 변화나 트렌드를 파악하는 데 도움을 줄 수 있다.

4) 카드 시각화

![Google_Studio_Table10](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/dd8b7ad9-c018-432d-8edc-c91b3440c2bc)

카드 시각화는 특정 지표나 값을 강조하여 보여주는 도구입니다. 주요 통계나 중요한 데이터 포인트를 강조해서 표시할 때 유용하다.

5) 실무 실습

다음 카드 시각화 만들기

* 매출액 합계

* 평균 매출

* 최고 판매

* 최저가 판매

* 판매된 제품 수

* 제품이 판매된 국가 수

* 제품 범주 및 채널별 이익

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/021de912-e08f-4d3f-9b76-16e6e321d656)

이 이미지는 실무에서 사용할만한 데이터 시각화를 예시로 보여준다. 각 카드는 특정 지표에 중점을 둔 시각화로 구성되어 있습니다.

</div>

<div id="slider-and-filter">

## 5. 슬라이더 및 시각화 필터



</div>

<div id="case-study">

## 6. 사례 연구



</div>

<div id="time-series-graph">

## 8. 시계열 그래프



</div>

<div id="other-visual">

## 9. 기타 시각화



</div>

<div id="dashboard">

## 10. 대화형 대시보드 게시 및 공유



</div>

<div id="case-study2">

## 11. 사례 연구2



</div>

<div id="conclusion">

## 12. 결론



</div>












