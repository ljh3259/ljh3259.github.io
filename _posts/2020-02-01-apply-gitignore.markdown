---
layout: post
title:  ".gitignore 설정을 적용하는 방법"
date:   2020-02-01 15:07:00 +0900
categories: git
---

# .gitignore 설정을 적용하는 방법

### 1. .gitignore 파일을 수정한다
```vim
  1 .idea/
  2 .gradle/
  3 build/
```
### 2. git 명령어 입력
- git add .gitignore 
    - 수정한 .gitignore 를 Staged 상태로 
- git rm -r --cached .
    - -r 
        - Allow recursive removal when a leading directory name is given.
        - 디렉토리 이름이 주어지면 재귀 제거를 허용한다는데 음..
    - --cached
        - Use this option to unstage and remove paths only from the index. Working tree files, whether modified or not, will be left alone.
        - Staging Area 에서만 제거하고 워킹 디렉토리에 있는 파일은 지우지 않고 남겨둔다.
        - 즉 더이상 추적하지 않는다.
- git add .
    - 무시하지 않을 파일을 Tracked 한다.
- git commit ".gitignore fix"
    - 에디터를 사용하지 않고 간단하게 commit
    
### 3. 참고.    
[Untrack files already added to git repository based on .gitignore](http://www.codeblocq.com/2016/01/Untrack-files-already-added-to-git-repository-based-on-gitignore/).
