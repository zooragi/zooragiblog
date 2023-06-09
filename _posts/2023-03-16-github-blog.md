---
title:  "GitHub Blog 1" 
author_profile: true
categories: githubblog

toc: true
toc_sticky: true
classes: wide 
---

## Git Pages 만들어 보자

> **준비물**
> 
> 1. typora - 블로그 관리 하기 편리함
> 2. Git Desktop - 블로그 관리 하기 편리함

- 파일 네이밍 - 2022-11-16-custom Name.md

### 이미지 업로드 방법

1. typora --> 파일 --> 환경설정 --> 이미지 --> 사용자 정의 image folder --> 경로 : ../images/${filename}

2. 밑에 그림 처럼 typora 에서 이미지를 드래그 하면 자동으로 images 폴더가 생기고 거기안에 이미지가 들어감
   
   <img src="../images/2022-11-16-first-posting/웃음.PNG" alt="웃음" style="zoom:50%;" />

### 업데이트 내역 실시간 확인

- 기존에는 page수정하고 git Desktop으로 반영시키고 업데이트 될때까지 기다려야 했다. 
1. https://mmistakes.github.io/minimal-mistakes/docs/installation/ 접속한다.

2. Official Documentation 링크 클릭

3. Ruby다운로드 (brew install ruby)

4. Jekyll 다운로드 (gem install jekyll) 에러나면 sudo 또는 gem install rouge -v 3.30.0 먼저 다운

5. Bundler 다운로드 (gem install bundler)

6. 나의 git 폴더 위치에서 bundle install

7. 로컬에서 서버를 실행해 줄건데, bundle exec Jekyll serve 여기서 에러남 
   
   - Crash 충돌 문제라는데 우선 brew update, brew upgrade, brew cleanup -s, gem update해봄
   - 안됨.... 흠 우선 M1이랑 Ruby랑 뭔가 안맞는듯??
   - 루비 부터 검색해서 다시 설치
     1. brew install rbenv ruby-build
     2. rbenv install -l --> 버전 확인
     3. rbenv install 2.7.6
     4. rbenv versions --> 버전 확인, 기본적으로 system버전을 가리키고있음
     5. rbenv global 2.7.5 --> 버전 변경
     6. rbenv rehash
     7. gem install bundler --> permission 에러남
     8. 권한 설정해줘야됨
        - open ~/.zshrc
        - export PATH={$Home}/.rbenv/bin:$PATH && \ eval "$(rbenv init -)"
        - source ~/.zshrc
     9. gem install jekyll
     10. bundler install
     11. bundle exec jekyll serve
         - 하..... 된다!!!!!!!!!!!!
         - https://danaing.github.io/etc/2022/03/14/M1-mac-jekyll-setting.html 감사합니다.

8. localhost:4000으로 접속하면 실시간 변경 확인 가능



![](../images/2022-11-16-first-posting/2023-03-07-15-19-11-image.png)
