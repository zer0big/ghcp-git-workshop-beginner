# 참가자 실습 가이드 (60분)

각 단계는 동일한 구조로 되어 있다.

- **개념**: 이 단계에서 이해할 한 가지 (근거: GitHub Git Guides)
- **Copilot에 붙여넣기**: 프롬프트를 그대로 복사해 Copilot 채팅에 붙여넣는다.
- **화면에서 확인**: Copilot이 한 일을 VS Code 화면으로 직접 검증한다.
- **직접 해보기(선택)**: 같은 작업을 터미널 명령으로 해본다.

> 핵심 원칙: Copilot이 명령을 실행하기 전 "승인(Allow)"을 요청하면, 표시된 명령을 한 번 읽고 승인한다. 읽고 이해하는 것 자체가 학습이다.

---

## 시간표

| 구간 | 시간 | 내용 |
|---|---|---|
| Step 0 | 5분 | 준비 확인 (Git, Copilot, 사용자 정보) |
| Step 1 | 10분 | 핵심 개념 5가지 |
| Lab 1 | 8분 | 저장소 만들기 (init, status) |
| Lab 2 | 10분 | 첫 커밋 (add, commit) |
| Lab 3 | 10분 | 브랜치와 병합 (branch, merge) |
| Lab 4 | 7분 | 이력 보기와 안전하게 되돌리기 (log, revert) |
| Lab 5 | 7분 | GitHub에 올리기 (remote, push, pull) - 선택 |
| 정리 | 3분 | 퀴즈로 복습 |

---

## Step 0. 준비 확인 (5분)

1. VS Code에서 이 키트 폴더가 열려 있는지 확인한다.
2. Copilot 채팅(Chat 보기)을 연다. 로그인을 요구하면 GitHub 계정으로 로그인한다.
3. 채팅 입력창 아래에서 에이전트를 **Agent** 로 선택한다. 권한(permissions)은 기본값 **Manual permissions** 그대로 둔다.
   - Manual permissions: 자동 승인되지 않은 작업은 실행 전에 사용자 확인을 받는다.
4. 아래 프롬프트를 붙여넣는다.

**Copilot에 붙여넣기**
```
Git이 설치되어 있는지 확인해줘. 그리고 Git에 내 이름(user.name)과 이메일(user.email)이 설정되어 있는지도 확인해줘. 설정이 안 되어 있으면 내가 어떤 값을 알려줘야 하는지 물어봐줘. 명령을 실행하기 전에 무슨 명령인지 한 줄로 먼저 설명해줘.
```

**화면에서 확인**
- Copilot 응답에 Git 버전 번호가 표시된다.
- 이름/이메일이 비어 있다면 Copilot이 값을 물어본다. 본인 이름과 이메일을 알려주면 설정해준다.

**직접 해보기(선택)** — 메뉴 **Terminal > New Terminal**
```
git --version
git config --global user.name "홍길동"
git config --global user.email "you@example.com"
```
> 이름과 이메일은 커밋의 "작성자"로 기록되는 값이며, 로그인 정보가 아니다.

---

## Step 1. 핵심 개념 5가지 (10분)

| 개념 | 한 줄 정의 | 일상 비유 |
|---|---|---|
| 저장소 (Repository) | 프로젝트 파일과 그 전체 변경 이력을 담는 공간 | 버전이 모두 보관되는 문서함 |
| 스테이징 (Staging) | 다음 커밋에 넣을 변경을 골라 담는 단계 | 결제 전 장바구니 |
| 커밋 (Commit) | 특정 시점의 저장소 스냅샷(저장 지점) | 게임의 세이브 포인트 |
| 브랜치 (Branch) | 원본에 영향 없이 따로 작업하는 안전한 작업 줄기 | 원본을 둔 채 사본에서 초안 작성 |
| 원격 (Remote) | GitHub처럼 다른 곳에 있는 공유 저장소 | 팀 공유 드라이브 |

> 흐름 정리: 파일 수정(저장) → 스테이징(add) → 커밋(commit) → 업로드(push)
> 저장(Save)만으로는 커밋되지 않는다. 커밋은 내 PC 이력에만 남고, push해야 GitHub에 올라간다.

**Copilot에 붙여넣기**
```
GitHub Git Guides(https://github.com/git-guides)를 기준으로 Git과 GitHub의 차이를 먼저 두 줄로 설명해줘. 그리고 repository, staging area, commit, branch, remote를 비개발자도 이해할 수 있게 일상 비유를 넣어 각각 두 줄 이내로 표로 정리해줘.
```
> 웹 페이지를 가져오기 전에 URL 승인을 요청할 수 있다. 내용을 확인하고 승인한다.

---

## Lab 1. 저장소 만들기 (8분)

**개념**: `git init` 은 일반 폴더를 Git 저장소로 만든다. `git status` 는 현재 브랜치와 파일 상태를 보여주는, 가장 자주 쓰는 확인 명령이다.
근거: https://github.com/git-guides/git-init , https://github.com/git-guides/git-status

**Copilot에 붙여넣기**
```
이 폴더를 기본 브랜치 이름이 main인 Git 저장소로 만들어줘. 그 다음 git status를 실행하고 결과를 초보자 눈높이로 설명해줘. 특히 .gitignore 파일이 어떤 역할을 하는지, guide 폴더와 START-HERE.md가 왜 목록에 보이지 않는지도 알려줘.
```

**화면에서 확인**
- 왼쪽 Source Control 보기(Ctrl+Shift+G)를 연다.
- **Changes** 아래 `.gitignore`, `.github/copilot-instructions.md` 가 **U**(Untracked, 아직 추적 안 됨)로 보인다.
- 왼쪽 아래 상태 표시줄에 브랜치 이름 `main` 이 보인다.

**직접 해보기(선택)**
```
git init -b main
git status
```

---

## Lab 2. 첫 커밋 (10분)

**개념**: 커밋은 두 단계다. 먼저 `git add` 로 담을 변경을 고르고(스테이징), `git commit` 으로 저장 지점을 만든다. Git은 스테이징된 것만 커밋한다.
근거: https://github.com/git-guides/git-add , https://github.com/git-guides/git-commit

**2-1. 파일 만들기 — Copilot에 붙여넣기**
```
profile.md 파일을 만들어줘. 내용은 "# 내 소개" 제목 아래에 이름, 소속, 오늘 배우고 싶은 것 한 줄씩 넣어줘(값은 예시로 채워줘). 아직 add나 commit은 하지 말고, git status로 이 파일이 지금 어떤 상태인지만 설명해줘.
```
- profile.md를 열어 예시 값을 본인 정보로 바꾸고 저장(Ctrl+S)한다.

**2-2. 스테이징 — Copilot에 붙여넣기**
```
profile.md 파일만 스테이징해줘. 그리고 git status를 다시 보여주면서, VS Code Source Control 화면의 Changes와 Staged Changes가 각각 무엇을 뜻하는지 설명해줘.
```

**화면에서 확인**
- profile.md가 **Changes** 에서 **Staged Changes** 로 이동했다.
- `.gitignore`, `.github` 는 여전히 Changes에 남아 있다. 고른 것만 담긴다는 점을 확인한다.

**2-3. 커밋 — 아래 둘 중 하나를 선택**
- (화면) Source Control의 메시지 입력란에서 반짝이 아이콘(Generate Commit Message)을 눌러 메시지를 생성하고, 읽어본 뒤 **Commit** 을 누른다.
- (Copilot) 아래 프롬프트를 붙여넣는다.
```
스테이징된 내용을 "Add profile" 메시지로 커밋해줘. 그 다음 남아 있는 .gitignore와 .github 폴더를 스테이징해서 "Add workshop settings" 메시지로 커밋해줘. 마지막으로 git log --oneline 결과를 보여주고 각 줄이 무엇인지 설명해줘.
```

**화면에서 확인**
- Source Control 보기 아래 **Source Control Graph** 를 펼치면 커밋 2개가 보인다. 커밋을 클릭하면 포함된 파일을 볼 수 있다.

**직접 해보기(선택)**
```
git add profile.md
git status
git commit -m "Add profile"
git add .gitignore .github
git commit -m "Add workshop settings"
git log --oneline
```
> 메시지 없이 `git commit` 만 입력해 낯선 편집기(Vim)가 열리면 Esc를 누르고 `:wq` 입력 후 Enter로 빠져나온다.

---

## Lab 3. 브랜치와 병합 (10분)

**개념**: 브랜치는 main을 건드리지 않고 안전하게 작업하는 공간이다. 작업이 끝나면 main에 병합(merge)한다. 브랜치 이름은 사람보다 "목적" 기준으로 짓는다.
근거: https://github.com/git-guides (Create a branch, Merge into main)

**3-1. 브랜치에서 작업 — Copilot에 붙여넣기**
```
update-profile이라는 새 브랜치를 만들고 그 브랜치로 전환해줘. profile.md 맨 아래에 "- 자주 쓰는 업무 도구: (예시)" 한 줄을 추가하고 "Update profile with tools" 메시지로 커밋해줘. 지금 어느 브랜치에 있는지도 알려줘.
```

**3-2. main과 비교 — Copilot에 붙여넣기**
```
main 브랜치로 전환해줘. 그리고 지금 profile.md에 방금 추가한 줄이 있는지 확인하고, 왜 그렇게 보이는지 브랜치 개념으로 설명해줘.
```

**화면에서 확인**
- 상태 표시줄의 브랜치 이름이 바뀐다.
- main으로 돌아가면 profile.md에서 추가한 줄이 사라져 보인다. 삭제된 것이 아니라 다른 브랜치에 있는 것이다.

**3-3. 병합 — Copilot에 붙여넣기**
```
update-profile 브랜치를 main에 병합해줘. 병합 후 git log --oneline --graph --all 결과를 보여주고, profile.md에 추가한 줄이 이제 main에 있는지 확인해줘. 다 쓴 update-profile 브랜치는 삭제해도 되는지도 알려줘.
```

**직접 해보기(선택)**
```
git checkout -b update-profile
git add profile.md
git commit -m "Update profile with tools"
git checkout main
git merge update-profile
git log --oneline --graph --all
git branch -d update-profile
```
> VS Code 화면에서는 명령 팔레트(Ctrl+Shift+P)의 **Git: Create Branch...**, **Git: Merge...** 로도 같은 작업을 할 수 있다.

---

## Lab 4. 이력 보기와 안전하게 되돌리기 (7분)

**개념**: 커밋은 변경되지 않는 기록이다. 실수한 커밋은 지우는 대신 `git revert` 로 "반대 내용의 새 커밋"을 만들어 되돌리는 것이 가장 안전하다.
근거: https://github.com/git-guides/git-commit (How to Undo Commits in Git)

**Copilot에 붙여넣기**
```
profile.md에 "실수로 넣은 문장입니다." 한 줄을 추가하고 "Add wrong line" 메시지로 커밋해줘. 그 다음 그 커밋을 git revert로 되돌려줘. 마지막으로 git log --oneline을 보여주고, reset 대신 revert를 쓰는 이유를 GitHub Git Guides 기준으로 두 줄로 설명해줘.
```

**화면에서 확인**
- profile.md에서 잘못 넣은 문장이 사라졌다.
- Source Control Graph에 "Revert ..." 커밋이 새로 추가됐다. 이력은 지워지지 않고 남는다.

**직접 해보기(선택)**
```
git log --oneline
git revert --no-edit HEAD
```

---

## Lab 5. GitHub에 올리기 (7분, 선택)

**개념**: 원격(remote)은 다른 곳에 있는 저장소로 가는 연결 이름이며, 보통 `origin` 이다. `push` 는 내 커밋을 올리고, `pull` 은 원격의 새 커밋을 가져와 내 브랜치에 합친다.
근거: https://github.com/git-guides/git-remote , https://github.com/git-guides/git-push , https://github.com/git-guides/git-pull

**5-1. 게시 (화면 조작)**
1. 명령 팔레트(Ctrl+Shift+P)에서 **Publish to GitHub** 를 실행한다.
2. 로그인 요청 시 GitHub에 로그인한다.
3. 저장소 이름(예: `git-workshop-practice`)을 입력하고 **private** 을 선택한다.
4. 완료 후 브라우저에서 저장소를 열어 profile.md와 커밋 이력이 올라갔는지 확인한다.

**5-2. 원격 이해 — Copilot에 붙여넣기**
```
git remote -v를 실행해서 origin이 무엇을 가리키는지 설명해줘. 그리고 fetch, pull, push, Sync Changes의 차이를 표로 정리해줘.
```

**5-3. 추가 도전: pull 체험**
1. GitHub 웹에서 profile.md를 열고 연필(Edit) 아이콘으로 한 줄을 추가해 커밋한다.
2. VS Code로 돌아와 아래를 붙여넣는다.
```
GitHub에 새로 생긴 커밋을 내 PC로 가져와줘(pull). 가져오기 전후 git log --oneline을 비교해서 보여줘.
```

> push가 거부되면 force push를 쓰지 않는다. 먼저 pull로 원격 변경을 합친 뒤 다시 push한다.

---

## 정리 (3분)

**Copilot에 붙여넣기**
```
오늘 실습한 Git 개념(repository, staging, commit, branch, merge, revert, remote, push, pull)으로 객관식 퀴즈 5문항을 내줘. 한 문항씩 내고, 내가 답하면 채점하고 짧게 해설해줘.
```

**오늘의 핵심 한 줄**: 수정하고(Save) → 골라 담고(add) → 저장 지점을 만들고(commit) → 필요하면 브랜치에서 안전하게 작업하고(branch/merge) → 공유한다(push/pull).

## 더 배우기
- GitHub Git Guides: https://github.com/git-guides
- Git 치트시트: https://github.github.io/training-kit/
- VS Code 소스 제어 빠른 시작: https://code.visualstudio.com/docs/sourcecontrol/quickstart
- Microsoft Learn - Introduction to Git: https://learn.microsoft.com/training/modules/intro-to-git/
