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

### 1) 테이블 만들기
* 보고서 페이지 내에서 '테이블' 위젯을 선택하여 드래그&드롭으로 페이지에 추가
* 오른쪽 '데이터' 탭을 통해 원하는 열을 테이블에 추가

![Google_Studio_Table1](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8d08d7d5-73bd-4266-95b0-2541e9f7e649)
  
### 2) 표 서식 지정 및 정렬
* 테이블의 각 열의 제목을 클릭하면 정렬 옵션을 볼 수 있다 원하는 방식대로 오름차순 또는 내림차순으로 정렬할 수 있다.

![Google_Studio_Table2](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2fe9c3f9-dcf1-4b21-8fd3-cde9186b3070)


### 3) 다중 서식 조치(교차 포함)
* 테이블에서 다중 서식을 적용하려면, 원하는 셀이나 열을 선택 후 서식 메뉴에서 '다중 서식' 옵션을 선택합니다. 교차되는 부분에 대한 서식도 동시에 조절할 수 있습니다.

  ![Google_Studio_Table3](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/ecd02f73-1627-4f99-9d10-6eb839c57d9d)

### 4) 조건부 서식
* 조건부 서식을 통해 특정 조건에 맞는 데이터에 대해 다른 스타일을 적용할 수 있습니다. 예를 들면, 수익이 특정 금액 이상일 때 셀의 배경색을 변경하는 것과 같은 작업입니다.

![Google_Studio_Table4](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e0e3fbeb-91b8-4934-8975-53546210931c)

   
### 5) 실무 활동 연습

#### 1.매출이 가장 높은 제조업체는 어디입니까?
- 답변 - Fabrikam – 12,054,281

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9838ad10-3619-4ac6-b9e5-2cc33d99ca9f)

  
#### 2.이익 값이 가장 낮은 제품 범주는 무엇입니까?
- 답변 - 오디오 – 577,270

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/7ee06038-7d78-4784-abfc-72c2cdf9d9cb)

  
#### 3.어느 제조업체가 가장 높은 이익을 얻었습니까?
- 답변 - Fabrikam – 7,158,977

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c0dff7be-6080-4e88-9a57-96b3eee02f0b)

  
#### 4.판매 비용이 가장 높은 채널은 무엇입니까?
- 답변 - 매장 – 13,671,368

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e7b6b34b-5b74-430a-aeec-17630cda42dc)

  
#### 5.매출이 가장 높은 프로모션 이름은 무엇입니까?
- 답변 - 할인 없음 – 18,329,360

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/b5fd68fb-7e95-4424-a577-05deb23b9d10)

  
#### 6.이익이 가장 높은 제품 하위 범주는 무엇입니까?
- 답변 - 캠코더 – 4,972,853


![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8800c56f-6b67-4d7a-a743-844d1ab84830)

</div>

<div id="data-aggregation">

## 3. 데이터 집계

집계는 데이터를 분석할 때 사용하는 기본적인 방법입니다. 여러분이 가지고 있는 데이터를 적절하게 분석하고 시각화하기 위해서는 다양한 집계 방법을 사용할 수 있습니다. 본 포스팅에서는 Google Studio의 기본적인 집계 방법에 대해 소개하겠습니다.

### 1번째 테이블

이 테이블에서는 제조사별 총 매출을 살펴볼 수 있습니다.

* 측정기준 : Manufactors
* 측정항목 : Salses

* SUM : Total Sales
* AVG : Avg Sales
* MIN : Lowest Sales
* MAX : Highest Sales

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/336dc3f9-b910-4781-9969-f1b0c64496bd)

이 이미지는 제조사별 매출을 다양한 측정항목으로 집계한 결과를 나타냅니다.


### 2번테이블

제품의 하위 카테고리와 제품 이름에 대한 집계 방법을 설명하고 있습니다.

* 측정기준 : Product sub category
* 측정항목 : Product Name

* CT : No of Trans
* CTS : No of Products

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/865e1a7d-ba65-47f2-b526-b741f7520bb4)

이 이미지는 제품 하위 카테고리별 제품 이름의 거래 횟수와 제품 수를 집계한 결과를 나타냅니다.

### 2) 실무 집계 연습

위 배운 방식으로 실무에서 쓰일 수 있는 테이블을 시각화 해보겠습니다.

#### 1. 제품 이름별 총 매출을 보여주는 새 테이블 만들기

- 가장 높은 판매에서 가장 낮은 판매로 표를 정렬합니다. 가장 많이 팔린 제품은?

- 답변 - Contoso 프로젝터 1080 P X980 검정 – 445,115

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/a1541996-7a73-4658-86a0-99ddf81500b6)

#### 2. 가장 낮은 매출에서 가장 높은 매출 순으로 표를 정렬합니다. 판매량이 가장 적은 제품은 무엇입니까?

- Answer - SV USB 데이터 케이블 E 600 그레이 - 46

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c84b6d11-b183-4d57-96dc-a28143269899)


#### 3. 가장 많은 도시에서 판매되는 제품은 무엇입니까?

- 답변 - Litware 홈 시어터 시스템 5.1 채널 M515 브라운 – 22

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/a95f6961-6359-4f77-b5b2-67ee8c259475)


#### 4. 국가별 총 매출을 보여주는 새 테이블 만들기

- 요약 방법을 다음과 같이 변경합니다.

- 평균 – 평균 매출이 가장 높은 국가는 어디입니까?

- 답변 - 중국 – 4518

- Min – 최소 매출이 가장 낮은 국가는 어디입니까?

- 답변 - 중국, 싱가포르, 미국 - 5

- Max – 최대 매출이 가장 높은 국가는 어디입니까?

- 답변 - 미국 - 78312

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/91d02bb3-3df1-4d22-9919-42a41ac28cbd)


#### 5. 도시별 이익을 표시하는 새 테이블을 만듭니다.

- 거래 건수가 가장 많은 도시는 어디입니까?

- 답변 - 베이징 - 1398

- 평균 이익이 가장 낮은 도시는 어디입니까?

- 답변 - 베네치아 - 438

- 가장 다양한 유형의 제품을 판매하는 도시

- 답변 - 베이징 - 924
  
![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/fc0a0e27-7f60-48e2-97a8-b1f535f17555)




### 3) 비교 계산

이 섹션에서는 데이터의 특정 값을 서로 비교하여 통계적 또는 분석적 정보를 얻습니다. 그래프에 표시된 값들은 서로의 비교를 통해 특정 패턴이나 추세를 파악하는 데 도움을 줍니다.

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/48589610-e299-4a5d-a2ac-5a6f28ded3c1)



### 4) 누계 계산

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




### 5) 드릴 다운 ( 교차 )

드릴 다운은 데이터를 상세하게 조사하기 위한 분석 기법입니다. 사용자는 더 상세한 수준의 데이터를 살펴볼 수 있습니다.

* Region >> County >> City:

지역, 국가, 도시 순으로 데이터의 세부 정보를 확인할 수 있습니다.

![Google_Studio_Table6](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2d3b3fcb-0765-47ef-82d6-8376a927bdaf)

* Asia >> South Korea >> Seoul: 

아시아 지역 내에서 대한민국의 서울까지의 데이터를 상세하게 살펴봅니다.

![Google_Studio_Table7](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/1487db46-33a1-482a-85de-cd402eb9d371)



### 6) 날짜 작업 ( 교차 )

이 섹션에서는 연도별, 분기별, 월별 및 요일별로 데이터를 정렬하고 분석합니다. 이러한 분석을 통해 시간에 따른 추세나 패턴을 파악할 수 있습니다.

연도별, 분기별 정렬

월, 요일별 정렬

![Google_Studio_Table8](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/021a1d5c-7b70-4adc-a7d7-d3fb409a2a04)

</div>

<div id="pivot-and-card">

## 4. 피벗 테이블 및 카드 시각화

### 1) 피벗 테이블 및 스코어카드 소개

피벗 테이블은 구글 스튜디오에서 데이터를 요약하고 분석하는 데 유용한 도구로, 여러 데이터 포인트를 쉽게 비교하고 파악할 수 있게 해준다 스코어카드는 구글 스튜디오의 시각화 도구 중 하나로, 중요한 통계나 정보를 강조해서 한 눈에 볼 수 있게 표시하는 역할을 한다 이렇게 해서, 둘 다 구글 스튜디오에서 데이터를 효과적으로 전달하고 분석하는 데 큰 도움이 됩니다


### 2) 피벗 테이블 만들기

![Google_Studio_Table11](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c713d30c-c5be-43a9-b538-c9baccfde474)

이 이미지는 피벗 테이블의 기본 구조를 보여줍니다. 행과 열을 기준으로 데이터가 어떻게 분류되고 집계되는지 한눈에 확인할 수 있

### 3) 비교 계산

![Google_Studio_Table9](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/99cf3474-ae6b-4070-a7c0-2a2d874a8ea7)

비교 계산은 데이터 간의 차이나 증감을 시각적으로 표현하여 데이터의 변화나 트렌드를 파악하는 데 도움을 줄 수 있다.

### 4) 카드 시각화

![Google_Studio_Table10](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/dd8b7ad9-c018-432d-8edc-c91b3440c2bc)

카드 시각화는 특정 지표나 값을 강조하여 보여주는 도구입니다. 주요 통계나 중요한 데이터 포인트를 강조해서 표시할 때 유용하다.

### 5) 실무 실습

다음 카드 시각화 만들기

* 매출액 합계

* 평균 매출

* 최고 판매

* 최저가 판매

* 판매된 제품 수

* 제품이 판매된 국가 수

* 제품 범주 및 채널별 이익

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/eb25580f-7e92-4cf3-858c-7dae4c3d0037)

이 이미지는 실무에서 사용할만한 데이터 시각화를 예시로 보여준다. 각 카드는 특정 지표에 중점을 둔 시각화로 구성되어 있습니다.

</div>

<div id="slider-and-filter">

## 5. 슬라이더 및 시각화 필터

### 1.슬라이더 및 시각화 필터 소개

슬라이더와 시각화 필터는 Google Studio의 대시보드에서 데이터를 동적으로 탐색하고, 특정 조건 또는 값 범위에 따라 시각화를 업데이트하는 데 사용되는 컨트롤입니다. 이를 사용하면 사용자는 대시보드 내에서 원하는 데이터를 쉽게 선택하거나 필터링할 수 있습니다.

![Google_Studio_Table12](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/753a4b27-15cf-4c7f-bedb-7d6d4c19d1db)

위 이미지는 슬라이더와 시각화 필터의 기본 인터페이스를 보여주는데, 이 도구들은 Google Studio의 대시보드에서 데이터를 동적으로 탐색하고 조작하는 데 사용된다

### 2.텍스트 슬라이더

텍스트 슬라이더는 고정 크기 목록, 드롭 다운, 고급 필터와 같은 텍스트 기반의 값에 따라 데이터를 필터링하는 데 사용됩니다.

컨트롤 추가 >> 고정 크기 목록, 드롭 다운, 고급 필터 추가

![Google_Studio_Table13](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/db69f52c-4e5d-4bc1-96fd-eae50685360f)

이 이미지는 텍스트 기반의 값에 따라 데이터를 필터링하는 텍스트 슬라이더의 예를 보여준다.


### 3.숫자 슬라이더

숫자 슬라이더는 특정 숫자 범위 내의 데이터를 선택하거나 필터링하는 데 사용된다

컨트롤 추가 >> 슬라이더 추가

![Google_Studio_Table14](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d1ac907d-98cf-4a3f-aad5-38ed09147870)

숫자 슬라이더 예시 이미지입니다. 사용자는 이 슬라이더를 조작하여 원하는 숫자 범위의 데이터를 쉽게 선택할 수 있다.


### 4.날짜 슬라이더

날짜 슬라이더는 특정 날짜 범위에 따라 데이터를 필터링하는 데 사용된다. 특히 특정 연도나 분기의 데이터만을 보고 싶을 때 사용할 수 있다.

![Google_Studio_Table15](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/cfb462f3-8732-4c44-abbf-3b724a8fe219)

특정 날짜 범위를 선택하여 데이터를 필터링할 수 있는 날짜 슬라이더의 예시


### 5.텍스트 시각화 필터

특정 문자 또는 단어로 시작하는 텍스트를 기반으로 데이터를 필터링한다. 예를 들어, 지역 이름이 'I' 또는 'O'로 시작하는 데이터만을 선택할 수 있습니다.

I 또는 O로 시작하는 지역 이름 필터

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9d455d8b-57af-4e12-8aad-1481c67b3db0)

결과

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/ebbe0051-5845-4d88-abc6-03f2b4533eb5)


### 6.숫자 시각화 필터

특정 숫자 조건을 기반으로 데이터를 필터링한다. 예를 들어, 특정 판매량 이상의 데이터만을 선택할 수 있다.

속성 >> 측정항목 >> 측정항목 v 

![Google_Studio_Table16](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/1737bf26-7be4-42c9-bd6e-dd44fe9af53c)

숫자 값을 기준으로 데이터를 필터링하는 숫자 시각화 필터의 인터페이스


### 7.날짜 시각화 필터

특정 날짜 조건을 기반으로 데이터를 필터링한다 여기에서는 2018년까지의 데이터 중에서 분기별 매출액을 나누어 보는 예제를 확인할 수 있다.

이러한 슬라이더와 필터 도구들은 사용자가 원하는 데이터를 더욱 쉽게 찾고, 분석 결과를 더욱 효과적으로 전달하는 데 큰 도움을 준다

속성 >> 기본기간 >> 맞춤 >> 기간선택

해당 자료는 2018년까지 자료가 있으므로 분기별로 매출액을 나눠보겠습니다.

![Google_Studio_Table17](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9f2c41cb-b334-4a08-8438-e0e3ab838968)

사용자가 특정 날짜 범위를 선택하여 데이터를 필터링할 수 있도록 도와주는 날짜 시각화 필터의 인터페이스이다

이러한 이미지들은 Google Studio의 다양한 필터와 슬라이더 도구를 시각적으로 이해하는 데 도움을 준다.


</div>

<div id="custom-calculation">

## 6. 맞춤 계산

### 1. 사용자 지정 계산 소개



### 2. 계산 만들기

![Google_Studio_Table19](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/cd2f05e2-9f67-4cc2-8bad-9dc5d2c9911d)


OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/f1dec162-be4b-4b33-91ec-edfb576836ed)


### 3. 실제 활동

* 평균 매출 - Avg(Sales)

* 최고 판매 - Max(Sales)

* 제품 수 - Count_Distinct(Products Name)

* 제품당 평균 매출 - Sum(Sales)/Count_Distinct(Products Name)

### 4. 실습 완료

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8315311b-afdc-4f80-a929-36d58a370c0b)

### 5. 연월일

* 데이터 >> 속성 >> 필드 추가 
* 필드 이름:Year
* 수식:Year(Order Date)

이하 Month, Day of Month 모두 같은 방식

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/510d8059-ec91-4638-bf82-e3fa199d43f5)



## 6. 사례 진술

Case Else문 사용

```
Case When Sales>1000 Then "Over 1000"
Else
"Less 1000"
End
```
![Google_Studio_Table20](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9a055ecc-7a05-4c19-bcf9-d1918c0e41f2)

이후 3가지 분류로도 가능하다

```
Case When Sales>1000 Then "Over 1000"
When Sales>500 Then "Over 500"
Else
"Less 500"
End
```

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d7cddc1c-5d7f-459b-a830-eed4b8c0dd78)


### 7. 실제 활동

* 요일을 표시할 새 필드를 만듭니다.

* 평일(주문일)

* 제품 카테고리별 매출과 요일을 표시하는 테이블 생성

* 이익이 $500 이상, $200 이상, $200 미만인 주문 수를 표시하는 테이블을 만듭니다.

### 8. 실습 완료

OutPut 

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/08599253-bfd1-4fa1-bf4d-e4918cb36a02)

```
Case When profit>500 Then
"Over 500$"
When Profit>200 Then
"Over 200$"
Else
"Under 200$"
End
```
OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c7a9acf0-b283-4c8e-9f59-0f90077c56d9)



### 9. 비교

#### 스코어 카드 비교

* 차트 추가 >> 스코어 카드 생성

* 기본 기간 2019.1.1 ~ 2019.4.30
 비교 기간 이전 년도 1.1 ~ 4.30

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/cb716105-7e2f-48e9-acb8-47024537d904)

#### 차트 비교

* 차트 추가 >> 테이블 생성

* 기본 기간 2019.1.1 ~ 2019.4.30
* 비교 기간 이전 년도 1.1 ~ 4.30

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8c4d7e22-e398-4961-96ea-09239246195a)




</div>

<div id="case-study">

## 7. 사례 연구

### 데이터 사례 연구 추출

* 데이터 추출 경로

리소스 >> 추가된 데이터 관리 >> 데이터 소스 추가 >> 데이터 추출

다음과 같이 데이터 추출을 클릭하여 원하는 필드만 가져와 저장한다.

그 후 data <==> 데이터 추출 을 스왑하면서 이용할 수 있다.

![Google_Studio_Table21](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0774e8bb-80e3-4ea8-a9ce-282d801a635e)


</div>

<div id="time-series-graph">

## 8.시계열 그래프


### 1.시계열 그래프 소개




### 2.시계열 그래프 만들기

시계열 그래프, 드릴 다운

OutPut

![Google_Studio_Table21](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/7b6a04d0-dbc9-4cc4-a24e-677dd8a203f8)

세부 측정 기준:채널 추가

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/05194acd-68bb-4914-8c00-bdbdd34ac1f6)


### 3.기간 변경

측정 기준: 연도별, 연도별 분기, 연도별 월, 요일별 판매 시계열 그래프

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/990f2a3c-325d-46e4-ae40-f4b88e787628)


### 4. 스타일과 서식

#### 차트 >> 스타일 >> 시리즈 >> 참조선 추가

##### 선1

* 유형:상숫값
* 값:1600000
* Show label

##### 선2

* 유형:측정항목 >> Sales
* 계산:평균값
* 라벨:평균값
* Snow label

* 축 표시

OutPut

![Google_Studio_Table24](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/116119de-2529-4e47-9563-a6cf0b68a83a)


### 5. 시계열 차트 옵션

설정 >> 기본 기간 >> 맞춤

기본기간:2018.1.1 ~ 2018.12.31
비교기간:이전기간

OutPut

![Google_Studio_Table25](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/31006c1d-3a63-4ba9-83e2-e8b6e05b2500)


### 6.영역 그래프

차트 추가 >> 영역 차트 >> 설정

측정기준:연도 분기
세부 측정기준:Region
측정항목:Sales

스타일

스택표시

OutPut

![Google_Studio_Table26](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8df29c12-c8ff-4c2b-be47-e466e76f4783)




### 7.과제

#### 1. 연도별 매출액

#### 2. 연도별 매출현황

#### 3. 요일별 매출

#### 4. 아시아 지역 연월별 매출액

#### 5. 각 채널에 대한 2018년 월별 매출을 표시하는 누적 영역 그래프. 필터를 사용하여 국가 변경


### 8.과제 완료

OutPut

![Google_Studio_Table27](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/bdd9b9a5-6f5a-4874-9f84-a99188d7fd91)



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












