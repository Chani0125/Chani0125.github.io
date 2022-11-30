# 블로그 주소
Link: <https://chani0125.github.io/>

<hr/>

# 블로그 제작 과정

## 1. Git 학습
아래 링크에 포스트 해놓았다.
Link: <https://chani0125.github.io/posts/Git-Github/>

## 2. 블로그 생성

### 1. Fork

<img src="https://user-images.githubusercontent.com/71829572/204723308-902d81aa-d8c3-4be4-891f-d615af7b32ba.png"/>

- Chripy 테마의 원격 저장소를 나의 원격 저장소로 fork 했다.
- 해당 저장소의 이름을 Chani0125.github.io 로 변경했다.
- git clone을 통해 로컬 저장소에서 작업을 계속했다.

``` bash
git clone <원격 저장소 주소>
```

### 2. 블로그 초기 설정

#### _config.yml` 파일에서 세부사항을 작성했다.

- `lang`: `ko-KR`로 언어 설정
- `timezone`: `Asia/Seoul`로 설정
- `title`: 제목
- `tagline`: 타이틀 밑에 내용
- `url`: 블로그 주소
- `avatar`: 아바타로 사용할 사진 위치
- `theme` : dark와 light 중 선택

#### 추가 작업

- `.github\workflows`에 있는 `pages-deploy.yml.hook`파일을 수정
1. `braches`를 소스가 위치할 브랜치 이름으로 수정했다. (`main`으로 함)
2. `ruby` 버전이 자신의 것과 맞는 버전으로 수정했다. (`3.1`로 했음)
3. 파일의 이름에서 `.hook`확장자를 제거했다.

### 3. Jekyll

- Jekyll 설치 확인
``` bash
jekyll -v
```

- Jekyll 실행하기
``` bash
bundle exec jekyll serve
```

- Jekyll 실행 후 다음 주소에 접속
해당 주소에 접속하여 블로그가 제대로 설정되었는지 확인했다.
``` bash
localhost:4000
```

- 소스 올리기
아래 git 명령을 사용하여 수정된 내용을 모두 github에 올렸다.
``` bash
git add -A
git commit -m "commit message"
git push origin main
```

- github Actions 탭
push를 하게되면 github은 자동으로 블로그 페이지를 만들어 준다.
<img src="https://user-images.githubusercontent.com/71829572/204814473-99163e6f-e0ba-42d0-ac92-8d094ffb2cd3.png"/>
위의 사진처럼 정상적으로 종료가 되었다.

- 들어가 보기
<img src="https://user-images.githubusercontent.com/71829572/204814940-67957c06-fd72-46cf-b6db-8871442664bf.png"/>
나의 깃허브 블로그 사이트에 들어가서 잘 나오는지 확인했다.

## 3. 블로그 꾸미기

### 1. 댓글 기능 추가

Disqus 사이트를 이용해서 댓글 기능을 추가하였다.

- Disqus 가입
웹페이지 이름을 정하고, Website URL에 블로그 주소를 입력했다.
<img src="https://user-images.githubusercontent.com/71829572/204822926-bff5db7b-676d-4a66-9e55-33102a72e6fa.png"/>

- Disqus 세팅
Disqus 사이트 정보에 있는 `Shortname`을 `_config.yml`에 사용했다.
``` yml
comments:
  active: disqus
  disqus:
    shortname: mincho-park-blog
```

