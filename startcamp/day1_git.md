# CLI

## 절대경로

- 절대경로 / 상대경로

## Command

- cd, date, ls, touch, mkdir
- ~ : 홈디렉토리를 의미 (c/사용자/)
- 가장앞에 / : root디렉토리
- cd : change directory (cd .. : 이전 directory)
- ls : list
- mkdir : 폴더생성 / make directory
- touch : 파일생성

# git (분산 버전 관리 시스템 DVCS)

- git은 버전을 관리해주는 시스템이고 github는 git파일을 저장 할 수 있도록 서비스를 제공해주는 공간이다.
- git이 버전을 관리할 때 차이점만 추가적으로 저장하는 방식이다

## git 명령어

- git init : .git이라는 폴더가 생성됨 / .git폴더가 존재하는 폴더는 git으로 관리한다를 의미 / git을 위한 공간이생성된다
- 3가지 공간으로 나눌 수 있다. Working directory, Staging area, Commit
- git add : Working directory -> Staging area 명령어
- git status : 상태확인
- git commit : Staging area -> Commit 명령어 / 히스토리(버전)를 생성하는 행위 / 내컴퓨터에 저장됨
- git push :
- 스냅샷 : 파일들의 차이점을 뽑아서 그 내용을 만든다라는 것? (좀더 공부필요)



- git remote add 이름 'git주소' -> git remote add origin https://github.com/hhhhhhdong/testpage
-  ㄴ origin이라는 이름으로 해당주소의 레파지토리를 등록한다
- git branch -M main : main 브런치로 바꾸겠다
- git push -u origin main
- git restore --staged <file> : Staging area -> Working directiory
- .gitignore에서 무시목록은 Untracked 상태에서 적용해야한다

