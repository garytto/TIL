# Python
  - 객체지향 언어이며, 모든 것이 객체로 구현되어있는 프로그래밍 언어.

## 객체와 변수

### 객체 (object)
  - 숫자, 문자, 클래스 등 값을 가지고 있는 모든 것

### 변수
  - 컴퓨터 메모리 어딘가에 저장되어 있는 객체를 참조하기 위해 사용되는이름
  - 동일 이름에 다른 객체를 언제든 할당할 수 있기 떄문에 `변수` 라고 불림
  - 변수는 할당 연산자(=)를 통해 값을 할당함.
  - type()
    - 변수에 할당된 값의 타입
  - id()
    - 변수에 할당 된 값의 고유한 고유값(identity)이며, 메모리주소이다.
#### 변수 할당
  - 같은 값을 동시에 할당할 수 있음.
  ``` python
  x = y = 1004
  ```

   - 다른 값을 동시에 할당할 수 있음.
  ```python
  x, y = 1, 2
  ```
  - 단 앞 변수와 명시할 값의 숫자가 동일해야 작동한다.<br>
    하기의 예시처럼 할당하면 작동하지 않음,
  ```python
  x, y = 1, 2, 3
  
  상기와 같이 할당 시 오류 발생.
  ```
## 자료형

### 자료형 분류
  - 숫자
    - 수치형(Numeeric Type)
      - int (정수,integer)
      - float (부동소수점, 실수, floating point number)
      - complex (복소수, complex number)
    - 불린형(Boolean Type)

  - 시퀀스(Sequence)
    - 문자열(String)
    - 튜플(Tuple)
    - 리스트(List)
    - 레인지(Range)
  
  - 컬렉션(Collection)
    - 집합(Set)
    - 딕셔너리(Dictionary)

### 수치형
  - **정수(`int`)**
    - 모든 정수의 타입은 int
    - 매우 큰 수를 나타낼 떄 오버플로우가 발생하지 않음
      - 오버플로우(overflow) : 데이터 타입별로 사용할 수 있는 메모리의 크기를 넘어서는 상황
      - 임의 정밀도 산술(Arbitrary precision arithmetic)을 통해 고정된 형태의 메모리가 아닌 가용 메모리들을 활용하여 모든 수 표현에 활용
  - **실수(`float`)**
    - 정수가 아닌 모든 실수는 float 타입
    - 부동소수점
      - 실수를 컴퓨터가 표현하는 방법 -2진수(비트)로 숫자를 표현
      - 이 과정에서 floating point rounding error가 발생하여, 예상치 못한 결과가 발생
        - Floating point rounding error : 부동소수점에서 실수 연산 과정에서 발생 가능
            - 값 비교 과정에서 정수가 아닌 실수인 경우 주의할 것
            - 매우 작은 수보다 작은지를 확인하거나 math 모듈 활용
            ```python
            # 1. 임의의 작은 수
            abs(a - b) <= 1e-10

            # 2. math 모듈 활용
            import math
            math.isclose(a, b)
            ```
  - **복소수(`complex`)**
    - 실수부와 허수부로 구성된 복소수는 모두 complex 타입.
      - 허수부를 j로 표현
      ```python
      a = 3+4j
      type(a)
      # <class 'complex'>
      a.real
      # 3.0
      a.img
      # 4.0
      ```
### 불린형
  - True / False 값을 가진 타입은 bool
    - True는 1, False는 0에 해당함.
  - 비교/논리 연산을 수행함에 있어서 활용됨
  - 다음은 모두 Flase로 변환
    - 0,0.0,(),[],{},", None

### 연산자
  - 산술 연산자(Arithimetic Operator)
    - 기본적인 사칙연산 및 수식 계산
  ![](/image/Operator.PNG)
  - 복합 연산자(In-place Operator)
    - 연산과 할당이 동시에 진행된다.
  ![](/image/In-place%20operator.PNG)

  - 비교 연산자(Comparison Operator)
    - 값을 비교하며, True / Flase 값을 리턴함.
  ![](/image/Comparison%20operator.PNG)

  - 논리 연산자(Logical Operator)
    - 논리식을 판단, 참(True)와 거짓(False)를 반환함.
  ![](/image/Logical%20Operator.PNG)
      
      - and : 모두 참인 경우 참, 그렇지 않으면 거짓 
      ![](/image/and.PNG)
      
      - or : 둘 중 하나만 참일경우 참, 그 외는 거짓
      ![](/image/or.PNG)

      - not : 참/거짓의 반대 결과.
      ![](/image/not.PNG)


## 컨테이너
- 컨테이너란 여러 개의 값을 담을 수 있는 것(객체)으로, 서로 다른 자료형을 저장할 수 있음
- 컨테이너의 분류
  - 순서가 있는 데이터(Ordered) vs 순서가 없는 데이터 (Unordered)
  - 순서가 있다 != 정렬 되어 있다.
  - 시퀀스
    - 문자열(immutable) : 문자들의 나열
    - 리스트(mutable) : 변경 가능한 값들의 나열
    - 튜플(immutable) : 변경 불가능한 값들의 나열
    - 레인지(immutable) : 숫자의 나열
  
- 컬렉션 /비시퀀스
    - 세트(mutable) : 유일한 값들의 모음
    - 딕셔너리 (mutalbe) : 키 - 값들의 모음

### **시퀀스형 컨테이너**
 - 시퀀스형 주요 공통 연산자
  ![](/image/Sequence%20Container.PNG)

 - **문자열(String Type)**
   - 모든 문자는 str 타입
   - 문자열은 작은 따옴표(')나 큰 따옴표를(")를 활용하여 표기
    - 문자열을 묶을 때 동일한 문장부호를 활용
    - PEP8에서는 소스코드 내에서 하나의 문장부호를 선택하여 유지하도록 함
  ```python
  print('hello')
  # hello
  print(type('hello'))
  # <class 'str'>
  ```

  - **중첩따옴표(Nested Quotes)**  
    - 따옴표 안에 따옴표를 표현할 경우
      - 작은 따옴표가 들어 있는 경우는 큰 따옴표로 문자열 생성
      - 큰 따옴표가 들어 있는 경우는 작은 따옴표로 문자열 생성
    ```python
    print("문자열 안에 '작은 따옴표'를 사용하려면 큰 따옴표로 묶는다.")
    print('문자열 안에 "큰 따옴표"를 사용하려면 작은 따옴표로 묶는다.)
    ```

  - **삼중따옴표(Triple Quotes)**
    - 작은 따옴표나 큰 따옴표를 삼중으로 사용
      - 따옴표 안에 따옴표를 넣을 때,
      - 여러줄을 나눠 입력할 떄 편리
      ```python
      print('''문자열 안에 '작은 따옴표'나 "큰 따옴표"를 사용할 수 있고 여러 줄을 사용할 때도 편리하다.''')
      ```

  - **인덱싱**
    - 인덱스를 통해 특정 값에 접근할 수 있음 (0 ~ )
    - 인덱스는 기본적으로는 0애서 부터 시작합니다.
    - s[1] => 'b'
  ![](/image/index.PNG)

  - **슬라이싱(Slicing)**
    - 슬라이싱의 구조는 기본적으로 `a[start:end:step]`과 같이 구성 되어 있다.
      - 앞의 0은 시작점을 의미하며 뒷 부분은 종착점(7번째까지)을 의미한다.
      - a[start, end] = end의 값은 포함되지 않는다.(해당 값의 직전까지 포함.)
      - a[start, end, step] = start 부터 end 까지의 값 중 step 만큼 뛰어 넘겨서 나타낸다.<br>
      만약 step 값이 정수라면 좌에서 우측으로 진행, 음수라면 우측에서 좌로 진행한다.
        * 하기 예시를 확인해보자.
      ```python
      s = "12345678"

      print(s[0:7]) #1234567 0 번째(1)에서부터 7번째까지의 값이 출력, 7번째 값은 포함X
      print(s[1:]) #2345678 1 번째(2)에서부터 모든 값이 출력
      print(s[:4]) #1234 4 번째까지의 모든 값이 출력 , 4번째 값은 포함 x
      print(s[-4:]) #5678 뒤에서 4번째 값 부터 이후 모든 값이 출력
      print(s[-8:]) #12345678 뒤에서 8번째 값(1) 부터 모든 값이 출력
      print(s[0:8:2]) #1357 0~ 8 번째 값을 2칸씩 띄어서 출력
      print(s[ : :2]) #1357 시작 부터 처음 값을 2칸씩 띄어서 출력
      print(s[-8: :3]) #147 -8(1) 번째 부터 끝 범위 내 값 중 3칸씩 띄어서 출력 
      print(s[ : :-1]) #87654321 역행해서 출력
      ```
        - 참고 사진
      ![](/image/slice1.PNG)
      ![](/image/slice2.PNG)

   - **기타**
     - 결합(Conatenation)
     ```python
     'hello, '+ 'python!'
     # 'hello, python!'
     ```
     - 반복 (Repetition)
     ```python
     'hello' * 3
     # 'hellohellohello'
     ```
     - 포함 (Membership)
     ```python
     print('a' in 'apple')
      # True
     print('appb' in 'apple')
      # False
     print('app' in 'apple')
      # True
     print('b' in 'apple')
      # false
     print('l' in 'apple')
      # True
     ```
  - **Escape sequence**
    - 문자열 내에서 특정 문자나 조작을 위해서 역슬래시(`\`)를 활용하여 구분 <br>
      ![](/image/escape.PNG)
      ```python
      print('철수 \'안녕\'')
      # 철수 '안녕'
      print('이 다음은 엔터.\n 그리고 탭\t 탭')
      # 이 다음은 엔터.
      # 그리고 탭   탭
      ```
  - 문자열 특징
    - 문자열은 변경 불가능(`Immutable`)하며, 반복 가능하다(`Iterable`)
      - 추후 수업에서 배울 예정 배우면 해당 내용 추가하겠음!

  ### List(리스트)
  - 리스트의 정의
    - 변경 가능한 값들의 나열된 자료형
    - 순서를 가지며, 서로 다른 타입의 요소를 가질 수 있음.
    - 변경 가능하며(`Mutable`), 반복 가능함(`Iterable`)
    - 항상 대괄호 형태로 정의하며, 요소의 구분은 콤마로 한다.
  
  - 생성과 접근
    - 리스트는 대괄호([]) 혹은 list() 를 통해 생성
    - 순서가 있는 시퀀스로 인덱스를 통해 접근 가능
      - 값에 대한 접근은 list[i]
    ![](/image/listExample.PNG)
  
  - 리스트 값 추가/삭제
    - 값 추가는 .append()를 활용하여 추가하고자 하는 값을 전달
    ```python
    yee_yee = [1,2,3,4]
    yee_yee.append(9)
    print(yee_yee) # [1,2,3,4,9]
    ```
    - 값 삭제는 .pop()을 활용하여 삭제하고자 하는 `인덱스`를 전달
    ```python
    numberpop = [1, 3, 4, 10]
    print(numberpop) # [1, 3, 4, 10]
    numberpop.pop(2) # 3번째 값 제거
    print(numberpop) # [1, 3, 10] 
    ```
  
  - len(Length)
    - len() 명령어는 ()안의 객체의 갯수를 세어주는 모듈이다.
    ```python
    test = [1,3,9,22]
    print(len(numberpop)) # 4
    ```

  - 반전 (reverse)
    - .reverse() 명령어를 통해 반대로 정렬 시킬 수 있다.
    ```python
    test = [1, 3, 99, 22, 738, 49]
    print(test) # [1, 3, 99, 22, 738, 49]
    test.reverse() # 반전
    print(test) # [47, 738, 22, 99, 3, 1]
    ```

  - 정렬 (sort)
    - .sort() 명령어를 통해 오름차순으로 정렬할 수 있다.
    ```python
    test = [1, 3, 99, 22, 738, 49]
    print(test) # [1, 3, 99, 22, 738, 49]
    test.sort() # 오름차순으로 정렬
    print(test) # [1, 3, 22, 49, 99, 738]
    ```
    - .reverse() 명령어를 통해 내림차순으로 정렬할 수도 있다.
    ```python
    test = [1, 3, 99, 22, 738, 49]
    print(test) # [1, 3, 99, 22, 738, 49]
    test.sort() # 오름차순으로 정렬
    test.reverse() # 반전
    print(test) # [738, 99, 49, 22, 3, 1]
    ```
  ### None
   - 파이썬 자료형 중 하나
   - 파이썬에서는 값이 없음을 표현하기 위해 None 타입이 존재함
   - 일반적으로 반환 값이 없는 함수에서 사용하기도 함.
  - **`상기 내용은 차후 추가 서술 예정.`**

  ## **Python 시작하기**

  ### **코드 작성 주의사항**
  - 대소문자 구분
  - 띄어쓰기, 문장부호 등 주의 깊게 활용
  - 들여쓰기(Identation)
    - 문장을 구분할 때, 들여쓰기 (indenation)를 사용
    - 들여쓰기를 할 떄는 4칸(space키 4번) 혹은 1탭(Tab키 1번)을 입력
      - `주의!` 한 코드 안에서는 반드시 한 종류의 들여쓰기를 사용 -> 혼용 금지
        - Tab으로 들여쓰면 계속 탭으로 들여써야함
        - 원칙적으로는 공백 (빈칸, space) 사용을 권장 *PEP8 권장사항

  ### **주석(Comment)**
  - 코드에 대한 설명
    - 중요한 점이나 다시 확인하여야 하는 부분을 표시
    - 컴퓨터는 주석을 인식하지 않음 사용자만을 위한 것
  - 주석으로 처리될 내용 앞에 '#'을 입력
    - 한줄을 온전히 사용할 수도 있고, 그 줄 코드 뒷부분에 작성 할 수 있음
    - VS Code에서는 단축키(ctrl+/)를 활용하여 주석 처리를 할 수 있음
  
  ### 사용자 입출력
  - input([prompt])
    - 사용자로부터 값을 즉시 입력 받을 수 있는 내장함수
      - 대괄호 부분에 문자열을 넣으면 입력 시, 해당 문자열을 출력할 수 있음
    - ***반환값은 항상 문자열의 형태로 반환***

  - print()
    - 모니터 화면에 결과물을 출력하기 위하여 활용
    - 변수의 경우 변수의 값을 출력하며, 객체별 표현 방식에 따라 출력하게 됨.
