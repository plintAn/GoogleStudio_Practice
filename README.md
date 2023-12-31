# 구글 스튜디오 & 구글 애널리틱스 연동 대쉬보드 개발 연습

 구글 애널리틱스의 웹 사이트, 앱의 트래픽, 세션 데이터를 구글 스튜디오에 연동합니다. 구글 스튜디오는 GA4보다 다양한 분석 리포트를 제공하며, 구글 스튜디오의 기능인 대시 보드 자동 업데이트 및 자동 전송 서비스를 합쳐 웹 사이트, 앱 데이터 대시보드를 자동으로 갱신하여 전송하는 서비스를 구축할 수 있다.

## Google Analytics 4(GA4) 대신 Google Studio를 사용하는 이유

GA4는 웹 사이트 혹은 앱 사용자의 세션 및 트래픽 분석 중심 도구이고, Studio는 데이터 시각화 도구로 데이터 소스를 추출, 변환 및 로드(ETL)하는 조금 더 복잡하고 세밀한 작업으로 대시보드 구성 요소를 개별적으로 만들어내어 표현한다. 즉 GA4는 웹 사이트, 앱의 데이터를 수집하고 Looker은 다양한 데이터 웨어하우스 및 데이터베이스를 직접 연결하여 데이터를 추출하고 분석한다. 



## Google Analytics vs Looker: 주요 차이점

| 번호 | 카테고리                       | Google Analytics                                | Looker                                             |
|------|--------------------------------|-------------------------------------------------|----------------------------------------------------|
| 1    | 용도와 주요 기능               | 웹사이트와 앱의 사용자 행동 및 트래픽 분석       | 복잡한 데이터 분석 및 대시보드 생성                 |
| 2    | 데이터 소스                    | 웹사이트와 앱의 트래픽 데이터                    | 다양한 데이터 웨어하우스 및 데이터베이스 연결        |
| 3    | 사용자 정의 및 확장성          | 기본 제공되는 메트릭 및 차원에 국한된 보고서      | SQL과 LookML을 이용한 고급 데이터 모델링 가능        |
| 4    | 데이터 저장 및 처리            | 자체 인프라에 저장 및 처리                        | 원본 데이터를 데이터 웨어하우스에서 실시간 쿼리     |
| 5    | 통합 및 API                   | Google 제품과의 통합, API 제공                   | 고급 API 제공, 다양한 플랫폼과의 통합 가능           |
| 6    | 가격 정책                     | 무료버전 및 유료버전 제공                        | 사용자 수, 데이터의 크기 등에 따라 가격 변동        |



## 과정에서 배운 주요 기능

* Google 스프레드시트와 데이터 스튜디오 연동: 데이터 로드 및 연결 방법 학습.
* 데이터 시각화 도구 활용: 피벗 테이블, 시계열 그래프, 다양한 차트와 슬라이서 등의 활용 방법 습득.
* 사용자 지정 계산 및 집계: 복잡한 데이터 분석과 집계 방법의 활용 방법 학습.
  
## 이를 활용할 수 있는 예시

### 1.매출 분석
* Google 스프레드시트에 기록된 월별 매출 데이터를 데이터 스튜디오로 불러와 시계열 그래프를 이용해 월별 매출 추이를 한눈에 확인 가능.
### 2.재고 관리
* 피벗 테이블을 활용하여 제품별 재고 수량을 정리하고, 특정 기준에 따라 재고가 부족한 제품을 즉시 확인.
### 3.예산 계획 및 모니터링
* 사용자 지정 계산을 활용하여 각 부서별 사용 예산과 실제 사용 금액의 차이를 분석.
### 4.마케팅 캠페인 분석
* 다양한 시각화 도구를 이용해 광고 캠페인별 ROI(Return on Investment)를 비교하여 가장 효과적인 캠페인 전략 파악.
### 5.고객 행동 분석
* 구글 애널리틱스 데이터를 활용하여 웹사이트 내 사용자의 행동 패턴을 분석하고, 개선점 도출.

<!-- 목차 -->

# 차 례

| 번호 | 내용                                             |
|------|--------------------------------------------------|
| 1  | [구글 스튜디오](#intro)                             |
| 2  | [테이블](#table)                                   |
| 3  | [데이터 집계](#data-aggregation)                   |
| 4  | [피벗 테이블 및 카드 시각화](#pivot-and-card)       |
| 5  | [슬라이더 및 시각화 필터](#slider-and-filter)       |
| 6  | [맞춤 계산](#custom-calculation)                   |
| 7  | [사례 연구](#case-study)                           |
| 8  | [시계열 그래프](#time-series-graph)                |
| 9  | [기타 시각화](#other-visual)                       |
| 10 | [대화형 대시보드 게시 및 공유](#dashboard)          |
| 11 | [사례 연구2](#case-study2)                         |
| 12 | [결론](#conclusion)                                |



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

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e510eaa7-4984-4518-9c76-ce0a862f0dcc)

</div>

<div id="table">

## 2. 테이블

### 1) 테이블 만들기

* 보고서 페이지 내에서 '테이블' 위젯을 선택하여 드래그&드롭으로 페이지에 추가
* 오른쪽 '데이터' 탭을 통해 원하는 열을 테이블에 추가

OutPut

![Google_Studio_Table1](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8d08d7d5-73bd-4266-95b0-2541e9f7e649)
  
### 2) 표 서식 지정 및 정렬

* 테이블의 각 열의 제목을 클릭하면 정렬 옵션을 볼 수 있다 원하는 방식대로 오름차순 또는 내림차순으로 정렬할 수 있다.

OutPut

![Google_Studio_Table2](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2fe9c3f9-dcf1-4b21-8fd3-cde9186b3070)


### 3) 다중 서식 조치(교차 포함)

* 테이블에서 다중 서식을 적용하려면, 원하는 셀이나 열을 선택 후 서식 메뉴에서 '다중 서식' 옵션을 선택합니다. 교차되는 부분에 대한 서식도 동시에 조절할 수 있습니다.

OutPut

  ![Google_Studio_Table3](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/ecd02f73-1627-4f99-9d10-6eb839c57d9d)

### 4) 조건부 서식

* 조건부 서식을 통해 특정 조건에 맞는 데이터에 대해 다른 스타일을 적용할 수 있습니다. 예를 들면, 수익이 특정 금액 이상일 때 셀의 배경색을 변경하는 것과 같은 작업입니다.

OutPut

![Google_Studio_Table4](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e0e3fbeb-91b8-4934-8975-53546210931c)

   
### 5) 실무 활동 연습

#### 1.매출이 가장 높은 제조업체는 어디입니까?
- 답변 - Fabrikam – 12,054,281

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9838ad10-3619-4ac6-b9e5-2cc33d99ca9f)

  
#### 2.이익 값이 가장 낮은 제품 범주는 무엇입니까?
- 답변 - 오디오 – 577,270

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/7ee06038-7d78-4784-abfc-72c2cdf9d9cb)

  
#### 3.어느 제조업체가 가장 높은 이익을 얻었습니까?
- 답변 - Fabrikam – 7,158,977

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c0dff7be-6080-4e88-9a57-96b3eee02f0b)

  
#### 4.판매 비용이 가장 높은 채널은 무엇입니까?
- 답변 - 매장 – 13,671,368

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e7b6b34b-5b74-430a-aeec-17630cda42dc)

  
#### 5.매출이 가장 높은 프로모션 이름은 무엇입니까?
- 답변 - 할인 없음 – 18,329,360

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/b5fd68fb-7e95-4424-a577-05deb23b9d10)

  
#### 6.이익이 가장 높은 제품 하위 범주는 무엇입니까?
- 답변 - 캠코더 – 4,972,853

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8800c56f-6b67-4d7a-a743-844d1ab84830)

</div>

<div id="data-aggregation">

## 3. 데이터 집계

집계는 데이터를 분석할 때 사용하는 기본적인 방법입니다. 여러분이 가지고 있는 데이터를 적절하게 분석하고 시각화하기 위해서는 다양한 집계 방법을 사용할 수 있습니다. 본 포스팅에서는 Google Studio의 기본적인 집계 방법에 대해 소개하겠습니다.

### 1번 테이블

이 테이블에서는 제조사별 총 매출을 살펴볼 수 있습니다.

* 측정기준 : Manufactors
* 측정항목 : Salses

* SUM : Total Sales
* AVG : Avg Sales
* MIN : Lowest Sales
* MAX : Highest Sales

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/336dc3f9-b910-4781-9969-f1b0c64496bd)

이 이미지는 제조사별 매출을 다양한 측정항목으로 집계한 결과를 나타냅니다.


### 2번 테이블

제품의 하위 카테고리와 제품 이름에 대한 집계 방법을 설명하고 있습니다.

* 측정기준 : Product sub category
* 측정항목 : Product Name

* CT : No of Trans
* CTS : No of Products

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/865e1a7d-ba65-47f2-b526-b741f7520bb4)

이 이미지는 제품 하위 카테고리별 제품 이름의 거래 횟수와 제품 수를 집계한 결과를 나타냅니다.

### 2) 실무 집계 연습

위 배운 방식으로 실무에서 쓰일 수 있는 테이블을 시각화 해보겠습니다.

#### 1. 제품 이름별 총 매출을 보여주는 새 테이블 만들기

- 가장 높은 판매에서 가장 낮은 판매로 표를 정렬합니다. 가장 많이 팔린 제품은?

- 답변 - Contoso 프로젝터 1080 P X980 검정 – 445,115

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/a1541996-7a73-4658-86a0-99ddf81500b6)

#### 2. 가장 낮은 매출에서 가장 높은 매출 순으로 표를 정렬합니다. 판매량이 가장 적은 제품은 무엇입니까?

- Answer - SV USB 데이터 케이블 E 600 그레이 - 46

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c84b6d11-b183-4d57-96dc-a28143269899)


#### 3. 가장 많은 도시에서 판매되는 제품은 무엇입니까?

- 답변 - Litware 홈 시어터 시스템 5.1 채널 M515 브라운 – 22

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/a95f6961-6359-4f77-b5b2-67ee8c259475)


#### 4. 국가별 총 매출을 보여주는 새 테이블 만들기

- 요약 방법을 다음과 같이 변경합니다.

- 평균 – 평균 매출이 가장 높은 국가는 어디입니까?

- 답변 - 중국 – 4518

- Min – 최소 매출이 가장 낮은 국가는 어디입니까?

- 답변 - 중국, 싱가포르, 미국 - 5

- Max – 최대 매출이 가장 높은 국가는 어디입니까?

- 답변 - 미국 - 78312

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/91d02bb3-3df1-4d22-9919-42a41ac28cbd)


#### 5. 도시별 이익을 표시하는 새 테이블을 만듭니다.

- 거래 건수가 가장 많은 도시는 어디입니까?

- 답변 - 베이징 - 1398

- 평균 이익이 가장 낮은 도시는 어디입니까?

- 답변 - 베네치아 - 438

- 가장 다양한 유형의 제품을 판매하는 도시

- 답변 - 베이징 - 924
  
OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/fc0a0e27-7f60-48e2-97a8-b1f535f17555)




### 3) 비교 계산

이 섹션에서는 데이터의 특정 값을 서로 비교하여 통계적 또는 분석적 정보를 얻습니다. 그래프에 표시된 값들은 서로의 비교를 통해 특정 패턴이나 추세를 파악하는 데 도움을 줍니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/48589610-e299-4a5d-a2ac-5a6f28ded3c1)



### 4) 누계 계산

누계는 데이터를 순서대로 더하는 방식으로, 특정 기간 동안의 누적된 값을 보여줍니다.

* 총계 백분율:

전체 중 특정 항목의 비율을 표시합니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/69f6fdd6-0258-434d-b805-289af72c03b4)

* 누계 백분율:

누적된 백분율 값을 표시합니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/826630e7-0052-4b50-a49e-e2463f0f1a66)

* 하위 범주 누적 백분율:
  
하위 카테고리에 따른 누적 백분율 값을 보여줍니다.

OutPut

![Google_Studio_Table5](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/6901b13c-1770-42b9-9690-d1ae8bd2b702)

* 최솟값 비교

데이터 집합에서 최솟값을 표시합니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/edc9befc-fc2a-488e-a563-01bc5eab5655)

* 최댓값 비교:
 
데이터 집합에서 최댓값을 표시합니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d1f7183b-5a92-433f-a791-ec397326c533)

* 집계 비교:

전체 집계된 값들의 비교를 보여줍니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9408ce4a-dd56-457c-9c45-df1cfb808930)

* 평균 비교:

전체 집계된 값들의 비교를 보여줍니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/fdd0516c-80b5-48fb-91a4-ebd0fdc3bb8f)

* 델타 비교: 

데이터의 변화량이나 차이를 나타내기 위해 사용됩니다.

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0256b15f-f418-4db8-9b92-6116ef50d97d)




### 5) 드릴 다운 ( 교차 )

드릴 다운은 데이터를 상세하게 조사하기 위한 분석 기법입니다. 사용자는 더 상세한 수준의 데이터를 살펴볼 수 있습니다.

* Region >> County >> City:

지역, 국가, 도시 순으로 데이터의 세부 정보를 확인할 수 있습니다.

OutPut

![Google_Studio_Table6](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/2d3b3fcb-0765-47ef-82d6-8376a927bdaf)

* Asia >> South Korea >> Seoul: 

아시아 지역 내에서 대한민국의 서울까지의 데이터를 상세하게 살펴봅니다.

OutPut

![Google_Studio_Table7](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/1487db46-33a1-482a-85de-cd402eb9d371)



### 6) 날짜 작업 ( 교차 )

이 섹션에서는 연도별, 분기별, 월별 및 요일별로 데이터를 정렬하고 분석합니다. 이러한 분석을 통해 시간에 따른 추세나 패턴을 파악할 수 있습니다.

연도별, 분기별 정렬

월, 요일별 정렬

OutPut

![Google_Studio_Table8](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/021a1d5c-7b70-4adc-a7d7-d3fb409a2a04)

</div>

<div id="pivot-and-card">

## 4. 피벗 테이블 및 카드 시각화

### 1) 피벗 테이블 및 스코어카드 소개

피벗 테이블은 구글 스튜디오에서 데이터를 요약하고 분석하는 데 유용한 도구로, 여러 데이터 포인트를 쉽게 비교하고 파악할 수 있게 해준다 스코어카드는 구글 스튜디오의 시각화 도구 중 하나로, 중요한 통계나 정보를 강조해서 한 눈에 볼 수 있게 표시하는 역할을 한다 이렇게 해서, 둘 다 구글 스튜디오에서 데이터를 효과적으로 전달하고 분석하는 데 큰 도움이 됩니다


### 2) 피벗 테이블 만들기

OutPut

![Google_Studio_Table11](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c713d30c-c5be-43a9-b538-c9baccfde474)

이 이미지는 피벗 테이블의 기본 구조를 보여줍니다. 행과 열을 기준으로 데이터가 어떻게 분류되고 집계되는지 한눈에 확인할 수 있

### 3) 비교 계산

OutPut

![Google_Studio_Table9](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/99cf3474-ae6b-4070-a7c0-2a2d874a8ea7)

비교 계산은 데이터 간의 차이나 증감을 시각적으로 표현하여 데이터의 변화나 트렌드를 파악하는 데 도움을 줄 수 있다.

### 4) 카드 시각화

OutPut

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

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/eb25580f-7e92-4cf3-858c-7dae4c3d0037)

이 이미지는 실무에서 사용할만한 데이터 시각화를 예시로 보여준다. 각 카드는 특정 지표에 중점을 둔 시각화로 구성되어 있습니다.

</div>

<div id="slider-and-filter">

## 5. 슬라이더 및 시각화 필터

### 1.슬라이더 및 시각화 필터 소개

슬라이더와 시각화 필터는 Google Studio의 대시보드에서 데이터를 동적으로 탐색하고, 특정 조건 또는 값 범위에 따라 시각화를 업데이트하는 데 사용되는 컨트롤입니다. 이를 사용하면 사용자는 대시보드 내에서 원하는 데이터를 쉽게 선택하거나 필터링할 수 있습니다.

OutPut

![Google_Studio_Table12](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/753a4b27-15cf-4c7f-bedb-7d6d4c19d1db)

위 이미지는 슬라이더와 시각화 필터의 기본 인터페이스를 보여주는데, 이 도구들은 Google Studio의 대시보드에서 데이터를 동적으로 탐색하고 조작하는 데 사용된다

### 2.텍스트 슬라이더

텍스트 슬라이더는 고정 크기 목록, 드롭 다운, 고급 필터와 같은 텍스트 기반의 값에 따라 데이터를 필터링하는 데 사용됩니다.

컨트롤 추가 >> 고정 크기 목록, 드롭 다운, 고급 필터 추가

OutPut

![Google_Studio_Table13](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/db69f52c-4e5d-4bc1-96fd-eae50685360f)

이 이미지는 텍스트 기반의 값에 따라 데이터를 필터링하는 텍스트 슬라이더의 예를 보여준다.


### 3.숫자 슬라이더

숫자 슬라이더는 특정 숫자 범위 내의 데이터를 선택하거나 필터링하는 데 사용된다

컨트롤 추가 >> 슬라이더 추가

OutPut

![Google_Studio_Table14](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d1ac907d-98cf-4a3f-aad5-38ed09147870)

숫자 슬라이더 예시 이미지입니다. 사용자는 이 슬라이더를 조작하여 원하는 숫자 범위의 데이터를 쉽게 선택할 수 있다.


### 4.날짜 슬라이더

날짜 슬라이더는 특정 날짜 범위에 따라 데이터를 필터링하는 데 사용된다. 특히 특정 연도나 분기의 데이터만을 보고 싶을 때 사용할 수 있다.

OutPut

![Google_Studio_Table15](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/cfb462f3-8732-4c44-abbf-3b724a8fe219)

특정 날짜 범위를 선택하여 데이터를 필터링할 수 있는 날짜 슬라이더의 예시


### 5.텍스트 시각화 필터

특정 문자 또는 단어로 시작하는 텍스트를 기반으로 데이터를 필터링한다. 예를 들어, 지역 이름이 'I' 또는 'O'로 시작하는 데이터만을 선택할 수 있습니다.

I 또는 O로 시작하는 지역 이름 필터

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9d455d8b-57af-4e12-8aad-1481c67b3db0)

OutPut

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/ebbe0051-5845-4d88-abc6-03f2b4533eb5)


### 6.숫자 시각화 필터

특정 숫자 조건을 기반으로 데이터를 필터링한다. 예를 들어, 특정 판매량 이상의 데이터만을 선택할 수 있다.

속성 >> 측정항목 >> 측정항목 v 

OutPut

![Google_Studio_Table16](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/1737bf26-7be4-42c9-bd6e-dd44fe9af53c)

숫자 값을 기준으로 데이터를 필터링하는 숫자 시각화 필터의 인터페이스


### 7.날짜 시각화 필터

특정 날짜 조건을 기반으로 데이터를 필터링한다 여기에서는 2018년까지의 데이터 중에서 분기별 매출액을 나누어 보는 예제를 확인할 수 있다.

이러한 슬라이더와 필터 도구들은 사용자가 원하는 데이터를 더욱 쉽게 찾고, 분석 결과를 더욱 효과적으로 전달하는 데 큰 도움을 준다

속성 >> 기본기간 >> 맞춤 >> 기간선택

해당 자료는 2018년까지 자료가 있으므로 분기별로 매출액을 나눠보겠습니다.

OutPut

![Google_Studio_Table17](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/9f2c41cb-b334-4a08-8438-e0e3ab838968)

사용자가 특정 날짜 범위를 선택하여 데이터를 필터링할 수 있도록 도와주는 날짜 시각화 필터의 인터페이스이다

이러한 이미지들은 Google Studio의 다양한 필터와 슬라이더 도구를 시각적으로 이해하는 데 도움을 준다.


</div>

<div id="custom-calculation">

## 6. 맞춤 계산

### 1. 사용자 지정 계산 소개



### 2. 계산 만들기

OutPut

![Google_Studio_Table19](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/cd2f05e2-9f67-4cc2-8bad-9dc5d2c9911d)


OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/f1dec162-be4b-4b33-91ec-edfb576836ed)


### 3. 실제 활동

* 평균 매출 - Avg(Sales)

* 최고 판매 - Max(Sales)

* 제품 수 - Count_Distinct(Products Name)

* 제품당 평균 매출 - Sum(Sales)/Count_Distinct(Products Name)

### 4. 실습 완료

OutPut

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

### 차트 비교

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

OutPut

![Google_Studio_Table21](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0774e8bb-80e3-4ea8-a9ce-282d801a635e)


</div>

<div id="time-series-graph">

## 8.시계열 그래프


### 1.시계열 그래프 소개

이 섹션에서는 시계열 그래프를 중점적으로 다룬다. 시계열 그래프는 시간의 흐름에 따른 데이터의 변화를 시각적으로 나타내주는 도구로, 데이터의 추세를 파악하거나 미래의 변화를 예측하는 데 유용하게 사용된다.


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

### 1. 다른 시각화 소개

* 데이터 스튜디오 내에서 사용 가능한 다양한 시각화 방법에 대한 소개

### 2. 열 및 막대 그래프

* 값들 사이의 크기 차이를 비교하기 위한 방법
* 항목 간의 크기 차이 이해하기

* 측정기준:Manufacturer, Product Category, Product Sub Category
* 시부 측정기준: Region
* 측정항목: Sales

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/8890fab0-6d47-4d6d-af30-e620f4d5cbb5)



### 3. 파이 그래프

* 전체에 대한 기여 및 백분율 확인
* 올바른 사용 방법 및 오용되는 경우 알아보기

#### 설정

* 측정기준:Manufacturer
* 측정항목: Sales

#### 스타일

* 원형차트:5개 조각
* 색상표시:원형 차트 순서
* 라벨>슬라이스 라벨 > 비율
* 범례:상단

![Google_Studio_Table28](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/71b48970-2099-48a7-b8c8-b2372a936b01)


OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/135fc3f7-ee36-498a-907a-995294e8118f)


### 4. 지리적 분석

* 지도를 사용한 시각화 방법 탐색
* 국가, 도시 등의 지리적 데이터 매핑 방법 소개

### 지역 차트

#### 설정

* 측정기준:Country
* 측정항목: Sales
* 측정항목 슬라이더

#### 스타일

* 지역차트:최대, 중간, 최소 값 색상 지정
* 범례 표시

전세계, 유럽, 아시아 

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/158c555d-0d29-44c5-948d-dd81b8a6e214)

### 버블 차트

#### 설정

* 위치:Country
* 크기: Sales

OutPut

![Google_Studio_Table30](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/7e488989-c35a-4f8b-9dc1-f9dd6af96c50)


### 5. 트리맵 그래프

* 사각형을 사용하여 데이터 크기 표현하기
* 어떤 값이 크고 어떤 값이 작은지 확인하기

#### 설정

* 측정기준:Country, City
* 측정항목: Sales

#### 스타일

트리맵: 최댓값 색상(브라운), 최솟값 색상(오렌지), 중간값 색상(회색)

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0f18254c-d28a-4550-8dd7-0753988ad68f)


### 6. 산점도 그래프

* 상관관계 분석을 위한 시각화
* x축과 y축을 사용한 변수 간의 관계 파악
* 버블 도표를 이용하여 세 번째 변수 표현하기

#### 설정

* 측정기준:Product Category
* 측정항목(X축): Sales
* 측정항목(X축): Profit
* 풍선 크기 측정항목: Order Qty

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/e7460905-f899-4fd1-a126-e3a270a196b3)


### 7. 맞춤형 시각화

* 데이터 스튜디오를 위한 사용자 정의 시각화 방법
* 데이터 가져오기, 형식화 및 스타일링 방법 소개

커뮤니티 시각화 및 구성요소 >> 더보기 >> 게이지

#### 설정
Metric:Sales, Profit
#### 스타일
Green Selection : 70, 80
Yellow Selection : 50, 70
Red Selection : 0, 50


OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/c14beb8d-65a0-4cdc-8551-1fd6f4bd16c1)


</div>

<div id="dashboard">

## 10. 대화형 대시보드 게시 및 공유

### 1.대시보드 소개

이 대시보드 보고서는 영업 관리자와의 협업을 위해 만들어 졌다. 이 보고서에는 다양한 시각화와 필터링 기능이 포함되어 있으며, 이를 통해 사용자는 보고서를 공유하고 공동 작업할 수 있습니다. 또한 이 보고서를 이메일로 전송하는 기능과 웹사이트에 삽입하는 기능도 제공됩니다. 여러 능력을 활용하여 효과적인 보고서 작성과 공유를 할 수 있습니다.

### 2.대화형 대시보드 게시 및 공유 섹션

다음 카드 시각화 만들기

· 총 매출

· 총 이윤

· 평균 매출

· 이익의 평균

· 판매된 제품 수(제품명)

- 연도 및 분기별 매출을 표시하는 선 그래프

- 제품 범주별 매출을 표시하는 막대 그래프

- 상위 10개 국가 판매 열 그래프

- 채널별 이익 – 도넛형 그래프 – 백분율 데이터 레이블 추가

- 필터로서의 지역



### 3.대시보드 만들기

#### 상단 바: 도형 >> 사각형, 텍스트 >> 'Sales Report '

#### 스코어 카드: 차트 >> 스코어 카드 >> 설정


* 총 매출:  측정항목(Sales)
* 총 이익:  측정항목(Profit)
* 평균 매출:  측정항목(Avg Sales)
* 평균 이익: 측정항목(Avg Profit)
* 상품 판매 종류: 측정항목(No of products)

#### 판매 시계열 차트: 차트 >> 시계열 차트 >> 설정

연도 및 분기별 매출을 표시하는 선 그래프

* 측정기준:Order Date(연도 분기)
* 측정항목:Sales

제품 범주별 매출을 표시하는 막대 그래프

* 측정기준:Product category
* 측정항목:Sales

상위 10개 국가 판매 열 그래프

* 측정기준:City
* 측정항목:Sales

채널별 이익 – 도넛형 그래프 – 백분율 데이터 레이블 추가

* 측정기준:Channel
* 측정항목:Sales

필터로서의 지역

* 측정기준:Order Date(연도 분기)
* 측정항목:Sales

지역별 필터 >> 컨트롤 추가 >> 고정필터 추가

* 컨트롤 필드:Region

OutPut

![Google_Studio_Table31](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/82785f80-e159-498f-b123-a9892b839e01)



</div>

<div id="case-study2">

## 11. 사례 연구2

### 사례 연구 소개

* 데이터 혼합: 서로 다른 데이터 소스를 하나의 테이블로 통합하는 과정을 다룬다 데이터 파일을 준비하고, 통합 테이블을 만드는 방법, 그리고 결과를 데이터 스튜디오에서 보여주는 방식을 알아보자
* 데이터 탐색기: Google의 베타 제품으로, 데이터 스튜디오와 유사하지만 다른 필터링 방법을 제공하는데 이 제품으로 생성된 파일을 어떻게 가져와 데이터 스튜디오에 넣는지를 알아보자
* Google 애널리틱스: 데이터 스튜디오를 활용한 가장 강력한 사용 사례 중 하나로, Google Analytics 데이터 소스와의 연결 방법과 간단한 시각화를 만드는 방법을 살펴보자

### 2. 교육 데이터 파일 다운로드

데이터 다운로드

### 3. 데이터 혼합을 위한 파일 준비

구글 스프레드 시트에 업로드, 구글 스튜디오에서 데이터 import

### 4. 데이터 혼합

* 구글 스튜디오 >> 리소스 >> 추가된 데이터 소스 관리 >> 데이터 소스 추가 >> 스프레드 시트 import >> 혼합 데이터 관리 >> 데이터 혼합 추가 

* Table 1(Data Blend - Master) , Table 2(Table Name) Left outer join


데이터 측정기준

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/566763bf-a3f2-4321-a6fc-1d7b8bca3939)


OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/ef9971a1-3550-4acd-ad67-13958d924050)



### 5. 데이터 탐색기

 "Data Explorer"라는 Google에서 제작한 베타 제품에 대한 소개

 데이터 익스플로러는 데이터를 필터링을 지원하는 도구이다. 이는 판매 데이터를 보고, 유럽 지역의 국가별 판매 데이터를 필터링하여 표로 표시하는 도구로 사용된다.

경로:Looker Studio >> 만들기 >> 탐색기 >> 데이터 소스 선택 >> 필터 적용

OutPut

 ![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/0a8e199f-9a8e-4e9a-a717-678b3eb7f62b)


### 5. 구글 애널리틱스 & 구글 스튜디오 연동하여 활용

경로: 

Looker Studio Home >> 데이터 소스 >> Google 애널리틱스 >> Demo Account >> GA4-Google Merch Shop 추가

OutPut

![image](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/51803c20-8fe1-4fdc-808c-4b3788ed5fc1)


#### 1.총 조회수 스코어 카드

* 측정항목:총 조회수

#### 2.세션수 스코어 카드

* 측정항목:세션수

#### 3.세션 수 시계열 차트

* 측정기준:날짜
* 측정항목:세션수

#### 4.세션 소스 컨트롤

컨트톨 추가 >> 고정 크기 목록

* 컨트롤 필드: 세션 소스

#### 5.카테고리별 세션수 원형 차트

* 측정기준:기기 카테고리
* 측정항목:세션수

#### 6.페이지 제목 별 세션수 바 차트

* 측정기준:페이지 제목
* 측정항목:세션수

OutPut

![Google_Studio_Table32](https://github.com/plintAn/GoogleStudio_Practice/assets/124107186/d78902c5-c989-4204-9000-8ca6c2044080)


</div>

<div id="conclusion">

## 12. 결론

이 과정은 Google 스프레드시트와 데이터 스튜디오의 기능을 깊게 파헤쳐 본 결과, 데이터를 효과적으로 로드, 분석, 시각화하는 방법에 대한 포괄적인 이해를 도와준다. 핵심적으로, 이 과정을 통해 우리는 데이터를 명확하게 표현하는 데 필요한 테이블 작성, 집계 방법, 피벗 테이블 및 다양한 시각화 도구 활용 방법을 알 수 있었다.

더불어, 사용자 지정 계산을 활용한 복잡한 데이터 분석부터, 대화형 대시보드의 제작 및 공유 방법을 다루었는데 특히, 실제 사례 연구를 통한 접근은 이론적 지식을 실제 활용하는 능력을 키울 수 있게 하는 혁신적인 기술이었다고 평가한다.

마무리로, 이 과정의 지식은 데이터 중심의 현대 사회에서 매우 중요하며, 효과적인 데이터 분석과 시각화 능력은 우리에게 의사결정에서의 큰 경쟁력을 제공할 수 있다. 기업이나 조직에서 발생하는 다양한 문제 해결 또는 전략 설정 시, 이 과정에서 얻은 지식을 바탕으로 데이터를 통한 명확한 해답을 제시하여 도움을 줄 수 있을 것이다.


</div>












