<div align=center><h1>🥗야금야금</h1></div>
냉장고 관리와 재료 기반 레시피 큐레이션 및 커뮤니티 기능을 통합 제공하고 쇼핑몰 기능을 추가하여 식재료에 관한 모든 것을 한번에 해결할 수 있는 통합 웹 서비스입니다.
<br><br>

* [프로젝트 개발 계획서](https://drive.google.com/file/d/1_PssbkaE6d5KJAjxExHMQXwDqBo37Z3n/view?usp=drive_link)
* [프로젝트 발표 ppt](https://drive.google.com/file/d/1VLI1FRs1U2VpuRQHEVHY4Tr-yTuZhRAN/view?usp=drive_link) - 페이지별 캡쳐 및 상세 설명이 포함되어 있습니다.
<br>

## 목차
1. [개요](#1.-개요)
2. [아키텍처](#2.-아키텍처)
3. [주요-기능](#3.-주요-기능) <br>
   3-1. [회원](#3-1.-회원) <br>
   3-2. [관리자](#3-2.-관리자)
4. [회고](#4.-회고)
<br>

## 1. 개요
* 개발 기간: 2023.05.22 ~ 06.30
* 개발 인원: 총 5명

### 개발 배경
고물가가 지속되는 가운데 코로나로 급증했던 배달 음식 수요가 감소하고 외식 대신 집에서 식사를 해결하는 가구가 증가하고 있다. 이에 시중에 있던 냉장고 식재료 관리 앱의 기능에 레시피 큐레이션 및 커뮤니티 서비스와 식재료 쇼핑몰을 통합하여 식재료에 관한 모든 것을 한번에 해결할 수 있는 통합 웹 서비스를 개발하고자 하였다.

### 프로젝트 시연
[시연 영상](https://drive.google.com/file/d/1WK0oqW7QR3gBUofHMrBOI_sQ6pe1mufp/view?usp=drive_link)
<img src="https://github.com/comiraioi/Project_YagumYagum/assets/134984755/5dc8531c-cbb7-4eaa-9caf-cee6749b736c" width=600> <br>

## 2. 아키텍처
* 기술 스택 및 활용 데이터 <br>
<img src="https://github.com/comiraioi/Project_YagumYagum/assets/134984755/082ecc6e-957e-4b9f-a533-145846f89330" width=600> <br><br>
* 와이어 프레임 및 사이트 맵 <br>
<img src="https://github.com/comiraioi/Project_YagumYagum/assets/134984755/09fab3be-db88-4482-a6df-99b438a5248d" width=600>  <br><br>
* ERD <br>
<img src="https://github.com/comiraioi/Project_YagumYagum/assets/134984755/8d456446-50ac-4cef-bad0-cad817703d70" width=600>  <br><br>

## 3. 주요 기능
페이지 별 캡쳐 및 상세 설명은 [여기](#프로젝트-개발-계획서) 참고

#### ⭐ 담당 역할
팀 내 기여도 30% (총 5명)
* Backend
나의 냉장고 (통계, 보관 위치 별 식재료 리스트, 식재료 추가 및 수정, 소비기한 계산)
/ 장보기 메모 (메모 추가 및 삭제, 체크박스)
/ 식재료 관리 (목록, 추가, 수정, 삭제)
* Frontend
메인 페이지 와이어프레임 및 사이트 맵 구성 / 전체적 디자인 수정 / 사용자 메인 	페이지 헤더, 네비게이션, 슬라이드 배너 / 관리자 메인 페이지
* Etc
노션을 통해 프로젝트 일정을 관리하고 주간 회의 주도 / 프로젝트 보고서 및 발표 자료 작성

### 3-1. 회원
<div>
<details>
<summary>⭐ 메인 페이지</summary>
<ul>
    <li>⭐ 슬라이드 배너: 사이트 소개 및 추천 레시피</li>
    <li>찜 많은 순 레시피 상위 4개</li>
    <li>상품 목록</li>
</ul>
</details>
</div>
<div>
<h4>회원가입 및 로그인</h4>
<dd>
<details>
<summary>회원 가입</summary>
<ul>
    <li>회원가입 창에서 정보를 입력하여 가입한다.</li>
    <li>회원가입이 되어있지 않은 상태에서 카카오 로그인하기 버튼을 누르면 사용자의 카카오 계정 정보로 폼이 채워진 회원가입 창으로 이동한다.</li>
    <li>주소 입력 시 카카오 우편번호 검색 API 사용</li>
</ul>
</details>
<details>
<summary>로그인</summary>
<ul>
    <li>회원 가입한 정보를 통한 로그인</li>
    <li>카카오 계정을 통한 로그인</li>
</ul>
</details>
</dd>
</div>

<div>
<h4>마이페이지</h4>
<dd>
<details>
<summary>개인 정보</summary>
<ul>
    <li>회원 정보 수정하기</li>
    <li>회원 탈퇴하가: 입력한 비밀번호가 일치하면 탈퇴 처리된다.</li>
</ul>
</details>
<details>
<summary>찜 목록</summary>
<ul>
    <li>찜한 상품 목록 확인, 정렬, 검색</li>
    <li>상품명 클릭 시 상품 상세 페이지로 이동한다.</li>
</ul>
</details>
<details>
<summary>주문 목록</summary>
<ul>
    <li>주문 정보 확인, 정렬, 검색</li>
    <li>주문 번호 클릭 시 주문 상세 페이지로 이동하여 상세 품목을 확인할 수 있다.</li>
</ul>
</details>
<details>
<summary>거래 상태</summary>
<ul>
    <li>환불 요청 버튼을 클릭하면 환불 요청 중으로 거래 상태가 바뀐다.</li>
    <li>관리자가 환불을 승인하면 환불 승인 완료로 거래 상태가 바뀐다.</li>
</ul>
</details>
</dd>
</div>

<div>
<dt><h4>⭐ 나의 냉장고</h4></dt>
<dd>
로그인 시 접근 가능한 페이지로 사용자가 보관 위치별 식재료 관리를 할 수 있다.
<details>
<summary>⭐ 배너</summary>
<ul>
    <li>식재료 통계: 보관 위치별 식재료 수, 소비기한 3일 이하 식재료 수</li>
    <li>식재료 기반 레시피 검색: 사용자 냉장고에 있는 식재료명을 넘겨주어 레시피 검색 페이지로 이동한다.</li>
    <li>식재료 기반 커뮤니티 검색: 사용자 냉장고에 있는 식재료명을 넘겨주어 커뮤니티 글 검색 페이지로 이동한다.</li>
</ul>
</details>
<details>
<summary>⭐ 식재료 목록</summary>
<ul>
    <li>슬라이드로 전체, 냉장고, 냉동고, 실온보관 등 위치별 식재료를 한눈에 확인 할 수 있다.</li>
    <li>체크박스로 보관 위치별 식재료 다중 선택 및 개별 선택이 가능하다.</li>
    <li>사용자가 등록한 식재료별 소비기한에 따라 디데이가 표시되며 7일 이하는 노란색, 3일 이하는 빨간색으로 표시된다. 소비기한 3일 이하인 식재료의 수는 상단 네비게이션에도 표시된다.</li>
</ul>
</details>
<details>
<summary>⭐ 식재료 추가</summary>
<ul>
    <li>특정 보관 위치의 슬라이드에서 추가 버튼을 누르면 해당 보관 위치로 자동 설정되며 변경도 가능하다.</li>
    <li>식재료 카테고리별 토글을 설정하였다.</li>
    <li>체크박스로 식재료를 다중 선택하여 추가할 수 있다.</li>
    <li>식재료들은 기본 소비기한이 설정되어있다.</li>
    <li>기본 식재료 목록에 사용자가 원하는 식재료가 없을 경우 사용자 추가를 선택하여 추가하면 사용자가 직접 입력할 수 있다.</li>
    <li>사용자 냉장고에 이미 있는 식재료는 재료명 앞에 체크 아이콘이 표시되어 있으며 중복 추가가 가능하다.</li>
</ul>
</details>
<details>
<summary>⭐ 식재료 수정</summary>
<ul>
    <li>기본 식재료는 소비기한 변경, 메모 추가가 가능하다.</li>
    <li>사용자 식재료는 식재료명 작성이 가능하고 카테고리 변경, 소비기한 변경이 가능하다.</li>
</ul>
</details>
<details>
<summary>⭐ 식재료 삭제</summary>
<ul>
    <li>다중 선택 또는 개별 선택하여 식재료를 삭제할 수 있다.</li>
    <li>보관 위치별로 전체 삭제가 가능하다.</li>
</ul>
</details>
</dd>
</div>

<div>
<h4>⭐ 장보기 메모</h4>
<dd>로그인 시 사용할 수 있으며 나의 냉장고, 상품 목록 페이지에서 사용자가 쇼핑 리스트를 메모할 수 있다. 작성한 메모를 클릭하면 해당 상품 검색 결과 페이지로 이동한다.
<details>
<summary>⭐ 메모 쓰기</summary>
메모 및 상세 메모 작성 후 추가가 가능하다 
</details>
<details>
<summary>⭐ 메모 저장</summary>
메모 옆 체크박스의 체크 유무가 유지된다.
</details>
<details>
<summary>⭐ 메모 삭제</summary>
메모 옆 체크박스의 체크 유무가 유지된다.
</details>
</dd>
</div>

<div>
<h4>장보기</h4>
<dd>
식재료 쇼핑 페이지입니다.
<details>
<summary>상품 목록</summary>
카테고리별 상품 보기, 상품 검색
</details>
<details>
<summary>상품 찜하기</summary>
찜 목록에 추가 및 해제
</details>
<details>
<summary>장바구니 담기</summary>
<ul>
    <li>상품 상세 페이지에서 수량 선택 가능함</li>
    <li>재고량 초과 시 추가 불가능</li>
</ul>
</details>
<details>
<summary>주문하기</summary>
<ul>
    <li>상품 상세 페이지에서 수량 선택 가능함</li>
    <li>장바구니에 추가하지 않고 바로 주문 페이지로 이동한다.</li>
</ul>
</details>
</dd>
</div>

<div>
<h4>장바구니</h4>
<dd>
<details>
<summary>상품 삭제</summary>
장바구니에서 상품 삭제하기
</details>
<details>
<summary>상품 수량 수정</summary>
장바구니에 담긴 상품의 수량 수정
</details>
<details>
<summary>주문하기</summary>
<ul>
    <li>주문하기 클릭 시 상품 주문 페이지로 이동한다.</li>
    <li>장바구니에 담긴 상품이 없으면 주문하기 버튼이 보이지 않는다.</li>
    <li>총 합이 5만원 이상이면 배송비 3000원이 할인된다.</li>
    <li>결제 완료 후에는 장바구니 리스트가 초기화 된다.</li>
</ul>
</details>
</dd>
</div>

<div>
<h4>주문 및 결제하기</h4>
<dd>
<details>
<summary>주문자 정보 입력</summary>
<ul>
    <li>이름, 번호, 주소 등 주문자 정보를 입력한다.</li>
    <li>총 합, 배송비를 합한 최종 결제 금액을 확인할 수 있다.</li>
</ul>
</details>
<details>
<summary>결제하기</summary>
KG 이니시스 결제창을 띄워 네이버페이, 카카오페이, 카드 결제 등 다양한 방법으로 결제가 가능하다.
</details>
</dd>
</div>

<div>
<h4>레시피 큐레이션</h4>
<dd>
만개의 레시피에서 크롤링한 데이터를 활용하였다.
<details>
<summary>레시피 검색 및 정렬</summary>
<ul>
    <li>키워드별(카테고리, 식재료, 분류별) 레시피 보기</li>
    <li>조회순, 찜순 정렬하기</li>
</ul>
</details>
<details>
<summary>북마크</summary>
<ul>
    <li>레시피 북마크 및 해제하기</li>
    <li>본인이 저장한 레시피 목록 확인, 카테고리별 정렬</li>
    <li>썸네일 또는 레시피명 클릭 시 레시피 상세페이지로 이동</li>
</ul>
</details>
<details>
<summary>⭐ 레시피 상세 페이지</summary>
<ul>
    <li>조회 수 및 북마크 수 표시</li>
    <li>⭐ 사용자 냉장고에 있는 재료는 옆에 체크 표시가 뜬다.</li>
    <li>재료를 클릭하면 상품 검색 결과 페이지로 이동한다.</li>
</ul>
</details>
<details>
<summary>리뷰(댓글) 등록하기</summary>
<ul>
    <li>로그인 시 댓글 작성이 가능하다.</li>
    <li>본인이 작성한 댓글 수정 및 삭제</li>
    <li>타인 댓글 신고</li>
</ul>
</details>
</dd>
</div>

<div>
<h4>방구석 쉐프</h4>
<dd>
회원들이 직접 레시피를 작성하여 올리는 커뮤니티 게시판
<details>
<summary>게시글 목록</summary>
<ul>
    <li>슬라이드 배너에 추천 수를 기준으로 게시물 띄움</li>
    <li>카테고리별 게시글 보기</li>
    <li>게시글 추천 및 추천 해제</li>
</ul>
</details>
<details>
<summary>게시글 작성, 수정, 삭제</summary>
<ul>
    <li>드래그 앤 드롭으로 이미지 파일 업로드가 가능하다.</li>
    <li>재료 추가 시 냉장고에 추가할 수 있는 재료 데이터를 바탕으로 검색 하여 추가할 수 있다.</li>
    <li>본인이 작성한 게시글만 수정 삭제가 가능하다.</li>
</ul>
</details>
<details>
<summary>댓글 및 대댓글</summary>
<ul>
    <li>로그인 시 댓글, 대댓글 작성이 가능하다.</li>
    <li>본인이 작성한 댓글은 수정, 삭제가 가능하다.</li>
    <li>타인의 댓글을 신고할 수 있다.</li>
</ul>
</details>
</dd>
</div>

### 3-2. 관리자
<div>
<details>
<summary>⭐ 메인 페이지</summary>
<ul>
    <li>매출 및 월별 가입자 수 추이</li>
    <li>사용자 게시판 최신글 5개</li>
    <li>주문 많은 상품 상위 5개</li>
    <li>주문 목록: 거래 내역 확인 및 환불 처리 가능</li>
</ul>
</details>
</div>
<div>
<h4>회원</h4>
<details>
<summary>회원 관리</summary>
<ul>
    <li>회원 목록: 회원 정보 보기, 검색, 정렬</li>
    <li>회원 삭제: 삭제 버튼 클릭 시 회원 탈퇴 처리 됨</li>
</ul>
</details>
<details>
<summary>댓글 관리</summary>
레시피 페이지와 커뮤니티 페이지의 댓글 신고 내역을 관리한다.
<ul>
    <li>신고 목록: 신고 사유 및 횟수 보기, 검색, 정렬</li>
    <li>댓글 삭제: 댓글 내역 삭제</li>
    <li>댓글 블라인드: "해당 댓글은 블라인드 처리 되었습니다"로 댓글이 수정됨</li>
    <li>회원 정지: 정지 일수에 따라 일정기간 로그인 불가능</li>
    <li>강제 탈퇴: 회원을 탈퇴시킨다.</li>
</ul>
</details>
<details>
<summary>정지 회원 관리</summary>
<ul>
    <li>정지 회원 목록: 정지일 보기</li>
    <li>회원 정지 및 해제: 정지일 추가 또는 해제</li>
</ul>
</details>
</div>

<div>
<h4>⭐식재료 관리</h4>
<details>
<summary>⭐ 식재료 목록</summary>
식재료 정보 보기, 검색, 정렬
</details>
<details>
<summary>⭐ 식재료 추가</summary>
식재료명 중복 체크하여 식재료 추가
</details>
<details>
<summary>⭐ 식재료 수정</summary>
아이콘 이미지, 카테고리, 식재료명(중복 체크, 기존 식재료명으로 유지 가능), 소비기한 등 수정
</details>
<details>
<summary>⭐ 식재료 삭제</summary>
사용자 냉장고에 추가되어있는 식재료는 삭제 불가능
</details>
</div>

<div>
<h4>상품 관리</h4>
<details>
<summary>상품 목록</summary>
상품 정보 보기, 검색, 정렬
</details>
<details>
<summary>상품 추가</summary>
상품 정보 작성하여 추가
</details>
<details>
<summary>상품 수정</summary>
아이콘 이미지, 상품명, 설명, 재고량 등 수정
</details>
<details>
<summary>상품 삭제</summary>
삭제 버튼을 클릭하여 상품 삭제
</details>
</div>

<div>
<h4>주문</h4>
<details>
<summary>주문 목록</summary>
<ul>
    <li>모든 회원의 주문 리스트, 정렬, 검색</li>
    <li>주문 번호 클릭 시 주문 상세 정보 확인 가능</li>
</ul>
</details>
<details>
<summary>환불 목록</summary>
<ul>
    <li>모든 회원의 환불 요청 리스트, 정렬, 검색</li>
    <li>주문 번호 클릭 시 주문 상세 정보 확인 가능</li>
    <li>환불 승인 클릭 시 환불 처리됨</li>
</ul>
</details>
</div>

<div>
<h4>사용자 게시글</h4>
<details>
<summary>게시글 목록</summary>
<ul>
    <li>모든 사용자의 게시글 목록 확인, 정렬 및 검색 가능</li>
    <li>글 제목 클릭 시 해당 글 상세 페이지로 이동</li>
</ul>
</details>
<details>
<summary>게시글 수정 및 삭제</summary>
모든 사용자의 게시글을 수정 및 삭제할 수 있다.
</details>
</div>

<br>

## 4. 회고
본격적인 개발에 들어가기 전 데이터베이스 구축에 많은 시간을 들였음에도 불구하고 나를 포함한 모든 팀원들이 개발 과정에서 DB를 수정하는 경우가 잦았다. 모든 기능들이 유기적으로 연결되어 있기 때문에 이 부분에서 가장 많은 시간이 소요되었다. 이에 협업 프로젝트에 있어서 활발한 소통과 데이터베이스 구축의  중요성을 몸소 느끼게 되었다. 지난 프로젝트에서 부족함을 느낀 AJAX는 나의 담당 기능은 아니지만 다른 팀원의 댓글, 대댓글 기능 코드 리뷰를 하면서 조금 더 이해하게 되었다.
