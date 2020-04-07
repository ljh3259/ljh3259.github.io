---
layout: post
title:  "pro git 책 읽으면서 중요하다고 생각하는 것들"
date:   2020-01-12 12:07:00 +0900
categories: book
---



## 리모트 브랜치
- `git ls-remote [remote (origin or upstream...)]` 명령으로 모든 리모트 Refs를 조회할 수 있다.
  - git remote -v 또는 -vv로 추적하고 있는 remote 들을 확인한다.
  - ```
     jihoonlee@jihoonui-iMac  ~/blog/ljh3259.github.io   master  git remote -vv
    origin  https://github.com/ljh3259/ljh3259.github.io.git (fetch)
    origin  https://github.com/ljh3259/ljh3259.github.io.git (push)
    ```
  -  ls-remote 로 확인한다.
  - ```
     jihoonlee@jihoonui-iMac  ~/blog/ljh3259.github.io   master  git ls-remote origin
    771a4a2464151265924988a7a07e8d14dda594d9        HEAD
    771a4a2464151265924988a7a07e8d14dda594d9        refs/heads/master
    ```
- 리모트 브랜치의 이름은 (remote)/(branch) 형식으로 되어있다.
- 멋대로 조종할 수 없다.

### git fetch
- P82
- fetch 명령으로 리모트 트래킹 브랜치를 내려 받는다고 해서 **로컬 저장소에 수정할 수 있는 브랜치가 새로 생기는 것이 아니다**
- 그저 수정 못하는 origin/serverfix 브랜치 포인터가 생기는것이다.
- git merge origin/serverfix 
  - 새로 받은 브랜치의 내용을 Merge
- git checkout -b serverfix origin/serverfix
  - Merge 하지 않고 리모트 트래킹 브랜치에서 시작하는 브랜치를 만든다. 
  
  
  
  
  
  
  
  
  
  
  
  
  
  