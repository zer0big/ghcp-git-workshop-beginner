# Copilot 프롬프트 모음 (복사-붙여넣기용)

- 사용 위치: VS Code Copilot 채팅, 에이전트 **Agent**, 권한 **Manual permissions**(기본값)
- 순서대로 하나씩 붙여넣는다. 실행 승인 요청이 나오면 명령을 읽고 승인한다.

## Step 0. 준비 확인
```
Git이 설치되어 있는지 확인해줘. 그리고 Git에 내 이름(user.name)과 이메일(user.email)이 설정되어 있는지도 확인해줘. 설정이 안 되어 있으면 내가 어떤 값을 알려줘야 하는지 물어봐줘. 명령을 실행하기 전에 무슨 명령인지 한 줄로 먼저 설명해줘.
```

## Step 1. 개념
```
GitHub Git Guides(https://github.com/git-guides)를 기준으로 Git과 GitHub의 차이를 먼저 두 줄로 설명해줘. 그리고 repository, staging area, commit, branch, remote를 비개발자도 이해할 수 있게 일상 비유를 넣어 각각 두 줄 이내로 표로 정리해줘.
```

## Lab 1. 저장소 만들기
```
이 폴더를 기본 브랜치 이름이 main인 Git 저장소로 만들어줘. 그 다음 git status를 실행하고 결과를 초보자 눈높이로 설명해줘. 특히 .gitignore 파일이 어떤 역할을 하는지, guide 폴더와 START-HERE.md가 왜 목록에 보이지 않는지도 알려줘.
```

## Lab 2. 첫 커밋
```
profile.md 파일을 만들어줘. 내용은 "# 내 소개" 제목 아래에 이름, 소속, 오늘 배우고 싶은 것 한 줄씩 넣어줘(값은 예시로 채워줘). 아직 add나 commit은 하지 말고, git status로 이 파일이 지금 어떤 상태인지만 설명해줘.
```
```
profile.md 파일만 스테이징해줘. 그리고 git status를 다시 보여주면서, VS Code Source Control 화면의 Changes와 Staged Changes가 각각 무엇을 뜻하는지 설명해줘.
```
```
스테이징된 내용을 "Add profile" 메시지로 커밋해줘. 그 다음 남아 있는 .gitignore와 .github 폴더를 스테이징해서 "Add workshop settings" 메시지로 커밋해줘. 마지막으로 git log --oneline 결과를 보여주고 각 줄이 무엇인지 설명해줘.
```

## Lab 3. 브랜치와 병합
```
update-profile이라는 새 브랜치를 만들고 그 브랜치로 전환해줘. profile.md 맨 아래에 "- 자주 쓰는 업무 도구: (예시)" 한 줄을 추가하고 "Update profile with tools" 메시지로 커밋해줘. 지금 어느 브랜치에 있는지도 알려줘.
```
```
main 브랜치로 전환해줘. 그리고 지금 profile.md에 방금 추가한 줄이 있는지 확인하고, 왜 그렇게 보이는지 브랜치 개념으로 설명해줘.
```
```
update-profile 브랜치를 main에 병합해줘. 병합 후 git log --oneline --graph --all 결과를 보여주고, profile.md에 추가한 줄이 이제 main에 있는지 확인해줘. 다 쓴 update-profile 브랜치는 삭제해도 되는지도 알려줘.
```

## Lab 4. 이력과 되돌리기
```
profile.md에 "실수로 넣은 문장입니다." 한 줄을 추가하고 "Add wrong line" 메시지로 커밋해줘. 그 다음 그 커밋을 git revert로 되돌려줘. 마지막으로 git log --oneline을 보여주고, reset 대신 revert를 쓰는 이유를 GitHub Git Guides 기준으로 두 줄로 설명해줘.
```

## Lab 5. GitHub (선택, 먼저 명령 팔레트에서 Publish to GitHub 실행)
```
git remote -v를 실행해서 origin이 무엇을 가리키는지 설명해줘. 그리고 fetch, pull, push, Sync Changes의 차이를 표로 정리해줘.
```
```
GitHub에 새로 생긴 커밋을 내 PC로 가져와줘(pull). 가져오기 전후 git log --oneline을 비교해서 보여줘.
```

## 정리 퀴즈
```
오늘 실습한 Git 개념(repository, staging, commit, branch, merge, revert, remote, push, pull)으로 객관식 퀴즈 5문항을 내줘. 한 문항씩 내고, 내가 답하면 채점하고 짧게 해설해줘.
```

## 막혔을 때 쓰는 만능 프롬프트
```
지금 Git 상태를 진단해줘. git status와 git log --oneline -5를 실행해서 내가 어느 브랜치에 있고, 커밋 안 된 변경이 무엇인지 쉽게 설명해줘. 아무것도 삭제하거나 되돌리지는 말아줘.
```
```
방금 나온 오류 메시지가 무슨 뜻인지 초보자 눈높이로 설명하고, 가장 안전한 해결 방법 하나만 제안해줘. 실행은 내가 승인한 뒤에 해줘.
```
