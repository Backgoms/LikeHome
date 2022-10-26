# LikeHome (모바일 웹)
중앙 1차 프로젝트
================

#### 1. 프로젝트 명 : LikeHome

#### 2. 프로젝트 기간 : 2022.07.05 ~ 2022.08.19(1개월 15일)

#### 3. 작업 인원 : 5 명

#### 4. 소속 : 중앙정보처리기술개발원

#### 5. 개발환경
   - Eclipes(Spring Framework) 
   - Oracle11g 
   - Apach Tomcat9
   - Java SE Development kit 11

#### 6. 프로젝트 설명 : 
    판매자와 구매자가 함께 상호작용을 하여 가구 및 인테리어 소품을 판매하는 쇼핑몰입니다.
    상품을 구매한 구매자는 커뮤니티에 구매한 상품을 이용한 인테리어를 게시하고 상품을 태그하여 다른 고객이 상품 태그를 타고 
    구매했을 경우 게시자에게 리워드가 제공되어져 판매자와 구매자가 상생하는 오픈마켓 플랫폼을 구현하였습니다.

#### 7. 담당 업무 : 
 커뮤니티(Post) 페이지 구현 및 기술 지원, 포트폴리오 기획을 담당하였습니다.
   * 해당 고객이 구매한 상품만 출력 및 검색/ 태그 기능 구현
   * 해쉬태그 기능 구현

#### 8. 담당 구현 페이지 :
 - 커뮤니티(Post)
      * 포스트 리스트
      * 포스트 상세
      * 포스트 수정
      * 포스트 등록
 - 유저홈
      * 홈
      * 사진
      * 팔로워
      * 팔로잉 
  - 공통
      * 메인페이지(커뮤니티 순위)

#### 9. 어려웠던 점
    포스트 등록을 구현할 때 해당 데이터를 Controller로 보내기에 어려움을 겪었습니다. 하나의 POST는 여러 개의 SUBPOST로 이루어져 있으며
    하나의 SUBPOST에는 사진, 상품 태그, 해시태그, 설명 등의 DATA가 있고 그 중 사진을 제외한 DATA는 필수 데이터가 아닌 구조로 되어있습니다.
    초기에 FORM태그를 사용하여 해당 DATA를 모두 배열로 보내서 처리하려고 했지만 비어있는 DATA로 인해 해당 SUBPOST의 데이터인지 구분을 할 수 없었습니다.
    위 문제로 인하여 AJAX를 통해 순차적으로 DATA를 넘기는 방식으로 변경하였습니다. 이 방법으로 변경하면서 input태그 안에 있는 사진DATA를 넘길 수 없는
    문제가 다시 발생하였습니다. 그 후 구글링을 통해 해결 방법을 찾아다가 FORMDATA라는 객체를 사용하여 사진과 DATA를 함께 보낼 수 있는 것을 확인하여
    시도하여 성공적으로 저장되었습니다. 하지만 작업을 진행하면서 저장된 DATA가 순차적으로 저장되지 않은 문제를 발견하게 되었습니다.
    이 문제는 초기에 원인조차 예상할 수 없었습니다. 그 후 프로젝트를 진행하면서 다른 팀의 팀원과 대화하다가 AJAX가 비동기 형식이며 동기로 변경이
    가능하다는 것을 알게 되었습니다. 그 이야기를 듣고 동기와 비동기의 차이를 공부하고 저장의 기능을 하는 AJAX를 동기 형식으로 바꿔 테스트하였더니
    정상적으로 작동하였습니다.
    작업을 하면서 막히는 부분을 찾아서 공부할 때마다 새로운 것을 알게 되며 많은 것을 알아야 더 효율적으로 작업을 할 수 있다는 것을 느꼈습니다.
    또한, 혼자서 해결 방법을 찾는 것 말고 동료에게 조언을 요청하는 것도 많은 도움이 된다는 것을 느꼈습니다.

#### 11. AWS배포 주소
   http://15.164.103.90:8080/LikeHome/main/mainPage
