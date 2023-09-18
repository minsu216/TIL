# Git

## 최초설정
커밋에 기록되는 사용자 정보
```bash
git config --global user.name <name>
git config --global user.email <email>

```

## 명령어
- `git init` 현재 폴더에 git 폴더 생성
    - `.git` repository를 생성 하는 명령어
    
- `git add <file name>`
    - `working directory`에서 `staging area`로 추가함
    - 일반적으로 모든 파일, 폴더를 한번에 추가하기 위해 아래의 명령어로 작성한다.
    - `git add . `

- `git commit -m "first commit"`
    - `staging area`에 올라간 파일들의 스냅샷을 찍어 `.git directory`에 저장한다.
    - 일반적으로 -m 옵션을 넣어서 커밋메세지를 추가한다.
    - `git commit -m "message"`