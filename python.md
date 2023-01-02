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
  - 정수
    - 모든 정수의 타입은 int
    - 매우 큰 수를 나타낼 떄 오버플로우가 발생하지 않음
      - 오버플로우(overflow) : 데이터 타입별로 사용할 수 있는 메모리의 크기를 넘어서는 상황
      - 임의 정밀도 산술(Arbitrary precision arithmetic)을 통해 고정된 형태의 메모리가 아닌 가용 메모리들을 활용하여 모든 수 표현에 활용
  - 실수
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
### 불린형
  - True / False 값을 가진 타입은 bool
    - True는 1, False는 0에 해당함.
  - 비교/논리 연산을 수행함에 있어서 활용됨
  - 다음은 모두 Flase로 변환
    - 0,0.0,(),[],{},", None

### 연산자
  - 산술 연산자(Arithimetic Operator)
    - 기본적인 사칙연산 및 수식 계산
  - 비교 연산자(Comparison operator)
    - 값을 비교하며, True / Flase 값을 리턴함.

### 컨테이너
- 컨테이너란 여러 개의 값을 담을 수 있는 것(객체)으로, ㅋ서로 다른 자료형을 저장할 수 있음
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

