## 이 파일은 단순 명령어 리스트 정리 용
---
### GO!
- `git init` : 특정 폴더에 git 저장소(repository)를 만들고 버전 관리
    - **.git** 폴더가 생성됨(숨김 상태)
    - **git bash**에서는 (master)라는 표기를 확인 가능.
    - ![](/image/git%20init.PNG)
    - `만약 관리를 안할거라면 .git 폴더를 삭제하면됨.`

<br>

- `git status` : 파일 변경 상태 확인.
    - 파일의 상태를 알 수 있음.
      - Untracked Files : 버전으로 관리된 적 없는 파일 상태(보통 새롭게 만든 경우)
      - Changes not staged for commit : 기존 파일이 변경이 되었으나 staging area에 올라가지 않은 상태.
        ![](/image/git%20status.PNG)
      
      - Changes to be committed : add에서 commit된 파일 들의 명단을 보여줌
      
         ![](/image/git%20status2.PNG)
      
      - Noting to commit, working tree clean : 변경 사항 없음.
         ![](/image/git%20status3.PNG)
      <br>
      <br>

- `git add 파일명.확장자` : 작업 사항이 저장된 파일명.확장자를 staging area로 추가하기 위해 사용 <br> 
 ***현 디렉토리의 파일만 가능***. 하위 디렉토리의 수정 사항을 넣고 싶으면 하위 디렉토리로 이동 후 해당 파일 add해야함.)
    - `git add .` : 현 디렉토리의 모든 작업 사항이 저장된 파일을 staging area로 전송.<br>
      - 하위 디렉토리에 존재하는 저장 된 모든 작업 사항 또한 staging area로 보냄.
    - untracked 상태의 파일을 staged로 변경
    - modifed 상태의 파일을 staged로 변경
  <br>
  <br>

- `git restore --staged 파일명.확장자` : add 명령어를 통해 staging area에 올린 파일을 치울때 사용.<br>
  ![](/image/git%20restore.PNG)

- `git commit -m '주석에 넣을 내용` : staging area에 올라가 있는 파일들을 버전화(포장) 시키는 기능.
  ![](/image/git%20commit.PNG)

- `git push '원격저장소이름' '브랜치 명칭'` : 원격 저장소로 로컬 저장소의 최근 변경 사항(버전 업된 커밋 내용)을 올림 (로컬 저장소의 내용을 밀어 넣음. ***push***)
  ![](/image/git%20push.PNG)
  - 협업을 하다보면 특정 오류가 발생하는 경우가 있는데 이를 ***[push conflict](/%EC%9E%90%EB%A3%8C%20%EB%AA%A8%EC%9D%8C%20%EB%A7%81%ED%81%AC%EC%9A%A9/pushcoflict.md)*** 라고 칭하며, 해당 문제를 해결하는 방법에 대해서는 링크 되어 있는 문서에서 추가적으로 서술.

<br>

- `git pull '원격저장소이름' '브랜치 명칭'` : 원격 저장소로부터 변경된 내역을 받아와서 이력을 병합함.
  - 해당 기능은 협업(여러명이서 작업) 중 원격 저장소에 있는 최신 변경 내역을 받아올 때 주로 사용함.<br>
    보통 본인이 혼자 작업하는 경우 pull기능이 필요하지 않음.<br>
    만약 로컬 저장소에 있는 파일이 날라가는 경우, 차후 추가설명 할 ***`git clone`*** 명령어를 통해 새롭게 로컬 저장소 제작
  
  



