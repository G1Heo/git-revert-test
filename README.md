164126: git log 통해 head commit 파악
<img width="749" height="675" alt="스크린샷 2026-01-08 16 41 26" src="https://github.com/user-attachments/assets/41f484a9-d646-449b-a7b8-142abfb202c9" />

README가 수정된 커밋: 3개
가장 최근 README 수정 커밋의 hash 값: 0e6ab70

## 01. HEAD는 무엇을 가리키고 있나요?
feature/change-weather-agent-ment 브랜치의 최신 커밋인 0e6ab70을 가리키고 있음. 현재 작업 디렉토리의 상태는 "사용법(usage instructions)이 추가된 상태"임

## 02. HEAD 이전 커밋으로 되돌아가면 어떤 변화가 발생할까요?
최신 커밋(0e6ab70)에서 추가했던 사용법(usage instructions) 관련 텍스트가 README.md 파일에서 사라지게 됨. 파일 내용은 프로젝트 설명까지만 존재하던 상태로 돌아감

## 03.협업 환경에서 reset 대신 revert가 필요한 이유는 무엇일까요?


164143, 164233: revert로 commit 삭제
<img width="771" height="680" alt="스크린샷 2026-01-08 16 41 43" src="https://github.com/user-attachments/assets/89c99a18-ada7-49a3-b2e7-720c3ff4340a" />
<img width="760" height="363" alt="스크린샷 2026-01-08 16 42 33" src="https://github.com/user-attachments/assets/1291d67f-a174-4859-92b1-e828f84a7450" />

### 작업 이력의 변화: 
reset을 썼다면 0e6ab70 이력 자체가 사라졌겠지만, revert를 사용했기에 0e6ab70 이력도 남고 그 뒤에 취소 기록인 8e95f27 이력도 남았음.
### 협업 관점에서의 장점: 
만약 이 코드가 Github 등에 이미 올라간 상태였다면, 이력을 지우는 reset은 다른 팀원들의 이력과 충돌을 일으킬 수 있음. 하지만  revert는 실수를 바로잡는 새로운 커밋을 추가하는 방식이므로, 팀원들이 그대로 pull을 받아도 아무런 충돌 없이 실수가 수정됨.
