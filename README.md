# 블로그 주소
Link: <https://chani0125.github.io/>

<hr/>

# 블로그 제작 과정

## 1. Make Blog

### 1. Git

<img src="https://user-images.githubusercontent.com/71829572/204723308-902d81aa-d8c3-4be4-891f-d615af7b32ba.png"/>

- Chripy 테마의 원격 저장소를 나의 원격 저장소로 fork 한다.
- 해당 저장소의 이름을 Chani0125.github.io 로 변경한다.
- git clone을 통해 로컬 저장소에서 작업을 계속한다.

### 2. Jekyll

- Jekyll 설치 확인
``` bash
jekyll -v
```

- 현재 디렉토리에 Jekyll 설치
``` bash
jekyll new . --force
```

- Jekyll 실행하기
``` bash
bundle exec jekyll serve
```

- Jekyll 실행 후 다음 주소에 접속
```
localhost:4000
```

