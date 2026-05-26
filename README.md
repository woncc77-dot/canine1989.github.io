# 의상 디자이너 자기소개 사이트

`자기소개서.md` 내용을 바탕으로 한 정적 1페이지 자기소개서입니다. HTML, CSS, JavaScript만 사용하며 빌드 도구가 필요 없습니다.

## 파일 구성

| 파일 | 설명 |
|------|------|
| `index.html` | 자기소개서 6개 섹션 + Hero + 연락처 |
| `styles.css` | Adri Dark UI 다크 테마 스타일 |
| `script.js` | 스티키 헤더, 모바일 메뉴, 스크롤 reveal |
| `자기소개서.md` | 원본 Markdown (수정 후 HTML과 동기화 권장) |

## 로컬에서 보기

### 방법 1: Python HTTP 서버 (권장)

```powershell
cd f:\test7
python -m http.server 8080
```

브라우저에서 [http://localhost:8080](http://localhost:8080) 을 엽니다.

### 방법 2: Live Server

Cursor/VS Code에서 **Live Server** 확장으로 `index.html`을 연습니다.

### 인쇄 / PDF 저장

브라우저에서 `Ctrl+P` → PDF로 저장. 인쇄용 스타일이 `@media print`에 정의되어 있습니다.

## 내용 수정

1. `index.html`과 `자기소개서.md`에서 `[이름]`, `[이메일]`, `[유명 브랜드 A]` 등 플레이스홀더를 실제 정보로 교체합니다.
2. 히어로 이미지 URL을 본인 작업 사진 경로로 바꿉니다 (예: `images/hero.jpg`).

## GitHub Pages 배포

로컬에서 확인한 뒤 다음 순서로 배포합니다.

1. GitHub에서 새 저장소를 만듭니다 (예: `fashion-cover-letter`).
2. 프로젝트 폴더에서 Git 초기화 및 푸시:

```powershell
cd f:\test7
git init
git add index.html styles.css script.js 자기소개서.md README.md
git commit -m "Add static cover letter site"
git branch -M main
git remote add origin https://github.com/<USERNAME>/<REPO>.git
git push -u origin main
```

3. 저장소 **Settings → Pages**:
   - **Source**: Deploy from a branch
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. 1~2분 후 `https://<USERNAME>.github.io/<REPO>/` 에서 확인합니다.

### 참고

- 에셋은 상대 경로(`styles.css`, `script.js`)를 사용하므로 Project site 배포에 추가 설정이 필요 없습니다.
- `.cursor/` 폴더는 팀과 스킬을 공유하지 않을 경우 `.gitignore`에 넣어도 됩니다.

## 디자인

[adri-dark-ui](.cursor/skills/adri-dark-ui/SKILL.md) 스킬의 다크 테마·타이포·여백·모션 가이드를 따릅니다.
