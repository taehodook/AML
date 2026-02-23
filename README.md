# TPAC 자금세탁방지 퀴즈 웹사이트

TPAC(자금세탁방지업무능력) 시험 대비 온라인 퀴즈 플랫폼입니다.

## 📋 기능

- **회원 모드**: 퀴즈 풀기, 틀린 문제 해설 확인, 랭킹 보기
- **관리자 모드**: 문제 추가/편집/삭제, JSON 파일로 문제 업로드, 회원 관리
- **50문제**: TPAC 제도편(1권) + 실무편(2권) 기반 문제
- **랭킹 시스템**: 회원 간 최고 점수 경쟁

## 🚀 GitHub Pages 배포 방법

### 1. GitHub 저장소 생성
```bash
git init
git add .
git commit -m "Initial commit: TPAC Quiz Website"
git branch -M main
git remote add origin https://github.com/[username]/[repo-name].git
git push -u origin main
```

### 2. GitHub Pages 설정
1. GitHub 저장소 → Settings → Pages
2. Source: `Deploy from a branch`
3. Branch: `main`, Folder: `/ (root)`
4. Save 클릭

### 3. 접속
`https://[username].github.io/[repo-name]` 으로 접속

## 🔐 계정 정보

- **관리자 비밀번호**: `tpac@admin2024`
- **회원**: 사이트에서 직접 회원가입

> ⚠️ 모든 데이터는 브라우저 localStorage에 저장됩니다.
> 같은 기기/브라우저에서만 데이터가 유지됩니다.

## 📁 파일 구조

```
index.html     - 메인 웹사이트 (단일 페이지)
quizdata.js    - 퀴즈 문제 데이터 (50문제)
README.md      - 배포 가이드
```

## 📝 문제 업로드 형식 (JSON)

```json
[
  {
    "id": 1,
    "question": "문제 내용",
    "options": ["①선택지", "②선택지", "③선택지", "④선택지", "⑤선택지"],
    "answer": 0,
    "explanation": "해설 내용",
    "source": "출처: 제도편(1권) XX페이지"
  }
]
```
- `answer`: 0부터 시작 (①=0, ②=1, ③=2, ④=3, ⑤=4)

## 🛠 기술 스택

- **순수 HTML/CSS/JavaScript** - 외부 백엔드 없음
- **localStorage** - 브라우저 내 데이터 저장
- **Web Crypto API** - 비밀번호 해싱
- **Google Fonts** - Noto Sans KR, Space Mono
