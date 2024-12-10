### 페어프로그래밍 규칙

- 30분씩 돌아가면서 한다.
- 소통 열심히 하기!
- 커밋은 최대한 기능 별로 쪼개어 보내기

### 커밋 컨벤션

- `docs`, `feat`, `fix`, `refactor`, `rename`, `style`, `test`

### 요구사항

- 사용자가 숫자와 연산자를 입력한다
  - 키패드(`=`, `-`, `/`, `*`, 숫자), 화면 클릭 모두 동작해야한다.
- 입력된 수식을 사칙 연산 우선 순위에 맞춰 계산한다.
- 사칙 연산 우선 순위
  - 1순위: `x`, `/`
  - 2순위: `+`, `-`
- 사칙 연산 우선 순위가 잘 나오는지 test 코드 작성하기
  - `2 + 3 x 4 / 2 = 8`

### 기능 구현 전 설계

- 1. 간단한 인터페이스 구현
- 2. 기능 구현
  - [x] 입력한 값 유효성 검사 기능 (숫자와 연산자 외 다른 문자 입력 시 예외 처리)
  - [x] 우선 순위 판단 기능
  - [x] 계산된 값 출력 기능
  - [ ] 음수 계산 구현
  - [x] 계산된 값을 이어서 계산하는 기능
  - [x] 콤마 찍어서 출력 기능
- 3. test 코드 작성
- 4. css 스타일 구현

### 계산 전 예외 처리

1. 기호를 반복해서 넣었을 때
2. `.`을 반복해서 넣었을 때
3. 기호를 먼저 눌렀을 때
4. 기호를 마지막으로 누르고 '='을 눌렀을 때

- 계산기마다 작동 방식이 다름
- 아이폰 계산기의 방식을 채택
  - ex. 2+3+ 입력 후 = 을 눌렀을 때 5로 정상 계산

5. 0이 반복적으로 눌렸을 때

- 0만 입력하였을 때 0을 더 입력하려고 하는 경우
- 연산자 다음에 0 입력 후 0을 더 입력하려고 하는 경우
