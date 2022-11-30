---
title: "Git, Github 소개"
author: Mincho_Park
date: 2022-11-30 23:14:00 +0900
categories: [Blog, Build]
tags: [git, github]
comments: true
---

# Git

- 오픈 소스 버전 관리 시스템
- 로컬에서 버전 관리
- 소프트웨어 개발 및 소스 코드 관리에 사용

<hr/>

# Github

- Git Repository를 위한 웹 기반 호스팅 서비스
- 클라우드 서버를 사용해서 로컬에서 버전 관리한 소스코드를 업로드하여 공유 가능
- 분산 버전 제어, 액세스 제어, 소스 코드 관리,  버그 추적, 기능 요청 및 작업 관리를 제공

<hr/>

# 명령어

## 저장소
- 로컬 저장소 생성
현재 작업중인 디렉토리를 git 저장소로 지정
```bash
git init
```

- 원격 서버의 저장소 복제
```bash
git clone <원격 저장소 주소>
```

## 변경사항 반영

- 현재 Git 상태 확인
```bash
git status
```

- <filename>을 생성하고 이를 Commit에 반영하고 싶은 경우
```bash
git add <filename>
```

- 변경사항이 반영된 new commit 생성
```bash
git commit -m "commit message" 
```

- commit 기록 확인하기
```bash
git log 
```

- 원격 저장소로 보내기
```bash
git push 
```

- 원격 저장소에서 가져오기
```bash
git pull 
```

## Branch

- Branch 생성
git branch <branch_name>을 통해 branch 생성
```bash
git branch <branch_name>
```

- Branch 전황
현재 작업중인 branch를 전황
```bash
git checkout <branch_name>
```

- Branch 병함
현재 작업중인 branch를 원하는 branch에 병합
```bash
git merge <branch_name>
```

- Branch 삭제
```bash
git branch -d <branch_name>
```
 
