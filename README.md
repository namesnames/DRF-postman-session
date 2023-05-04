# POSTMAN
![](https://velog.velcdn.com/images/97gkswn/post/da688b03-e636-44cd-b6d9-dbebe7b2fa6a/image.png)

# POSTMAN이란?
- API를 개발, 테스트, 문서화 및 공유하는 데 사용
- HTTP 요청을 만들고 보내고, 응답을 확인
- 다른 API 개발자나 팀원들과 공유도 가능

# 이걸 왜 쓸까?

우리가 만든 기능들을 바로바로 프론트가 만든 페이지에서 확인하면 좋지만 front-end 와 back-end의 작업속도는 다르다. 따라서 이러한 POSTMAN같은 tool들을 이용해서 우리가 만든 API들이 제대로 작동되는지 테스트해 볼 필요가 있다.

ex) 이 주소에 GET을 보냈을 때 응답이 어떻게 오는지
<br>
<br>

# 예시
![](https://velog.velcdn.com/images/97gkswn/post/737d6cdc-f52c-4cb2-a8fc-f93d32f62605/image.png)
http://localhost:44311/api/v1/reg-accountinfo 라는 주소에

-------------------------------------------------------------------------------------------------------------------
```
{
"UserID":"gdhong",
"UserPWD":"1234",
"UserName":"홍길동",
"CNIC":"01022223333",
"EmailAddr":"gdhong@gamil.com",
"UseState":0"
}
```
라는 데이터를 POST요청으로 보내는 상황이다.
(일반적으로 Body->raw->Json으로 설정해서 보냄)

지금 아래에 보면 `Status: 200ok` 라는 `정상적으로 됐다` 라는 사인과 우리가 보낸 데이터에 UserNo만 추가돼서 return값이 온 상황이다. ( 그냥 개발자가 return 값을 그렇게 넘겨주도록 짠거임)

이런식으로 테스트 해볼 수 있습니다!

<br>
<br>

# 설치
https://www.postman.com 로 이동해서 

>![](https://velog.velcdn.com/images/97gkswn/post/58327789-ecb2-4171-b2b4-cb44f9a8236a/image.png)
우측 상단에 회원가입 (sign up) 클릭해서 회원가입 진행

<br>
<br>

>![](https://velog.velcdn.com/images/97gkswn/post/e72ba233-3ad5-42fd-8067-7fe28ed00cd0/image.png)
회원가입 했으면 로그인하고 맨 아래로 가서 `Download the app` 클릭

<br>
<br>

>![](https://velog.velcdn.com/images/97gkswn/post/8bfcdbb1-3bf2-4b6e-9758-ebb57f882a38/image.png)
요거 클릭해서 exe파일 다운하세용

<br>
<br>

>![](https://velog.velcdn.com/images/97gkswn/post/bcd456a0-4a59-47f0-a06f-b08ae46fd8da/image.png)
실행시키고 Workspaces-> My Workspace

<br>
<br>

![](https://velog.velcdn.com/images/97gkswn/post/5d277e5b-8b5e-4b67-935f-bac873edf07b/image.png)
`+`버튼 클릭

<br>
<br>

>![](https://velog.velcdn.com/images/97gkswn/post/3bf099cb-c713-4351-b007-efc67fc0c958/image.png)
그리고 위와 같이 Body->raw->Json으로 각각 선택해주면 준비 완료
