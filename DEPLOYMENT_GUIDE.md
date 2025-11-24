# 🚀 GitHub Pages 배포 가이드

## 단계별 진행 방법

### ✅ 현재 완료된 작업
- [x] 포트폴리오 웹사이트 생성 (index.html)
- [x] 4개 프로젝트 페이지 생성 (project1-4.html)
- [x] Git 저장소 초기화 및 커밋 완료
- [x] README 및 설명서 작성

### 📋 이제 할 일

#### 1단계: GitHub 저장소 생성 (GitHub 웹사이트에서)

1. **GitHub 로그인**
   - https://github.com 접속
   - 계정으로 로그인

2. **새 저장소 만들기**
   - 오른쪽 상단 `+` 버튼 클릭
   - `New repository` 선택

3. **저장소 설정**
   ```
   Repository name: p5-portfolio
   Description: P5.js 작품 포트폴리오 - 숭실대학교 과제
   ✓ Public (반드시 Public으로 설정!)
   ☐ Add a README file (체크 안 함)
   ☐ Add .gitignore (체크 안 함)
   ☐ Choose a license (체크 안 함)
   ```
   - **Create repository** 클릭

#### 2단계: 로컬 저장소와 GitHub 연결 (터미널에서)

저장소 생성 후 나오는 명령어를 사용하되, 아래 명령어를 복사하여 실행:

```bash
# GitHub username 입력 필요 (YOUR_USERNAME을 본인 GitHub 아이디로 변경)
git remote add origin https://github.com/YOUR_USERNAME/p5-portfolio.git

# main 브랜치로 푸시
git push -u origin main
```

**예시:**
```bash
# 만약 GitHub 아이디가 'wondoll'이면:
git remote add origin https://github.com/wondoll/p5-portfolio.git
git push -u origin main
```

**인증 방법:**
- **Personal Access Token 사용 (권장)**
  1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
  2. Generate new token (classic)
  3. repo 권한 체크
  4. 생성된 토큰을 복사 (한 번만 보임!)
  5. git push 시 비밀번호 대신 토큰 입력

#### 3단계: GitHub Pages 활성화 (GitHub 웹사이트에서)

1. **저장소 페이지로 이동**
   - https://github.com/YOUR_USERNAME/p5-portfolio

2. **Settings 메뉴**
   - 저장소 상단의 `Settings` 탭 클릭

3. **Pages 설정**
   - 왼쪽 메뉴에서 `Pages` 클릭
   - **Source** 섹션에서:
     - Branch: `main` 선택
     - Folder: `/ (root)` 선택
   - `Save` 버튼 클릭

4. **배포 대기**
   - 1-2분 정도 기다리면 자동 배포
   - 페이지 새로고침하면 배포 URL 표시됨

#### 4단계: 배포 확인 및 제출

1. **URL 확인**
   ```
   https://YOUR_USERNAME.github.io/p5-portfolio/
   ```

2. **작동 확인**
   - 웹사이트가 정상적으로 로드되는지 확인
   - 4개 프로젝트 모두 작동하는지 확인
   - 레이아웃이 올바른지 확인 (1,4 / 2,3 배치)

3. **LMS 제출**
   - 위 URL을 복사하여 LMS 과제 제출란에 입력
   - 제출 완료!

---

## 🔧 문제 해결 (Troubleshooting)

### 문제 1: git push가 안 됨
```bash
# 원인: 인증 실패
# 해결: Personal Access Token 생성 후 사용
# Settings → Developer settings → Personal access tokens
```

### 문제 2: GitHub Pages가 404 에러
```bash
# 원인: 배포가 아직 진행 중이거나 설정 오류
# 해결:
# 1. 1-2분 더 기다리기
# 2. Settings → Pages에서 Branch가 'main', Folder가 '/ (root)'인지 확인
# 3. Actions 탭에서 배포 진행 상황 확인
```

### 문제 3: 프로젝트가 안 보임
```bash
# 원인: iframe 경로 문제 또는 파일 누락
# 해결:
# 1. 브라우저 개발자 도구 (F12) 열어서 Console 확인
# 2. 모든 project1-4.html 파일이 제대로 업로드되었는지 확인
# 3. 캐시 지우고 새로고침 (Ctrl+Shift+R 또는 Cmd+Shift+R)
```

---

## 📱 추가 정보

### 레이아웃 구성
```
┌─────────────┬─────────────┐
│   과제 1    │   과제 4    │
│  (정적)     │ (애니메이션) │
├─────────────┼─────────────┤
│   과제 2    │   과제 3    │
│  (정적)     │(인터랙티브) │
└─────────────┴─────────────┘
```

### 사용된 기술
- **P5.js CDN**: https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.7.0/p5.min.js
- **반응형 디자인**: CSS Grid, Media Queries
- **GitHub Pages**: 무료 정적 웹 호스팅

### 유용한 링크
- **P5.js 공식 문서**: https://p5js.org/reference/
- **GitHub Pages 가이드**: https://pages.github.com/
- **Git 기초 가이드**: https://git-scm.com/book/ko/v2

---

## ✨ 완성 예시 URL

배포 완료 후 다음과 같은 형식의 URL을 받게 됩니다:

```
https://wondoll.github.io/p5-portfolio/
```

이 URL을 LMS에 제출하면 과제 완료! 🎉

---

**작성일**: 2024-11-24
**작성자**: Claude Code AI Assistant