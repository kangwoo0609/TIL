# Python 기초 핵심 정리 🐍

## 1. 프로그래밍과 Python

### 프로그래밍이란?
-   **프로그램**: 문제 해결을 위한 **명령어들의 집합** (예: "두 블록 직진 후 좌회전"이라는 길 찾기 방법)
-   **프로그래밍**: 컴퓨터가 이해할 수 있는 언어로 명령어 뭉치(프로그램)를 만드는 과정

### 왜 Python을 사용하는가?
-   **쉬운 문법**: 사람이 생각하는 방식과 유사하여 배우기 쉽고 간결
-   **강력한 커뮤니티**: 크고 활성화된 커뮤니티 덕분에 자료를 얻거나 문제를 해결하기 용이
-   **광범위한 응용 분야**: 웹 개발, 데이터 분석, 인공지능(AI), 업무 자동화 등 다양한 분야에서 활용
-   **실행**: 보통 `.py` 확장자를 가진 파일을 작성한 후 실행하는 방식으로 사용

---

## 2. 코드의 기본 구성 요소

### 값 (Value)
-   더 이상 계산될 수 없는 가장 기본적인 데이터 조각
-   **예시**: 숫자 `10`, 문자열 `'hello'`, 불리언 `True`

### 표현식 (Expression)
-   하나의 **'값(Value)'으로 평가될 수 있는** 코드
-   **평가(Evaluation)**: 표현식을 계산하여 값을 만들어내는 과정
-   **예시**: `3 + 5`는 평가를 통해 `8`이라는 값을 도출

### 변수 (Variable) 📦
-   특정 값을 다시 사용하기 위해, 그 값에 붙여주는 **고유한 이름**. 메모리 상의 객체를 가리키는 이름표
-   **할당 (Assignment)**: 값에 변수라는 이름을 붙이는 과정. Python에서 `=` 기호는 '같다'가 아닌 **'할당한다'**는 의미
    ```python
    # 36.5 라는 값을 degrees 라는 변수에 할당
    degrees = 36.5
    ```
-   **재할당 (Re-assignment)**: 이미 할당된 변수에 다른 값을 새로 할당하는 것. 변수는 이전 값을 잊고 새로운 값을 가리킴
-   **작명 규칙**:
    -   영문 알파벳, 숫자, 언더스코어(`_`) 사용 가능
    -   숫자로 시작할 수 없음
    -   Python 예약어(예: `True`, `if`, `for`)는 사용 불가

---

## 3. 데이터 타입 (Data Types)

해당 값이 어떤 종류이고 어떤 연산이 가능한지 알려주는 분류

### 숫자형 (Numeric Types) 🔢
-   **정수 (int)**: 소수점이 없는 숫자 (예: `10`, `0`, `-100`)
-   **실수 (float)**: 소수점이 있는 숫자 (예: `3.14`, `-0.5`)

> **주의**: 연산자 우선순위가 존재하며, 헷갈릴 경우 소괄호 `()`를 사용하여 명확히 지정하는 것이 좋음

### 시퀀스 타입 (Sequence Types) 📜
-   여러 개의 값을 **순서대로 나열**하여 저장하는 자료형
-   **공통 특징**:
    -   **순서 (Ordering)**: 각 값에 0부터 시작하는 고유한 순서(인덱스)가 있음
    -   **인덱싱 (Indexing)**: 특정 위치의 값을 번호로 조회 가능
    -   **슬라이싱 (Slicing)**: 전체 범위 중 일부를 잘라낼 수 있음
    -   **길이 (Length)**: `len()` 함수로 길이를 구할 수 있음
    -   **반복 (Iteration)**: 반복문을 통해 각 요소를 순서대로 하나씩 꺼낼 수 있음
-   **종류**: `str` (문자열), `list`, `tuple`, `range` 등

---

## 4. 문자열 (String)

-   문자들의 순서가 있는 **변경 불가능한(immutable)** 시퀀스 자료형
-   작은따옴표(`'`)나 큰따옴표(`"`)로 감싸서 만듦

### f-string (Formatted String Literals)
-   문자열 안에 변수나 표현식의 결과를 손쉽게 삽입하는 방법. **알고리즘 문제 풀이나 데이터 출력 시 매우 유용**
    ```python
    name = '홍길동'
    age = 25
    greeting = f'안녕하세요, 제 이름은 {name}이고 나이는 {age}입니다.'
    print(greeting)
    # 출력: 안녕하세요, 제 이름은 홍길동이고 나이는 25입니다.
    ```

### 인덱싱과 슬라이싱
-   **인덱스**: 0부터 시작하는 고유 번호. 음수 인덱스는 맨 뒤부터 접근하며, `-1`이 마지막 값을 의미
-   **슬라이싱**: `my_sequence[start:stop:step]` 형식으로 범위를 잘라냄
    -   `start`: 시작 인덱스 (포함)
    -   `stop`: 끝 인덱스 (**미포함**)
    -   `step`: 가져오는 간격

### 불변성 (Immutability)
-   문자열은 생성된 후에 **내용 자체를 수정할 수 없습니다**
-   문자열을 수정하고 싶다면, 새로운 변수에 변경된 문자열을 만들어 재할당 필요

---

## 5. 기타 주요 개념 및 스타일 가이드

### 표현식 vs 문장
-   코드를 실행했을 때 하나의 **값이 남으면 표현식**, 그렇지 않으면 **문장(Statement)**
-   **문장 예시**: 변수 할당문 (`degrees = 36.5`), 제어문 (`if`, `for`) 등

### 코드 스타일 가이드 (PEP 8) 🎨
-   코드의 **일관성과 가독성**을 높이기 위한 규칙 모음. 협업과 유지보수를 위해 매우 중요
-   **주요 규칙**:
    -   변수명은 그 쓰임새를 **직관적으로** 알 수 있게 짓는 게 좋음
    -   들여쓰기는 **공백(space) 4칸**을 사용
    -   한 줄의 길이는 **79자**로 제한
    -   함수나 클래스 정의 사이에는 적절한 **빈 줄을 추가**하여 가독성을 높이는 것이 좋음
    -   주석 (`#`)을 활용하여 코드에 대한 설명을 추가
