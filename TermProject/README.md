# 1. 게임의 소개
* 제목: Avoid Enemy
```
게임의 장르는 탄막 슈팅입니다.
점점 어려워지는 스테이지를 한 단계씩 클리어하는 과정을 통해 높은 스코어를 얻는 것이 이 게임의 최종 목적입니다.
게임 플레이 방법은 이동을 위한 W,A,S,D와 공격을 위한 마우스로 구성됩니다.
```

# 2. GameState의 수 및 각각의 이름
* Scene은 4개로 구성
```
- Start state
- Title state
- Ingame state
- Pause state
```

# 3. 각 GameState 별 다음 항목
* Start: 게임이 실행됐을 때 최초로 한 번만 출력되는 state
  ```
  객체: KPU 이미지 로고
  처리할 키/마우스: 없음
  다른 state 이동 조건: 몇초 대기 후 자동으로 타이틀 state로 이동
  ```
* Title: 게임 시작을 준비하기 위한 state
  ```
  객체: 시작 버튼, 종료 버튼, 스코어, 플레이어의 모양을 표시하는 이미지
  처리할 키/마우스: 버튼을 위한 마우스 처리
  다른 state 이동 조건: 시작 버튼을 눌렀을 때 Ingame state로 이동
  ```
* Ingame: 게임이 플레이되는 스테이트입니다.
  ```
  객체: 플레이어, 적, 줌, 플레이어 상태 ui, 타격을 particle, 카메라
  처리할 키/마우스: 이동을 위한 W,A,S,D와 공격을 위한 마우스 처리, 다른 state를 위한 키 등
  다른 State 이동 조건: Esc키를 누르면 Pause state로 이동
  ```
* Pause:
  ```
  객체: 다시 시작 버튼, 재개 버튼, 종료 버튼
  처리할 키/마우스: 버튼을 위한 마우스 처리
  다른 state 이동 조건: 다시 시작 버튼을 누르면 Ingame state가 리셋된 상태로 시작, Esc키 혹은 재개 버튼을 누르면 InGame state가 재개
  ```

# 4. 필요한 기술
- 다른 과목에서 배운 기술
```
1. 이미지 회전 조정
2. 이미지 크기 조정
```
- 이 과목에서 배울 것으로 기대되는 기술
```
1. 사운드 처리
2. 충돌 처리
3. 텍스처 관리
4. 데이터 로드 방법
5. UI
6, 카메라
```
- 다루지 않은 것 같아서 수업에 다루어 달라고 요청할 기술
```
1. 이미지 회전 조정할 수 있는 방법
2. 이미지 크기 조정할 수 있는 방법
3. 이미지 투명도를 조정할 수 있는 방법
```