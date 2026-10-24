# 개인 블로그

Hexo 기반 공개 블로그. 목표 주소: https://gandarf.github.io/techy.github.io/
GitHub 저장소: https://github.com/gandarf/techy.github.io
공개하려면 저장소 Settings → Pages → Source를 GitHub Actions로 설정합니다. 기본 Hello World 글은 Hexo 샘플입니다.

## 로컬 사용

Node.js 22에서 이 폴더를 열고 실행합니다.

```sh
npm ci
npm run server
```

미리보기: http://localhost:4000

```sh
npx hexo new "글 제목"
npm run build
```

공개 글은 `source/_posts/`에 둡니다. 개인 일기는 Notion 개인 공간에 작성합니다.
공개 저장소에는 초안 파일도 보이므로 비공개 일기를 저장하지 않습니다.

## GitHub Pages 연결

1. GitHub의 `gandarf/techy.github.io` 공개 저장소를 사용합니다.
2. 이 `blog` 폴더의 내용 자체를 저장소 루트로 올립니다. CMS 폴더 전체를 올리지 않습니다.
3. 기본 브랜치는 `main`으로 설정합니다.
4. Settings → Pages → Source를 GitHub Actions로 설정합니다.
5. Actions의 Publish blog 워크플로를 실행합니다. 이후 main 업데이트 시 자동 배포됩니다.

## 나중에 독립 도메인 연결

1. 원하는 도메인을 확보합니다. 등록·갱신 비용은 별도입니다.
2. GitHub Pages 설정에서 도메인을 연결하고 GitHub 공식 안내에 따라 DNS를 설정합니다.
3. `_config.yml`의 `url`을 새 HTTPS 주소로 바꾸고 `root`를 `/`로 바꿉니다.
4. `source/CNAME` 파일에 도메인 이름만 한 줄로 적습니다.
5. 다시 배포하고 HTTPS 및 기존 링크의 동작을 확인합니다.

글의 permalink 구조는 유지합니다.

공식 안내: https://hexo.io/docs/github-pages
