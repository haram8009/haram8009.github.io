---
layout: post
title: Jekyll, Github Pages
commants: true
---
## Jekyll
Ruby 기반 정적 웹사이트 생성기
>정적웹사이트(Static Webpage)
: HTML 등으로 작성된 문서를 그대로 전달해주는 것

## Github Pages
Guthub Repo를 Webpage로 만들어준다.

## Github Page 시작하기
1. `<username>.github.io`라는 이름의 Repo를 생성한다.
2. `.html`문서를 작성한다.
3. 몇 분 뒤 `<username>.github.io`에 접속하면 문서가 웹사이트로 변해있다!

## Build Jekyll Project
- 로컬 저장소에서 Jekyll을 시작한다.
```shell script
jekyll -v  # 지킬이 설치되어있는지 확인
jekyll new . --force  # 지킬 시작하기
bundle exec jekyll serve  # jekyll serve 실행
```
지킬 실행 후, `localhost:4000` 접속!

- 원격저장소에 반영
```shell script
git add *
git commit -m "add: jekyll on repository"
git push
```
`<username>.github.io`에 접속!

## 포스트 업로드
 `_posts` 폴더에 `YYYY-MM-DD-TITLE.md`형태로 문서를 작성한다.
 머릿말의 layout을 post로 선택하면 `_layouts` 폴더 하위의 `post.html`을 이용해 페이지가 생성된다.
```markdown
---
layout: post
title: "title"
~메타정보는 사용하는 블로그 테마에 따라 다르게 작성할 수 있다.~
---
```
local에 `commit`으로 반영 후, remote로 `push`한다.
