# Docsy + Decap CMS + Hugo Boilerplate

이 프로젝트는 Hugo의 Docsy 테마를 사용하며, Decap CMS를 통해 브라우저에서 편리하게 콘텐츠를 관리할 수 있는 멀티-북 라이브러리 보일러플레이트입니다.

## 🚀 빠른 시작 (Quick Start)

### 1. 저장소 준비
이 저장소를 **Fork** 하거나 **Clone** 하세요.
```bash
git clone <your-repo-url>
cd decapcms-hugo-netlify
npm install
```

### 2. Netlify 배포
1. [Netlify](https://www.netlify.com/)에 로그인하고 **'Add new site' > 'Import an existing project'**를 선택합니다.
2. 사용자의 GitHub 저장소를 연결합니다.
3. 빌드 설정은 자동으로 감지됩니다 (`netlify.toml` 참조).

### 3. CMS 설정 (중요)
Netlify 배포 후 다음 설정을 완료해야 관리자 페이지 접근이 가능합니다.

1. **Identity 활성화**:
   - Netlify CMS 대시보드에서 **'Site configuration' > 'Identity' > 'Enable Identity'** 클릭.
2. **Git Gateway 활성화**:
   - 'Identity' > 'Services' > 'Git Gateway' > 'Enable Git Gateway' 클릭.
3. **사용자 초대**:
   - 'Identity' > 'Invite users'를 통해 관리자 이메일을 초대하고 승인합니다.

### 4. 관리자 접속
배포된 사이트 주소 뒤에 `/admin/`을 붙여 접속하세요. (예: `https://your-site.netlify.app/admin/`)

## 📂 폴더 구조 및 콘텐츠 추가

- `content/book-n/`: 각 도서의 폴더입니다.
- `_index.md`: 도서의 소개 페이지 (CMS의 'Books' 컬렉션에서 수정).
- `chapter-n.md`: 도서 내부의 각 장 (CMS의 'Chapters' 컬렉션에서 수정).

## 🛠 로컬 개발
```bash
npm start # 또는 hugo server
```
로컬 서버 실행 후 `http://localhost:1313`에서 확인 가능합니다.
