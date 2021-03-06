# 2021 Farm 경진대회
### URL_FARM (싱가포르 팀)


## 1. 팀 구성

본 경진대회에 참여하는 싱가포르 팀의 팀원과 팀원의 역할은 다음과 같다. (가나다 순으로 나열)

- [김명준](https://github.com/audwns227) (개발자)
- [김중원](https://github.com/jw0293) (개발자)
- [이태검](https://github.com/LeeTaeGeom) (개발자, 팀장)
- [이형석](https://github.com/lhs961021) (개발자)
- [정재우](https://github.com/Jung-jaewoo) (개발자)

### 1.1. 참여 과제

주제: 자유주제 (지난 스터디/프로젝트 파생 또는 신규 프로젝트)<br>
- 여러 사이트의 정보를 활용할 때 url의 정보가 많으면 한눈에 보기 힘들고 각 정보의 핵심을 파악하는것에 어려움을 느낄 수 있다.<br>
- 이전에 참고한 url을 다시 찾아볼 때 url만 보면 어떤 내용에 해당하는 것인지 모르고,<br> 
저장해 둔 url이 많다면 찾고자 하는 url을 찾는 것이 어렵다.<br>

이러한 것에 대한 문제점을 파악하여 이를 개선하고자 한다. 

### 1.2 과제 주제

URL 요약 정리 공유 사이트

### 1.3 프로젝트 설계

개념설계 :<br> 
   기사분석에 필요한 머신러닝 모델 설계<br> 
      - 가장 정확도가 높은 모델 선정<br> 
      - okt()를 이용해 pos(명사+형용사)로 모델학습<br> 
      
상세설계:<br> 
   서비스를 구체화 시킬 웹서비스 설계<br> 
      - python을 기반으로한 django 사용<br> 
      - 각 웹페이지별 필요한 기술 설계<br> 
      
구현 이론:<br> 
      - lstm, xgboost, randomforest<br> 
      - tfidf, kr-wordrank<br> 
      - gensim summarize<br> 
      - python, django<br> 
      
### 1.4 과제 주요 기능

<메인페이지>
url 검색 기능
- 찾는 기사가 아닐 경우 내가 직접 입력
- 찾은 기사 마이페이지에 저장

내가 저장한 게시물, 작성한 게시물 메인페이지 표시

url 분석(상세페이지)
- 본문 요약
- 워드클라우드 이미지 저장
- 상위 3개의 키워드 추출
- 카테고리 분류
- 원문 url 링크 
- 메모기능

<채팅기능>
채팅방
- 생성, 수정, 삭제 기능
- 닉네임 검색을 통한 참가자 추가
채팅
- 내가 친 채팅 수정, 삭제 기능
- 채팅 친 시간 및 작성자 표시 
- url 공유 기능
- 공유한 url 퍼오기 기능

<마이페이지>
- 뉴스 카테고리별 저장한 글 보기
- 퍼온글 내가쓴글 나눠보기
- 메인페이지에 띄울 기사 선택하기(최대 6개)

## 2. 프로그래밍 언어

본 프로젝트는
[**Python**](https://www.python.org)을 메인 프로그래밍 언어로 사용하고, 
웹 프레임워크로 [**Django**](https://www.djangoproject.com)를 이용한다.

### 2.1. 외부 라이브러리의 사용

본 애플리케이션을 구현하는 과정에서 활용 가능한 외부 라이브러리는 제한없이 사용하는 것을 원칙으로 한다.

### 2.2. Requirements.txt

본 애플리케이션의 소스코드 내에서 활용한 모든 외부 라이브러리는 requirements.txt에 해당 라이브러리 리스트를 저장하여 팀원들에게 공유하여야 한다.
```
$ pip freeze > requirements.txt
```
requirements.txt에 저장된 외부 라이브러리를 다운로드 받는 명령어는 다음과 같다.
```
$ pip install -r requirements.txt
```

### 2.3. Python 가상환경
- [pipenv](https://github.com/pypa/pipenv) :  Python.org에서 공식적으로 권장하는 패키지 설치 툴 및 가상환경 구현용 프로그램

## 3. 서버 실행
```
$ python manage.py runserver 
```
## 4. 환경변수 파일

.gitignore

- Git 관련 환경변수 파일

requirements.txt

- 파이썬 라이브러리 종속성 파일

## 5. 배포

서버 배포는 aws EC2의 Ubuntu Server 18.04 LTS (HVM), SSD Volume Type - 64bit, t2.micro(프리티어) 인스턴스를 이용한다. 

## 6. 자료
[프로젝트 계획서 바로가기](Farm경진대회_수행계획서_팀싱가포르.hwp) <br>
[프로젝트 결과 보고서 요약본 바로가기](2._Farm경진대회_결과보고서_요약본_팀_싱가포르.hwp)  
[프로젝트 결과 보고서 바로가기](1._Farm경진대회_결과보고서_팀_싱가포르.hwp)  
[프로젝트 발표 ppt 바로가기](URLfarm_발표ppt_팀싱가포르.pptx)  
[프로젝트 발표 영상 바로가기](URLfarm_발표영상_팀싱가포르.mp4)  
