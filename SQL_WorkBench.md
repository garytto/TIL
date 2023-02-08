## 주의 사항
- 만약 본인의 workbench의 버전이 8.0.32 인 경우 8.0.31로 다운그레이드 하여 재 다운로드해야한다.
  - 방법
    1. 기존 Sql 다운 받을 때 공식 사이트에서 다운 받은 mysql-installer-community-8.0.32 파일을 실행.
    2. remove 버튼을 클릭.
      ![](/image/workbench_remove.PNG)
    3. MySQL Workbench 8.0.32 선택 후 삭제 진행
      ![](/image/workbench_remove_2.PNG)
      ![](/image/workbench_remove_3.PNG)
    4. 삭제 완료 후 [링크](https://downloads.mysql.com/archives/workbench/)를 타고 가 해당 파일 다운로드
      ![](/image/workbench_download.PNG)
    5. 해당 파일 설치 진행하면 끝.
## How To Use
 - 워크 밴치 실행 후 MySQL과 연결 점 제작 진행.
  1. MySQL Connections 옆 추가 버튼 클릭
  ![](/image/mysql_branch_make.PNG)
  2. Connection Name (연결점 명칭)을 작성 후 OK를 눌러 생성
   - Store in valt password 버튼 클릭 후 서버 비밀번호를 입력하고 생성을 하면, 연결점 진입 마다 서버 password를 입력해야하는 수고를 덜 수 있다.
  ![](/image/setting_new_connection.PNG)
  3. 해당 서버 연결점 클릭하여 진입

## 데이터 베이스 설정
 1. Administration 탭의 Management / Data Import/Restore 진입.
  ![](/image/sql_data_setting_1.PNG)
 2. Import from Self-Contained File 클릭 후 우측에 있는 ...(더보기)를 클릭하여, 본인이 사용할 데이터 베이스 파일 선택.
  ![](/image/sql_data_setting_2.PNG)
 3. 우측 하단 Start import 버튼을 통해 해당 Sql 파일 import 진행.
  ![](/image/sql_data_setting_3.PNG)

## 기본적인 활용 (Quary 활용)
- 해당 활용은 기본적으로 Quary Work Space에서 진행해야함으로 본인의 현재 work Space가 Quary인지 확인 요망.
    ![](/image/HTN_WorkSpace.PNG)

1. 본인이 확인하고자 하는 데이터베이스 `더블` 클릭(예 : classicmodels)
  - 데이터 베이스는 Schemas 탭에서 확인이 가능하니 참고.
  - 단순 클릭만 하면 지정이 되지 않음.
  - 더블 클릭 시 해당 데이터베이스의 글씨체가 굵어지며 하이라이트 표시가 됨.
  ![](/image/qua_progress_1.PNG)
    - **주의 사항**
      - 만약? 데이터 베이스를 선택하지 않고 명령어 작성 후 실행한다면?
      <br> `No database selected ~` 오류가 발생한다.
      ![](/image/ifnotselectdatabase.PNG)

2. Quary창에서 명령어 입력 후 실행 버튼 클릭
  - 명령어 예시 : `SELECT * FROM customers;`
  - 이후 번개 모양 버튼을 클릭하여 실행 진행.
  ![](/image/qua_progress_2.PNG)
    - `SELECT` 명령어 주의 사항.
      해당 명령어는 `From ~`을 통해 선택한 데이터베이스 Tables 탭 내 값을 확인하는 명령어로, 만약 Tables 내에 관련 값이 없다면 오류가 발생하니 참고.<br>
      - `Table 'classicmodels.customer' does't exist` 오류 발생
          <br> **classicmodels 하위에 customer 라는 것은 존재하지 않는다.**
        ![](/image/select_careful.PNG)
3. 검색 값 확인.
  ![](/image/qua_progress_3.PNG)

  





