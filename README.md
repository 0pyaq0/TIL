# TIL (Today I Learned ☺️📝)
<br><br>
![제목 없음](https://user-images.githubusercontent.com/72568433/150020906-675ae821-d3d2-4e18-8153-3a0a7b4348d7.png)
<br><br><br>

      공부한 전공 내용을 기록하는 공간입니다.
      
<br><br><br>


## Rule
<br><br>

### 커밋메세지

> 다음은 커밋메세지의 형식입니다.
``` 

  CommitType :: (#issue number) Subject
  
```
<br>

### Commit Type

 > 다음은 커밋타입 형식입니다.

|CommitType|설명|
|------|----------------------|
|📑 ::|파일 생성 및 구조 변경|
|⚡️ ::|기능 업데이트|
|⚰️ ::|기능 삭제|
|🐛 ::|버그 수정|
|♻️ ::|코드 리펙토링|
|📝 ::|문서 작성 및 수정|
|⚙️ ::|프로젝트 세팅|
|🧪 ::|테스트 코드 추가|
|🚀 ::|새 버전 릴리즈 ( 커밋은 아니지만😏|
|🔀 ::|Merge or PR|

<br>

### Subject

> 커밋메세지 형식의 Subject 부분에 기재

* 50자를 넘기지 않게 명령형으로 작성한다.
* 한국어로 작성한다.
* ```어떻게``` 보단 ```무엇을```, ```왜``` 에 초점을 두고 작성한다.

```bash

"~수정 했다" → "~수정"

"Add~" → "~추가"

```

<br>

### Example

```
🐛 :: [MainPage] 헤더가 안보이는 버그 수정
```
```
🐛 :: (#19)[FeedServiceImpl] 피드 버그 로직 수정
```
```
🚀 :: v1.0.0
```
```
📝 :: README 파일 수정
```

<br><br>

* [참고](https://github.com/team-xquare/README.md/blob/main/README.md)
