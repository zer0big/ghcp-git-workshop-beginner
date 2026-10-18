# Git 한 장 요약 (개념 - 명령 - VS Code 화면)

| 하고 싶은 일 | 명령어 | VS Code 화면 | 근거 (Git Guides) |
|---|---|---|---|
| 설치 확인 | `git --version` | Terminal > New Terminal | [install-git](https://github.com/git-guides/install-git) |
| 작성자 설정 | `git config --global user.name "이름"` / `user.email` | (터미널) | [VS Code Quickstart](https://code.visualstudio.com/docs/sourcecontrol/quickstart) |
| 폴더를 저장소로 | `git init -b main` | Source Control > Initialize Repository | [git-init](https://github.com/git-guides/git-init) |
| 상태 확인 | `git status` | Source Control의 Changes / Staged Changes | [git-status](https://github.com/git-guides/git-status) |
| 커밋할 변경 고르기 | `git add 파일명` | 파일 옆 + (Stage Changes) | [git-add](https://github.com/git-guides/git-add) |
| 스테이징 취소 | `git restore --staged 파일명` | 파일 옆 - (Unstage Changes) | [VS Code Staging](https://code.visualstudio.com/docs/sourcecontrol/staging-commits) |
| 저장 지점 만들기 | `git commit -m "메시지"` | 메시지 입력 후 Commit (반짝이 아이콘으로 메시지 생성 가능) | [git-commit](https://github.com/git-guides/git-commit) |
| 이력 보기 | `git log --oneline --graph --all` | Source Control Graph | [git-guides](https://github.com/git-guides) |
| 브랜치 만들고 이동 | `git checkout -b 이름` | Git: Create Branch... / 상태 표시줄 브랜치명 클릭 | [git-guides](https://github.com/git-guides) |
| 브랜치 이동 | `git checkout 이름` | 상태 표시줄 브랜치명 클릭 | [git-guides](https://github.com/git-guides) |
| 병합 | `git merge 이름` (main에서 실행) | Git: Merge... | [git-guides](https://github.com/git-guides) |
| 안전하게 되돌리기 | `git revert 커밋ID` | (터미널) | [git-commit](https://github.com/git-guides/git-commit) |
| 원격 확인 | `git remote -v` | Source Control > ... > Remotes | [git-remote](https://github.com/git-guides/git-remote) |
| GitHub에 새로 게시 | (VS Code 기능) | 명령 팔레트 > Publish to GitHub | [VS Code Remotes](https://code.visualstudio.com/docs/sourcecontrol/repos-remotes) |
| 업로드 | `git push` | Source Control > ... > Push | [git-push](https://github.com/git-guides/git-push) |
| 내려받아 합치기 | `git pull` | Source Control > ... > Pull | [git-pull](https://github.com/git-guides/git-pull) |
| 기존 저장소 복제 | `git clone URL` | Git: Clone | [git-clone](https://github.com/git-guides/git-clone) |

## 파일 상태 표시
- **U** Untracked: Git이 아직 추적하지 않는 새 파일
- **M** Modified: 추적 중인 파일이 수정됨
- **D** Deleted: 추적 중인 파일이 삭제됨

## 기억할 4가지
1. 저장(Save)은 커밋이 아니다. 커밋해야 이력에 남는다.
2. 커밋은 내 PC에만 있다. push해야 GitHub에 올라간다.
3. 작업은 브랜치에서, 완료되면 main에 병합한다.
4. 공유된 커밋은 revert로 되돌린다. force push와 reset --hard는 쓰지 않는다.
