## 이 파일은 단순 명령어 리스트 정리 용
---
### GO!
- `git init` : 특정 폴더에 git 저장소(repository)를 만들고 버전 관리
    - **.git** 폴더가 생성됨(숨김 상태)
    - **git bash**에서는 (master)라는 표기를 확인 가능.
    - ![](/image/git%20init.PNG)
    - `만약 관리를 안할거라면 .git 폴더를 삭제하면됨.`
    
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



