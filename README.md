# Decap CMS + Hugo + Docsy Theme Boilerplate

Rust 언어 기반 Hugo SSG Framework의 Docsy Theme을 사용하며, Decap CMS를 통해 브라우저에서 콘텐츠를 관리할 수 있는 멀티-북 라이브러리 보일러플레이트입니다.

## 🚀 빠른 시작 (Quick Start)

### 1. 저장소 준비
이 저장소를 **Fork** 하거나 **Clone** 하세요.
```bash
git clone <your-repo-url>
cd decapcms-hugo-netlify
npm install
```

### 2. Netlify 배포
1. [Netlify](https://www.netlify.com/)에 로그인하고 'Add new site' > 'Import an existing project'를 선택합니다.
2. 사용자의 GitHub 저장소를 연결합니다.
3. 빌드 설정은 자동으로 감지됩니다 (`netlify.toml` 참조).

### 3. CMS 설정 (중요)
Netlify 배포 후 다음 설정을 완료해야 관리자 페이지 접근이 가능합니다.

1. **Identity 활성화**:
   - Netlify CMS 대시보드에서 **'Site configuration' > 'Identity' > 'Enable Identity'** 클릭.
2. **Git Gateway 활성화**:
   - 'Identity' > 'Services' > 'Git Gateway' > 'Enable Git Gateway' 클릭.
3. **사용자 초대**:
   - 'Identity' > 'Invite users' 를 통해 관리자 이메일을 초대하고 승인합니다.

### 4. 관리자 접속
배포된 사이트 주소 뒤에 `/admin/`을 붙여 접속하세요. (예: `https://your-site.netlify.app/admin/`)

## 📂 CMS 관리 메뉴 가이드

관리자 페이지 접속 시 왼쪽 사이드바에서 다음 메뉴를 확인하실 수 있습니다:

- **Main Website**: 메인 홈페이지(`content/_index.md`)의 제목과 본문 내용을 직접 수정합니다.
- **Library (Books & Chapters)**: 
  - **계층형 트리 구조**: 도서 폴더(예: `book-1`)를 클릭하여 내부의 소개글과 챕터들을 관리합니다.
  - **Books**: 폴더 내의 `_index.md` 파일을 수정하여 도서 소개를 작성합니다.
  - **Chapters**: 도서 내부의 각 장(`chapter-*.md`)을 작성하고 `weight` 값을 통해 정렬 순서를 조정합니다.

## 🏗 프로젝트 특장점

- **커스텀 홈 레이아웃**: 메인 페이지에서 관리자가 작성한 본문과 등록된 도서 목록이 자동으로 렌더링되도록 `layouts/index.html`이 개선되어 있습니다.
- **테마 내재화(Vendoring)**: Docsy 테마를 서브모듈이 아닌 프로젝트 내부 파일로 직접 관리하여 Netlify 빌드 안정성을 높였습니다.
- **Netlify 최적화**: 별도의 추가 설정 없이 `netlify.toml` 기반으로 즉시 빌드 및 배포가 가능합니다.

## 🛠 로컬 개발
```bash
npm start # 또는 hugo server
```
로컬 서버 실행 후 `http://localhost:1313`에서 확인 가능합니다.

---
**Tip**: 빌드가 꼬인 것처럼 보일 때는 Netlify 대시보드에서 **'Trigger deploy' > 'Clear cache and deploy site'**를 실행해 주세요.
