# java-lotto-precourse

## Goal

- **간단한 로또 발매기를 구현한다.**
- **당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.**
    - 1등: 6개 번호 일치 / 2,000,000,000원
    - 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
    - 3등: 5개 번호 일치 / 1,500,000원
    - 4등: 4개 번호 일치 / 50,000원
    - 5등: 3개 번호 일치 / 5,000원

## 기능 목록

1. **구입 금액 입력 기능**
    - [x] 입력 안내 문구를 출력한다.
    - [x] 구입 금액은 1,000원 단위의 숫자를 입력받는다.
    - [x] 입력이 비어있거나 숫자가 아니라면 예외 처리한다.
    - [x] 구입 금액이 0이라면 예외 처리한다.
    - [x] 구입 금액이 음수라면 예외 처리한다.
    - [x] 구입 금액이 int 범위를 벗어난다면 예외 처리한다.
    - [x] 구입 금액이 1,000원으로 나누어 떨어지지 않으면 예외 처리한다.
2. **로또 숫자**
    - [x] 로또 숫자는 1 이상 45 이하의 자연수이다.
3. **로또 발행 기능**
    - [x] 중복되지 않는 로또 숫자 6개를 무작위로 추첨해 로또 1장을 발행한다.
    - [x] 로또 번호를 오름차순으로 정렬한다.
    - [x] 로또 번호를 출력한다.
4. **로또 구매 기능**
    - [x] 로또는 1장 당 1,000원이다.
    - [x] 구입 금액을 1,000으로 나눈 수 만큼 로또를 발행한다.
    - [x] 발행한 모든 로또 번호를 출력한다.
5. **당첨 번호 입력 기능**
    - [x] 입력 안내 문구를 출력한다.
    - [x] 로또 숫자 6개를 입력받는다.
    - [x] 입력이 비어있다면 예외 처리한다.
    - [x] 입력한 숫자 중 하나라도 로또 숫자가 아니라면 예외 처리한다.
    - [x] 입력한 숫자가 정확히 6개가 아니라면 예외 처리한다.
    - [x] 중복된 로또 숫자를 입력한다면 예외 처리한다.
6. **보너스 번호 입력 기능**
    - [x] 입력 안내 문구를 출력한다.
    - [x] 로또 숫자 1개를 입력받는다.
    - [x] 입력이 비어있다면 예외 처리한다.
    - [x] 입력한 숫자가 로또 숫자가 아니라면 예외 처리한다.
    - [x] 입력한 숫자와 당첨 번호 중 하나라도 중복된다면 예외 처리한다.
7. **로또 당첨 기능**
    - [ ] 당첨 기준에 따라 로또 번호를 당첨 번호 및 보너스 번호와 비교한다.
    - [ ] 비교 결과 당첨된 내역을 저장한다.
    - [ ] 당첨 내역은 당첨 기준 별 당첨 횟수를 포함한다.
8. **총 수익률 기능**
    - [ ] 총 수익률은 `(당첨 금액의 총합) / (구입 금액)%`을 소수점 둘째 자리에서 반올림한 값이다.
9. **당첨 통계 기능**
    - [ ] 당첨 기준과 당첨 기준 별 당첨 횟수를 출력한다.
    - [ ] 총 수익률을 출력한다.
10. **예외 처리**
    - [x] 유효하지 않은 입력으로 인한 예외는 `IllegalArgumentException`를 발생시킨다.
    - [x] `IllegalArgumentException` 발생 시 에러 문구를 출력하고, 다시 입력받는다.
    - [x] 에러 문구는 `[ERROR]`로 시작한다.

## 클래스 구조

- 전체 애플리케이션의 기능을 두 개의 기능으로 분리한다.
    - [x] 로또 구매 기능
    - [ ] 로또 추첨 기능
- 각 기능은 별도의 입/출력 프롬포트를 갖는다.
    - [x] 로또 구매 입력 Prompt
    - [x] 로또 구매 출력 Prompt
    - [x] 로또 추첨 입력 Prompt
    - [ ] 로또 추첨 출력 Prompt
- 도메인 클래스 목록
    - [x] 금액
    - [x] 로또 숫자
    - [x] 로또
    - [x] 로또 묶음
    - [x] 보너스 번호
    - [x] 당첨 번호
    - [ ] 당첨 기준
    - [ ] 당첨 순위
    - [ ] 당첨 금액
    - [ ] 당첨 통계

## 테스트 목록

- 테스트 할 기능을 우선 구현한다.