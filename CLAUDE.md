# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## 📍 프로젝트 개요

**웹 이력서 (Developer Portfolio Website)** - HTML, CSS, JavaScript를 사용한 반응형 개발자 포트폴리오 웹사이트 프로젝트입니다.

### 프로젝트 목표
- 프로페셔널한 웹 이력서 구축
- 데스크톱 & 모바일 반응형 디자인
- 인터랙티브한 사용자 경험 제공

---

## 🗂️ 프로젝트 구조

```
.
├── index.html              # 메인 HTML 파일
├── styles/
│   └── style.css          # 통합 스타일 시트
├── scripts/
│   └── main.js            # 주요 JavaScript 로직
├── assets/
│   ├── images/            # 프로필 사진, 프로젝트 이미지
│   └── icons/             # SVG 아이콘
├── ROADMAP.md             # 개발 로드맵
└── CLAUDE.md              # 이 파일
```

### 핵심 파일 설명

| 파일 | 용도 |
|------|------|
| `index.html` | 이력서 구조 (헤더, 경력, 기술, 프로젝트, 교육, 푸터) |
| `styles/style.css` | 반응형 디자인 (Flexbox/Grid, 미디어 쿼리) |
| `scripts/main.js` | 상호작용 기능 (메뉴, 테마, 부드러운 스크롤) |

---

## 🚀 개발 명령어

현재 프로젝트는 빌드 도구 없이 순수 HTML/CSS/JavaScript를 사용합니다.

### 로컬 개발 서버 실행
```bash
# Python 3 사용
python3 -m http.server 8000

# 또는 Node.js http-server 사용
npx http-server -p 8000
```

브라우저에서 `http://localhost:8000` 접속

### 파일 구조 생성 (처음 시작할 때)
```bash
# 프로젝트 폴더 구조 생성
mkdir -p assets/images assets/icons styles scripts
```

---

## 🎨 개발 가이드

### HTML 개발
- 시맨틱 HTML5 태그 사용 (header, nav, section, article, footer)
- 접근성(a11y)을 고려한 마크업
- 각 섹션은 `<section>` 태그로 구분

### CSS 개발
- CSS3 Flexbox/Grid 레이아웃 사용
- 반응형 디자인: 모바일-퍼스트 접근
- 미디어 쿼리 breakpoint:
  - 모바일: 320px ~ 767px
  - 태블릿: 768px ~ 1199px
  - 데스크톱: 1200px+
- 애니메이션은 `transition` 또는 `@keyframes` 사용
- CSS 변수로 색상, 폰트 크기 관리

### JavaScript 개발
- Vanilla JavaScript (ES6+)
- DOM 조작 최소화, 이벤트 위임 활용
- 주요 기능:
  - 부드러운 스크롤 네비게이션
  - 모바일 메뉴 토글
  - 라이트/다크 모드 전환
  - PDF 다운로드

---

## 📱 테스트 및 배포

### 브라우저 호환성 테스트
```
✓ Chrome (최신)
✓ Firefox (최신)
✓ Safari (최신)
✓ Edge (최신)
```

### 성능 최적화
- 이미지 압축 (WebP 권장)
- CSS/JS 최소화 (배포 전)
- Lazy loading 이미지 (선택사항)

### 배포 옵션
- **GitHub Pages**: 무료, GitHub 저장소 필요
- **Netlify**: 무료, 지속적 배포 지원
- **Vercel**: 무료, 정적 호스팅

---

## 🔄 언어 및 커뮤니케이션 규칙

### 기본 응답 언어
- **기본 응답 언어**: 한국어

### 코드 작성 규칙
- **코드 주석**: 한국어로 작성
- **커밋 메시지**: 한국어로 작성
- **문서화**: 한국어로 작성
- **변수명/함수명**: 영어 (코드 표준 준수)

### 예시
```javascript
// 사용자의 테마 선택 상태 저장
function toggleTheme() {
  const currentTheme = localStorage.getItem('theme');
  const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
  localStorage.setItem('theme', newTheme);
}
```

```html
<!-- 프로필 섹션 -->
<section id="profile" class="profile">
  <h1>이름</h1>
</section>
```

---

## 📋 개발 체크리스트 (ROADMAP.md 참고)

개발 단계별 진행 상황은 **ROADMAP.md** 파일에서 추적합니다.

- Phase 1: 프로젝트 설정
- Phase 2: HTML 구조 및 콘텐츠
- Phase 3: CSS 스타일링
- Phase 4: JavaScript 기능
- Phase 5: 반응형 테스트
- Phase 6: 배포 & 최적화
- Phase 7: 유지보수

---

## 🔗 유용한 도구 & 리소스

- [MDN Web Docs](https://developer.mozilla.org/) - HTML/CSS/JavaScript 레퍼런스
- [Can I Use](https://caniuse.com/) - 브라우저 호환성 확인
- [DevTools](https://developer.chrome.com/docs/devtools/) - 브라우저 개발자 도구
- [TinyPNG](https://tinypng.com/) - 이미지 압축

---

## ✅ 주의사항

1. **라이브 서버 필요**: 로컬에서 `file://` 프로토콜로 열면 일부 JavaScript 기능이 작동하지 않을 수 있음
2. **CORS 이슈**: 외부 API 호출 시 CORS 설정 필수
3. **성능**: 대용량 이미지는 반드시 최적화 후 사용
4. **SEO**: 배포 전 메타 데이터와 구조화된 데이터 검토

---

**Last Updated**: 2026-07-05
