Heroku 배포

IaaS / PaaS
 - IaaS(Infrastructure as a Service)
    - AWS EC2

 - PaaS(Platform as as Service)
    - Heroku, AWS EB
    

# 배포 전 준비사항
    1. github 배포하려는 소스 올리기 (new repo)
    2. decouple 설치 : pip install python-decouple
    3. setting.py - secret_key, debug -> .env파일 만들고 이동 (SECRET_KEY=p5h6#olp6*)ijzlyry9fuc7sj565^@7lw9+-mdc0_#f&(89t_+
DEBUG=True)
    4. 헤로쿠 설치:pip install django-heroku
    5. settings.py 맨 밑에 : 
        import django_heroku
        django_heroku.settings(locals())
    ---------------- 준비 끝 -------------------------

# 배포를 위한 설정
    1. Procfile 생성 : (띄어쓰기 조심)
        web: gunicorn config.wsgi --log-file -
    2. gunicorn 설치 장고와 서버간의 데이터 중개 역할 (uwsgi 대신 heroku 추천) : $ pip install gunicorn
    3. runtime.txt 생성 - $ python --version  버전 확인 후 입력
    4. $ pip freeze > requirements.txt


# 배포
    1. 헤로쿠 가입
    







