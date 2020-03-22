# parkkisun
Parkkisun's Personal Website


### 1. 클론받기

github를 통해 parkkisun repository를 클론 받습니다. sourcetree를 이용하거나, 터미널에서 직접 할 수 있습니다.

### 2. 파이썬 가상환경 만들기

터미널을 열고, parkkisun repository로 이동합니다. 여기에 파이썬 가상환경을 만들어야합니다. 
```
~parkkisun % python3 -m venv myvenv
```

### 3. 파이썬 가상환경 실행하기

parkkisun repository를 기준으로 다음 명령어를 입력합니다. 
```
~parkkisun % source myvenv/bin/activate
(myvenv) ~parkkisun % 
```

### 4. pip 설정

pip는 이미 설치되어 있을 가능성이 높습니다. pip가 설치되어 있지 않다면 별도로 설치하고, 버전을 업데이트합니다.
```
(myvenv) ~parkkisun % python3 -m pip install --upgrade pip
```

### 5. djando 설치

pip를 사용하여 django를 설치합니다.
```
(myvenv) ~parkkisun % pip install django~=2.0.0
Collecting Django~=2.0.6
  Downloading Django-2.0.6-py3-none-any.whl (7.1MB)
Installing collected packages: Django
Successfully installed Django-2.0.6
```

### 6. markdown 설치

이 블로그는 markdown을 사용하기 때문에 markdown 모듈을 설치해야합니다. 
```
(myvenv) ~parkkisun % pip install markdown
Collecting markdown
  Downloading Markdown-3.2.1-py2.py3-none-any.whl (88 kB)
     |████████████████████████████████| 88 kB 260 kB/s 
Requirement already satisfied: setuptools>=36 in ./myvenv/lib/python3.8/site-packages (from markdown) (41.2.0)
Installing collected packages: markdown
Successfully installed markdown-3.2.1
```

### 7. 데이터베이스 생성

클론 받은 코드에 데이터베이스 관련 코드는 포함되어 있을거지만, migrate를 해야합니다. 
```
(myvenv) ~parkkisun % python manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, blog, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying blog.0001_initial... OK
  Applying sessions.0001_initial... OK
```


### 8. 서버 실행

프로젝트 디렉토리(djangogirls)에 `manage.py`파일이 있어야 합니다. 콘솔에서는 python manage.py runserver명령을 실행해, 웹 서버를 바로 시작할 수 있습니다.
```
(myvenv) ~parkkisun % python manage.py runserver
Performing system checks...

System check identified no issues (0 silenced).
March 09, 2020 - 18:57:34
Django version 2.0.13, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```


### 9. 로컬 브라우저에서 확인

서버를 실행하면 나오는 url `http://127.0.0.1:8000/` 을 브라우저의 주소창에 입력합니다. 정상적으로 블로그가 표시되면 성공적으로 설치가 완료된겁니다. 



