# Git 첫걸음 워크샵 키트

> 명령어를 몰라도 괜찮아요. VS Code의 **GitHub Copilot 채팅**이 옆에서 알려주는 **60분 Git 입문 실습**입니다.

## 이런 분께 추천해요

- Git이라는 말은 들어봤지만 한 번도 써본 적이 없는 분
- 터미널 명령어가 낯설고 무서운 분
- "커밋", "브랜치"가 정확히 뭔지 궁금한 분

## 무엇을 배우나요?

| 배우는 것 | 쉬운 비유 |
|---|---|
| 저장소 (Repository) | 모든 버전이 보관되는 문서함 |
| 스테이징 (Staging) | 결제 전 장바구니 |
| 커밋 (Commit) | 게임의 세이브 포인트 |
| 브랜치 (Branch) | 원본은 두고 사본에서 써보는 초안 |
| 원격 (Remote) | 팀이 함께 쓰는 공유 드라이브 |

실수했을 때 이력을 지우지 않고 **안전하게 되돌리는 방법(revert)** 도 함께 익힙니다.

## 준비물

- [Visual Studio Code](https://code.visualstudio.com/) 최신 버전
- [Git](https://github.com/git-guides/install-git) (설치 확인: VS Code 터미널에서 `git --version`)
- GitHub 계정 + GitHub Copilot 사용 권한 (Free 플랜 포함)

## 시작하는 3단계

1. **내려받기**: 이 페이지 위쪽의 초록색 **Code** 버튼 > **Download ZIP** 을 눌러 원하는 위치(예: 바탕화면)에 압축을 풉니다.
2. **열기**: VS Code에서 **File > Open Folder...** 로 압축 푼 폴더를 열고, 신뢰 여부를 물으면 **Trust** 를 선택합니다.
3. **따라 하기**: [`guide/LAB-GUIDE.md`](guide/LAB-GUIDE.md) 를 열고 Step 0부터 순서대로 진행합니다.

## 실습 진행 방식

각 단계는 같은 순서로 구성되어 있어요.

1. **개념** 읽기 (한 가지씩만)
2. **프롬프트 복사** 후 Copilot 채팅에 붙여넣기
3. **VS Code 화면에서 결과 확인** (Source Control 보기: `Ctrl+Shift+G`)
4. (선택) 같은 작업을 터미널 명령으로 직접 해보기

> Copilot이 명령 실행 전에 "승인(Allow)"을 물으면, 표시된 명령을 한 번 읽고 승인하세요. 읽고 이해하는 것 자체가 학습입니다.

## 60분 시간표

| 구간 | 시간 | 내용 |
|---|---|---|
| Step 0 | 5분 | 준비 확인 |
| Step 1 | 10분 | 핵심 개념 5가지 |
| Lab 1 | 8분 | 저장소 만들기 |
| Lab 2 | 10분 | 첫 커밋 |
| Lab 3 | 10분 | 브랜치와 병합 |
| Lab 4 | 7분 | 이력 보기와 안전하게 되돌리기 |
| Lab 5 | 7분 | GitHub에 올리기 (선택) |
| 정리 | 3분 | 퀴즈로 복습 |

## 문서 안내

| 문서 | 용도 |
|---|---|
| [START-HERE.md](START-HERE.md) | 키트 전체 안내 |
| [guide/LAB-GUIDE.md](guide/LAB-GUIDE.md) | 단계별 실습 가이드 (본문) |
| [guide/PROMPTS.md](guide/PROMPTS.md) | 복사해서 붙여넣는 Copilot 프롬프트 모음 |
| [guide/CHEATSHEET.md](guide/CHEATSHEET.md) | 개념, 명령어, VS Code 화면 대응표 |
| [guide/FACILITATOR-GUIDE.md](guide/FACILITATOR-GUIDE.md) | 진행자용 (시간표, 멘트, 문제 해결) |

> 참고: 실습 중 Source Control 화면에 `README.md` 가 함께 보일 수 있어요. GitHub 첫 화면용 파일이니 신경 쓰지 않아도 됩니다.

## 더 알아보기

- [GitHub Git Guides](https://github.com/git-guides)
- [VS Code 소스 제어 문서](https://code.visualstudio.com/docs/sourcecontrol/overview)
