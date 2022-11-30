# 블로그 주소
Link: <https://chani0125.github.io/>

<hr/>

# 블로그 제작 과정

## 1. 블로그 생성

### 1. Fork

<img src="https://user-images.githubusercontent.com/71829572/204723308-902d81aa-d8c3-4be4-891f-d615af7b32ba.png"/>

- Chripy 테마의 원격 저장소를 나의 원격 저장소로 fork 한다.
- 해당 저장소의 이름을 Chani0125.github.io 로 변경한다.
- git clone을 통해 로컬 저장소에서 작업을 계속한다.

``` bash
git clone <원격 저장소 주소>
```

### 2. 블로그 초기 설정

#### _config.yml` 파일에서 세부사항을 작성한다.

- `lang': `ko-KR`로 언어 설정
- `timezone`: `Asia/Seoul`로 설정
- `title`: 제목
- `tagline`: 타이틀 밑에 내용
- `url`: 블로그 주소
- `avatar`: 아바타로 사용할 사진 위치
- `theme` : dark와 light 중 선택

#### 추가 작업

###### `.github\workflows`에 있는 `pages-deploy.yml.hook`파일을 수정
1. `braches`를 소스가 위치할 브랜치 이름으로 수정한다. (`main`으로 함)
2. `ruby` 버전이 자신의 것과 맞는 버전으로 수정한다. (`3.1`로 했음)
3. 파일의 이름에서 `.hook`확장자를 제거한다.

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
```
localhost:4000
```

