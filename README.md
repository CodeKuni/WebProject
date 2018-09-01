카카오톡 자동응답 API 버튼형 웹으로 구현하기
=============


개발동기
---------
2018.09.01 오산시 진로진학박람회에서 전공체험으로 무엇을 하면 좋을지 생각해보았다.
그러던 도중 체험을 하는 학생들에게는 개발자라는 말 보다는 운영자라는 표현이 훨씬 친숙할거라는 생각이 들어,
내가 해봤던 여러가지들 중에서도 이론 보다는 재미를 붙일 수 있고, 호기심을 갖을 수 있는것으로 직접 자기가 만들었다는 느낌을 받을 수 있기 위해서 카카오톡 플러스친구 자동응답 API 사용해 간단히 연동해서 비전공자도 시도해 볼 수 있는 restfull api 연동 웹을 개발하였다.

사용된 기술 및 라이브러리
-----------------
JSP
MD Bootstrap
javascript 
jquery
jquery-ui
json
kakao plus friends auto reply api

동작방식
-------------
기본 Restfull API 사용법과 동일하다.
파트너 서버에서 웹에서 메뉴생성 명령으로 메뉴이름, 내용을 입력하면 카카오톡 플러스친구에 버튼이 만들어지고 버튼을 누르면 그 내용을 볼 수 있다.

아쉬운 점
-----
메뉴를 만든 내용을 DB에 저장하는게 조금 더 깔끔하게 제작이 가능했을 것 같다.
DB사용 경험이 많지 않고, 많이 잊어버린 상태였을 뿐더러 급하게 생각해서 만들었던거라 시간이 촉박해서 최소한으로 이용했다.

메뉴에 대한 정보는 서버 디렉토리 내 새로운 디렉토리를 만들어 그곳에 파일 형태로 저장을 했고,
만들어지고, 수정된 내용은 바로바로 업데이트 되어 파일에 json 배열 형태로 저장해서 keyboard API를 사용하면 불러올 수 있게하였다.

수정해야할 부분
----------------------------------
메뉴 수정 기능을 너무 허접하게 만들었다.
수정 기능을 찾기가 많이 귀찮아서 그냥 수정을 누르면 삭제하고, 다시 그 내용을 쿼리스트링으로 받아서 그 파일을 다시 생성하도록 하였다.
