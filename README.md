## 설정 파일
### Procfile
- Procfile은 실행시킬 파일을 설정해준다. (확장자는 필요없음)
```bash
web: gunicorn main:app
```

### requirements.txt
- requirements 파일은 파이썬에서 필요한 package버전을 적어둔다.
```bash
Flask==2.0.2
gunicorn==20.1.0
```

### runtime.txt
- runtime 파일은 파이썬 버전을 설정한다.
```bash
python-3.9.1
```
----
### 헤로쿠에서 배포하는 법
- https://www.heroku.com/ 에서 헤로쿠 사이트에 회원가입후 사용가능
- `salesforce authenticator` 앱를 앱스토어에서 받아서 헤로쿠 아이디 보안 적용

### 명령어 사용
- `heroku create [프로젝트 이름]` ( 프로젝트 이름은 중복체크가 있어 유니크하게 설정해줘야된다. )
  - ex) `heroku create tono-heroku-test`
- 위 코드 작성후 아래와 같은 과정을 terminal에서 진행한다.
  - `git init`
  - `git add .`
  - `git commit -m "first commit"`
  - `git push heroku master`
- 위와 같이 진행했을 경우 heroku 대시보드에서 프로젝트가 생성된 것을 확인할 수 있다.

### 헤로쿠 실행
- `heroku ps:scale web=1`
  - commend를 terminal에서 입력하여 app을 열어준다.
- `heroku ps`
  - commend를 통해 웹 사이트 상태를 확인
- `heroku open`
  - commend를 통해 웹사이트를 열어준다.
- 코드 수정후 `heroku open`만 사용해도 바로 적용된다.
