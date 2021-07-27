#	git bash

- `start .`  : 현재 폴더를 열기(더블클릭)
- `start <filename>` : 파일열기(더블클릭)
- `mkdir <dirname>` : 폴더 생성하기
- `cd <dirname>` : 폴더 들어가기
- `touch <filename>` : 파일 생성하기
- `rm <filename>` : 파일 완전삭제(휴지통x)
- `rm -r <dirname>` : 



# Git



### 초기화

- Directory(폴더) -------- `git init` --------> Repository(저장소)
- Warnning : repo 안에 repo를 만들지 않는다. (이미 git init한 폴더안에서 또 git init하지 않는다.)



### Repo

- 스냅샷 == 커밋





### Remote Repo

- `$ git remote add <name> <url>` : Remote repo와 Local repo 연결
- `$ git remote remove <name>` : 리모트 삭제
- `$ git remote -v` : 현재 remote 확인
- `$ git push <name> <branch>` : upload commit
- `$ git clone <url>` : remote repo 받아오기
- `$ git push -u origin master` : -u (경로저장)

