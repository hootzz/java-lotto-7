# java-lotto-precourse

# 로또 게임
사용자로부터 구입 금액을 입력받아 로또를 발행하고, 추첨 결과에 따라 당첨 내역과 수익률을 계산하는 프로그램

## 기능 요구사항

### 1. 로또 구매
- [x] 구입 금액 입력 받기
    - [ ] 1,000원 단위로만 입력 가능
    - [ ] 1,000원으로 나누어 떨어지지 않는 경우 예외 처리 
      (`[ERROR] 로또 구입 금액은 1,000원 단위여야 합니다.`)
    - [ ] 숫자가 아닌 입력 예외 처리
      (`[ERROR] 숫자만 입력 가능합니다.`)

### 2. 로또 발행
- [x] 구입 금액만큼 로또 발행
    - [ ] 1장당 1,000원
    - [ ] 각 로또는 6개의 번호로 구성
    - [ ] 번호는 1~45 범위의 랜덤 숫자
    - [ ] 중복되지 않는 숫자 선택
    - [ ] 번호는 오름차순 정렬하여 출력

### 3. 당첨 번호 입력
- [x] 당첨 번호 6개 입력 받기
    - [ ] 쉼표(,)로 구분된 6개의 숫자
    - [ ] 1~45 범위 검증
      (`[ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.`)
    - [ ] 중복 번호 검증
      (`[ERROR] 당첨 번호에 중복된 숫자가 있습니다.`)
    - [ ] 숫자가 아닌 입력 예외 처리
      (`[ERROR] 숫자만 입력 가능합니다.`)
    - [ ] 6개가 아닌 경우 예외 처리
      (`[ERROR] 당첨 번호는 6개여야 합니다.`)

### 4. 보너스 번호 입력
- [x] 보너스 번호 1개 입력 받기
    - [ ] 1~45 범위 검증 
      (`[ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.`)
    - [ ] 당첨 번호와 중복 검증
      (`[ERROR] 보너스 번호가 당첨 번호와 중복됩니다.`)
    - [ ] 숫자가 아닌 입력 예외 처리 
      (`[ERROR] 숫자만 입력 가능합니다.`)

### 5. 당첨 결과 계산
- [x] 각 로또별 당첨 여부 확인
    - [ ] 3개 일치: 5등 (5,000원)
    - [ ] 4개 일치: 4등 (50,000원)
    - [ ] 5개 일치: 3등 (1,500,000원)
    - [ ] 5개 일치 + 보너스 번호: 2등 (30,000,000원)
    - [ ] 6개 일치: 1등 (2,000,000,000원)

### 6. 결과 출력
- [x] 당첨 통계 출력
    - [ ] 각 등수별 당첨 개수
    - [ ] 수익률 계산 (소수점 둘째 자리에서 반올림)
    - [ ] 총 수익률 = (당첨 금액 합계 / 구입 금액) * 100

## 프로그래밍 요구사항

### 프로그래밍 제약사항
- Java 코드 컨벤션 준수
- indent depth 2까지만 허용
- 3항 연산자 사용 금지
- 메서드 길이 15라인 이하
- else 키워드 사용 금지
- Java Enum 활용
- 모든 기능은 단위 테스트 작성 (UI 로직 제외)

### 라이브러리 사용
- `camp.nextstep.edu.missionutils.Randoms`
- `camp.nextstep.edu.missionutils.Console`

### 기본 제공 클래스
- `Lotto` 클래스 활용 (numbers 필드의 접근 제어자 변경 불가)