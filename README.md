# ![로고](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/064c9d75-fbd9-40b2-867c-a31359cfc231) PROJECT 소개

![브로셔메인](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/cfc3c265-097b-44e4-85bf-d4250a1c1d47)

> ✨ 기술 스택 : `React` `Spring` <br>
> 
> 🚩 개발 기간 : 2023.05.23 ~ 2023.06.29 <br>
>
> ➡️ URL : https://ohpick.shop/

<br>

<br>

## ![로고](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/064c9d75-fbd9-40b2-867c-a31359cfc231) 서비스 소개 <br>


    📢  저희 'OhPick'은 우리만의 오피스 공간이 필요하신 분들을 위해 개인이 가진 공간을 오피스 공간으로 
        공유, 대여할 수 있도록 중개하는 서비스입니다.
        
        개인 작업실부터 큰 규모의 팀 공간까지 다양한 유형의 오피스 정보를 제공해 드립니다. 
        간편한 지역 검색 및 필터링 기능으로 원하는 조건에 맞는 오피스를 손쉽게 찾을 수 있을 뿐만 아니라
        간편 예약 서비스까지 제공하여 고객이 원하는 날짜에 빠른 예약이 가능하도록 설계하였습니다.


<br>

<br>

## ![로고](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/064c9d75-fbd9-40b2-867c-a31359cfc231) 아키텍처 구성도 <br>

![아키텍처 구성도](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/13250ebe-c18e-4b8e-a9bd-30b91f8f2eab)


<br>

<br>


## ![로고](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/064c9d75-fbd9-40b2-867c-a31359cfc231) 주요 기능 <br>


<details>
  <summary> 1️⃣ 게시글 CRUD 기능 (포스트 작성, 조회, 수정, 삭제) </summary>
  
</details>
<details>
  <summary> 2️⃣ 예약 및 채팅 기능 </summary>
  
</details>
<details>
  <summary> 3️⃣ 키워드 / 지역 별 검색 및 로그인, 회원가입 기능 </summary>
  
</details>
<details>
  <summary> 4️⃣ 마이페이지 (글 목록 조회, 로그아웃 및 회원 탈퇴) 기능 </summary>
  
</details>

<br>

<br>



## ![로고](https://github.com/ShareOffice-11/OHPickOfficial/assets/83201893/064c9d75-fbd9-40b2-867c-a31359cfc231) 기술적 의사 결정 <br>

### 👥 FRONT-END

<details>
  <summary> Reac-query </summary>

|  |  |
| --- | --- |
| **도입 이유** | react-query를 사용해 서버 상태를 관리하여 캐싱 처리로 속도와 성능을 개선 하기 위해 도입하였습니다. |
| **문제 상황** | 저희 OHPick서비스는 사용자들에게 많은 오피스 데이터들을 쾌적하게 제공해야 합니다. 특히 주요 기능인 오피스 검색(무한스크롤), 채팅 등에서 사용자의 검색 필터링에 따라 수시로 데이터 결과 값이 변경되어야 합니다. 많은 데이터가 수시로 변경되는 부분에 있어 속도와 성능 관련하여 문제가 있을 수 있다고 판단하여 성능적인 측면에서 캐싱 처리를 고민했습니다. |
| **해결 방안** | 1. Axios만을 이용한 데이터 통신 <br>
2. Axios와 React Query를 함께 사용하여 서버 상태 관리 |
| **의견 조율 및 의정** | ⇒ `성능을 위해 캐싱 기능에 대한 고려가 필요`<br>
<br>
1. Axios는 HTTP 요청을 처리, 캐싱과 상태 관리는 지원하지 않음<br>
2. 상태 관리와 캐싱이 필요할 경우 React-query와 함께 사용하는 것이 더 적합<br>
3. 리액트 쿼리의 장점(최신 데이터 자동 동기화 기능, 캐싱, 서버 데이터 처리 로직 분리로 가독성 및 유지보수성 증가 등)<br>
<br>
react-query를 사용하게 되면 캐싱 데이터를 사용하여 중복되는 데이터 요청을 줄이고, 필요할 때에 캐싱된 데이터와 새로 업데이트 된 데이터를 새로 가져올 수도 있습니다. 이렇게 캐싱 처리된 데이터를 사용하게 되면 사용자가 빠르게 데이터를 확인할 수 있기 때문에 사용자 경험성이 향상될 것으로 판단하여 react-query를 도입하였습니다. |
| **결과** | ⇒ `성능을 위해 캐싱 기능에 대한 고려가 필요`

1. Axios는 HTTP 요청을 처리, 캐싱과 상태 관리는 지원하지 않음
2. 상태 관리와 캐싱이 필요할 경우 React-query와 함께 사용하는 것이 더 적합
3. 리액트 쿼리의 장점(최신 데이터 자동 동기화 기능, 캐싱, 서버 데이터 처리 로직 분리로 가독성 및 유지보수성 증가 등)

react-query를 사용하게 되면 캐싱 데이터를 사용하여 중복되는 데이터 요청을 줄이고, 필요할 때에 캐싱된 데이터와 새로 업데이트 된 데이터를 새로 가져올 수도 있습니다. 이렇게 캐싱 처리된 데이터를 사용하게 되면 사용자가 빠르게 데이터를 확인할 수 있기 때문에 사용자 경험성이 향상될 것으로 판단하여 react-query를 도입하였습니다. |
  
</details>





