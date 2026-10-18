# 진행자 가이드 (60분)

## 1. 운영 개요
- 대상: Git 경험이 없는 비개발자, 입문 엔지니어
- 방식: 진행자 화면 공유 + 참가자는 LAB-GUIDE의 프롬프트 복사-붙여넣기
- 원칙: Copilot이 "실행", 참가자는 "읽고 승인하고 화면에서 검증". 개념 이해가 목표이며 명령 암기는 목표가 아니다.

## 2. 사전 준비 체크리스트 (D-1)
- [ ] 참가자 PC: VS Code 최신 버전, Git 설치, `git --version` 확인
- [ ] 참가자 GitHub 계정과 Copilot 사용 가능 여부 확인 (조직 정책으로 Agent가 비활성화된 경우 대비안 숙지)
- [ ] 네트워크에서 github.com, api.github.com 접속 허용 확인
- [ ] 키트 zip 배포 및 압축 해제 위치 안내 (기존 Git 저장소 폴더 내부는 피한다)
- [ ] 진행자 리허설: 새 폴더에 키트를 풀고 LAB 전 과정 1회 수행

## 3. 시간표와 진행 멘트

| 시간 | 구간 | 진행자 핵심 멘트 / 활동 | 체크포인트 |
|---|---|---|---|
| 00-05 | Step 0 준비 | "Copilot을 Agent로, 권한은 기본값 그대로. 실행 전 승인 창이 뜨면 명령을 소리 내어 읽어보자." | 전원 Git 버전 출력, user.name/email 설정 |
| 05-15 | Step 1 개념 | 장바구니 비유로 Save → add → commit → push 흐름 설명. "저장과 커밋은 다르다"를 강조 | 참가자가 5개 개념 표를 Copilot 응답으로 확보 |
| 15-23 | Lab 1 init | Source Control 보기 열기 시연. .gitignore로 안내 문서가 제외된 이유 설명 | Changes에 U 표시 2개, 상태 표시줄 main |
| 23-33 | Lab 2 commit | "고른 것만 담긴다" 시연. 반짝이 아이콘으로 메시지 생성 시연 | Graph에 커밋 2개 |
| 33-43 | Lab 3 branch | main으로 돌아가면 줄이 "사라져 보이는" 순간을 강조 → 병합 후 다시 보임 | merge 후 main에 줄 존재 |
| 43-50 | Lab 4 revert | "지우지 않고 반대 커밋을 쌓는다". reset --hard와의 차이 한 줄 | Graph에 Revert 커밋 |
| 50-57 | Lab 5 GitHub | Publish to GitHub(private) 시연. 시간 부족 시 진행자 시연으로 대체 | 브라우저에서 저장소 확인 |
| 57-60 | 정리 | 퀴즈 프롬프트 실행, 핵심 한 줄 복창 | - |

시간 조정 우선순위: 지연 시 Lab 5를 진행자 시연으로 대체하고, 그래도 부족하면 Lab 4를 시연으로 전환한다.

## 4. 자주 발생하는 문제와 대응

| 증상 | 원인 | 대응 |
|---|---|---|
| `git` 명령을 찾을 수 없음 | Git 미설치 또는 설치 후 VS Code 미재시작 | Git 설치 후 VS Code 재시작 |
| 커밋 시 "Author identity unknown" | user.name/email 미설정 | Step 0의 git config 명령 실행 |
| 브랜치 이름이 master로 표시 | `-b main` 없이 init됨 | 그대로 진행해도 무방. 필요 시 `git branch -m main` |
| Copilot이 명령을 실행하지 않고 설명만 함 | Ask 에이전트 선택됨, 또는 조직 정책 | 에이전트를 Agent로 변경. 정책상 불가 시 Copilot이 알려준 명령을 터미널에 직접 붙여넣기 |
| 승인 창이 계속 뜸 | Manual permissions 기본 동작 | 정상. 학습 목적상 Allow all로 바꾸지 않는다 |
| 커밋 후 Vim 편집기가 열림 | `-m` 없이 git commit 실행 | Esc → `:wq` → Enter |
| main으로 전환이 거부됨 | 커밋 안 된 변경 존재 | 먼저 커밋하거나 Copilot에 상황 진단 요청 |
| push 거부(rejected) | 원격에 내가 없는 커밋 존재 | force push 금지. pull 후 다시 push |
| 키트 폴더가 상위 Git 저장소 안에 있음 | 압축 해제 위치 문제 | 바탕화면 등 일반 폴더로 옮긴 후 다시 열기 |

## 5. 안전 운영 원칙
- 권한 수준은 기본값 Manual permissions를 유지한다. Allow all과 Autopilot은 확인 없이 파일 편집, 터미널 명령을 실행하므로 입문 실습에서는 사용하지 않는다.
- `.github/copilot-instructions.md` 가 위험 명령(reset --hard, push --force, clean 등) 실행 전 확인을 요구하도록 지시한다. 단, 이는 보조 장치이므로 참가자가 승인 전 명령을 읽는 습관이 우선이다.
- Lab 5 저장소는 private으로 생성한다.

## 6. 근거 문서
- GitHub Git Guides: https://github.com/git-guides
- Git Guides - git commit: https://github.com/git-guides/git-commit
- VS Code Source Control Quickstart: https://code.visualstudio.com/docs/sourcecontrol/quickstart
- VS Code Staging and committing: https://code.visualstudio.com/docs/sourcecontrol/staging-commits
- VS Code Branches: https://code.visualstudio.com/docs/sourcecontrol/branches-worktrees
- VS Code Repositories and remotes: https://code.visualstudio.com/docs/sourcecontrol/repos-remotes
- VS Code Approvals and permissions: https://code.visualstudio.com/docs/agents/run/approvals
- VS Code Custom instructions: https://code.visualstudio.com/docs/agent-customization/custom-instructions
- Microsoft Learn - Introduction to Git: https://learn.microsoft.com/training/modules/intro-to-git/
