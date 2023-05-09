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
>![](https://velog.velcdn.com/images/97gkswn/post/737d6cdc-f52c-4cb2-a8fc-f93d32f62605/image.png)
--------------------------------------------------------------------------------------------------------------------------------

지금 위의 사진을 보면 http://localhost:44311/api/v1/reg-accountinfo 라는 주소에

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

>![](https://velog.velcdn.com/images/97gkswn/post/5d277e5b-8b5e-4b67-935f-bac873edf07b/image.png)
`+`버튼 클릭

<br>
<br>

>![](https://velog.velcdn.com/images/97gkswn/post/3bf099cb-c713-4351-b007-efc67fc0c958/image.png)
그리고 위와 같이 Body->raw->Json으로 각각 선택해주면 준비 완료


<br>
<br>
<br>
<br>



# DRF과제 
## 학습 목표 & 진행방식

- DRF(Django Rest Framework) 및 Serializer를 이해한다.
- 앞서 만든 MBTI 커뮤니티에서 기능 추가 
- 팀 구성: 2인 1팀
- 발표: 5/17 수요일 세션에 발표. 발표 내용은 제작한 웹사이트에 대해 간단히 3~5분정도로 간략 소개하는 방식
- 제출방식 : 각 팀별로 작업 과정 및 결과물이 담긴 GitHub Repository 를 생성후 작업 진행 및 제출


---

## 실습 과제


### 구현해야 하는 기능

1. '카테고리별' 게시글 작성 
    - 각자 원하는 만큼의 카테고리를 (최소 3개 이상) 정해서 글을 작성할 때 카테고리도 입력해서 작성할 수 있도록 수정해주세요!

2. '카테고리별' 게시글 조회
    - 실제 서비스라고 가정하면 다양한 사람들이 글을 작성해서 카테고리 별로 여러 개의 글들이 있을겁니다!
    - 카테고리 별로 글을 모아볼 수 있도록 카테고리 별 글 조회 기능을 구현해주세요!
    
3. '내'가 작성한 게시글 조회
    - 내가 작성한 글들만 조회가 가능하도록 기능을 추가해주세요!
    
4. '내'가 작성한 댓글만 조회
    - 내가 작성한 댓글들만 조회가 가능하도록 기능을 추가해주세요!
    
5. '특정 유저'가 작성한 게시글 조회
    - '내'가 아닌 '특정 유저'가 작성한 게시글만 조회 가능하도록 기능을 추가해주세요!
    - 예를 들면 작성자 'A'가 작성한 글만 조회하는 기능입니다!    

6. 게시글 좋아요 기능 (BONUS // 필수가 아닙니다! 하고싶은 분들만 하시면 됩니다!)
    - 게시글 좋아요 버튼을 누르면 좋아요가 1씩 늘어나게 해주세요!
    - 한 사람당 좋아요는 한 번씩만 누를 수 있어야합니다!

---

### 유의사항

- 통합 세션에서 배웠던 HTML과 CSS를 활용해 프론트도 같이 개발하되, **프론트는 간단하게만** 구현합니다. 
포커스는 백엔드 구현 🎯
- 협업 시 GitHub를 활용해주세요.
- 이때, **커밋 메시지**에 본인의 작업 내용이 명시되도록 작성해주세요.
    - 커밋 메시지를 작성하는 일반적인 규칙에 대해서는 ‘커밋 메시지 작성 규칙' 등을 구글링해 참고해주세요.

---

# 제출물 안내


아래의 안내에 따라, 과제를 제출해주세요!

- 작업 과정 및 최종 결과물이 담긴 **GitHub Repository 링크**를 제출합니다.
    - Repository는 멋쟁이사자처럼 10기 Organization 내부에 만들어주세요.
    - Repository 이름 형식 : be-django-trainingDRF-(팀명)


- **README**에는 다음과 같은 내용이 포함되어야 합니다.
    - API 명세서
    - 본인이 설계한 DB를 도식화하여 설명
        - 테이블, 테이블 간 관계, 각 필드의 데이터 타입과 제약 조건 등을 포함
        - 자유 형식 (참고 : ERD)
    - 간단한 개인별 회고 1~2줄
        - 들어가면 좋을 내용 : 프로젝트를 진행하며 발생한 어려움과 해결 방법에 대해 기록해두면 좋습니다.
- 프로젝트 코드, README 등 최종 결과물은 `main`(또는 `master`) 브랜치에 올려주세요.
 

---


