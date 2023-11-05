# example
깃헙 예제 리포입니다

## Github 팀 작업 권장 사항

1. PR 은 approve 된 후에 Squash Merge로만 merge 합니다.
  - 그래야 `main` 브랜치 안에서의 커밋 역사가 일괄적으로 깨끗하게 유지가 됩니다.

2. `main` 브랜치 안에 내용이 가장 최신 릴리스 코드 버젼입니다.
  - 생각하기 쉽게 됩니다.
  - 만약 릴리스를 버젼으로 관리 하고 싶다면, [release-please](https://github.com/googleapis/release-please) 툴을 추천합니다.
    - 이렇게 하면 `main`은 Staging (실제 프로덕션이 아닌 임시 환경 - 테스트를 돌리고 등)이 되고, 릴리스 된 버젼이 production이 됩니다.
    - 아마도 프로젝트를 진행함에 있어 여기까지 신경은 안써도 되지만, 만약 CI/CD를 이제 할 단계가 온다면 제일 쉽게 릴리스 버젼을 추가할 수 있는 방법이 아닐까 합니다.

## Git 진짜로 많이 쓰는 커멘드들

- `git ci -m "commit message"`: `git ci` 하면 화면이 뜨고 거기다가 커밋 메세지 써야 하는데 그냥 터미널 상에서 내용 적기
- `git checkout -b`: create new branch
- `git stash`: 작업을 하다 팀원이 자기 PR 체크좀 해달라할때 굳이 커밋 하긴 싫고 할때 커밋 하지 않은 것들은 그냥 임시 저장 해놓음
- `git stash apply`: 마지막 stash 한 것을 다시 불러냄
- `git branch -D branch-i-am-not-on`: 확 다른 브랜치 지울때
- `git pull`: 남들이 작업하고 merge하거나 다른 브랜치들 다 업뎃 할때
- `git pull --rebase`: 만약 github UI로 코드작업을 좀 해서 커밋이 앞설 경우, 내가 로컬로 작업하는 커밋들을 가장 최근으로 놓기 위한 rebase를 pull할 때 하는거
- `git diff X..Y`: 커밋 X와 Y 의 변함
- `git add -i`: interactive add mode. 메뉴를 통해 파일 몇개만 이번 커밋에 넣고, 선택한 파일들 diff 보기 등
- `git reset --soft HEAD~1 && git reset`: 악 실수로 커밋을 했다! 이 최근 커밋을 취소하고 다시 리셋해서 `git add `이전의 상태로 돌아감

