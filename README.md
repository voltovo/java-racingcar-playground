## [NEXTSTEP 플레이그라운드의 미션 진행 과정](https://github.com/next-step/nextstep-docs/blob/master/playground/README.md)

---

## 학습 효과를 높이기 위해 추천하는 미션 진행 방법

---

1. 피드백 강의 전까지 미션 진행
   > 피드백 강의 전까지 혼자 힘으로 미션 진행. 미션을 진행하면서 하나의 작업이 끝날 때 마다 add, commit
   > 예를 들어 다음 숫자 야구 게임의 경우 0, 1, 2단계까지 구현을 완료한 후 push

![mission baseball](https://raw.githubusercontent.com/next-step/nextstep-docs/master/playground/images/mission_baseball.png)

---

2. 피드백 앞 단계까지 미션 구현을 완료한 후 피드백 강의를 학습한다.

---

3. Git 브랜치를 master 또는 main으로 변경한 후 피드백을 반영하기 위한 새로운 브랜치를 생성한 후 처음부터 다시 미션 구현을 도전한다.

```
git branch -a // 모든 로컬 브랜치 확인
git checkout master // 기본 브랜치가 master인 경우
git checkout main // 기본 브랜치가 main인 경우

git checkout -b 브랜치이름
ex) git checkout -b apply-feedback
```

---

### 연습 문제 : 문자열 덧셈 계산기

---

1. 기능 요구 사항
   > 문자로된 숫자를 모두 계산

- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환 (예: “” => 0, "1,2" => 3, "1,2,3" => 6, “1,2:3” => 6)
- 앞의 기본 구분자(쉼표, 콜론)외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 “//”와 “\n” 사이에 위치하는 문자를 커스텀 구분자로 사용한다. 예를 들어 “//;\n1;2;3”과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
- 문자열 계산기에 숫자 이외의 값 또는 음수를 전달하는 경우 RuntimeException 예외를 throw한다.

---

2. 구현할 기능 목록 (To Do List)

- [ ] 음수 여부 체크
- [ ] 문자열 길이 체크
  - [x] 빈 값이면 return 0
  - [ ] 한 자리 숫자면 return 숫자
- [ ] 구분자 구분 체크
  - [ ] 쉼표 구분자
  - [ ] 콤마 구분자
  - [ ] 커스텀 구분자 (//;\n)
