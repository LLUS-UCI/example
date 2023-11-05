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


