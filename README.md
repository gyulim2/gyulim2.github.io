# 김규림 보안 포트폴리오

순수 HTML + CSS 정적 사이트입니다. 빌드 도구가 필요 없습니다.

```
index.html            # 모든 섹션 (Hero / Research / Projects / Hands-on / Skills / Contact)
assets/css/style.css  # 색상은 :root 변수, 다크모드는 prefers-color-scheme
assets/img/           # 이미지 (OG 이미지 등)
projects/             # 프로젝트 상세 페이지 (선택)
```

## 로컬 확인
```bash
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000
```

## 수정 방법
- `index.html`에서 `TODO:` 를 검색해 비어 있는 값(이메일, 링크, 수치, 날짜)을 채웁니다.
- 포인트 컬러는 `style.css` 상단 `--accent` 한 곳만 바꾸면 됩니다 (라이트/다크 각각).
- 프로젝트 카드를 추가하려면 `#projects` 안의 `<article class="card">` 블록을 복사합니다.
- 배포 후 `og:url`을 실제 주소로 바꾸고, `assets/img/og.png`(1200x630)를 추가한 뒤 주석 처리된 `og:image`를 활성화합니다.

## GitHub Pages 배포
1. GitHub에서 새 저장소를 만듭니다. 이름은 반드시 `<GitHub아이디>.github.io` (예: `gyulim2.github.io`), Public.
2. 로컬에서 연결 후 push:
   ```bash
   git remote add origin https://github.com/<GitHub아이디>/<GitHub아이디>.github.io.git
   git branch -M main
   git push -u origin main
   ```
3. 저장소 **Settings > Pages** → Source: *Deploy from a branch* → Branch: `main`, 폴더 `/ (root)` → Save.
4. 1~2분 뒤 `https://<GitHub아이디>.github.io` 에서 확인합니다.
