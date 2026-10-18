# Git 첫걸음 워크샵 키트 v1.0 (60분)

VS Code의 GitHub Copilot 채팅을 "개인 튜터"로 활용해 Git의 핵심 개념을 이해하고 직접 실습하는 1시간 과정이다.
명령어를 몰라도 된다. 가이드의 프롬프트를 복사해 Copilot 채팅에 붙여넣고, 결과를 VS Code 화면에서 확인하면 된다.

- 기준 콘텐츠: GitHub Git Guides — https://github.com/git-guides
- 실습 도구: Visual Studio Code + Git + GitHub Copilot (Chat)

## 1. 시작 3단계

1. 이 폴더(`git-workshop-kit-v1.0`) 전체를 원하는 위치(예: 바탕화면)에 압축 해제한다.
2. VS Code에서 **File > Open Folder...** 로 이 폴더를 연다. 신뢰 여부를 물으면 **Trust** 를 선택한다.
3. `guide/LAB-GUIDE.md` 를 열고 Step 0부터 순서대로 따라 한다.

## 2. 폴더 구성

| 파일 | 대상 | 용도 |
|---|---|---|
| `START-HERE.md` | 전원 | 지금 보고 있는 시작 안내 |
| `guide/LAB-GUIDE.md` | 참가자 | 단계별 실습 가이드(본문) |
| `guide/PROMPTS.md` | 참가자 | 복사-붙여넣기용 Copilot 프롬프트 모음 |
| `guide/CHEATSHEET.md` | 참가자 | 개념-명령어-VS Code 화면 대응표 |
| `guide/FACILITATOR-GUIDE.md` | 진행자 | 시간표, 진행 멘트, 체크포인트, 문제 해결 |
| `.github/copilot-instructions.md` | 자동 적용 | Copilot이 "초보자용 Git 튜터"로 답하도록 하는 지침 |
| `.gitignore` | 자동 적용 | 안내 문서(guide, START-HERE)를 실습 이력에서 제외 |

## 3. 사전 준비물

- Visual Studio Code 최신 버전
- Git (설치 확인: VS Code 터미널에서 `git --version`)
- GitHub 계정 + GitHub Copilot 사용 권한 (Free 플랜 포함)
- (선택) Lab 5 실습 시 GitHub에 비공개 저장소를 만들 수 있는 권한

## 4. 학습 목표

- 저장소(Repository), 스테이징(Staging), 커밋(Commit), 브랜치(Branch), 원격(Remote)을 자신의 말로 설명한다.
- Copilot 채팅으로 Git 명령을 실행하고, 그 결과를 VS Code Source Control 화면에서 검증한다.
- 실수했을 때 이력을 해치지 않고 안전하게 되돌리는 방법(revert)을 안다.
