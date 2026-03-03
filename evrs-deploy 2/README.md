# Evrs0024 배포 가이드

## 파일 구조
```
evrs0024/
├── index.html       ← 사이트 본체
├── vercel.json      ← Vercel 설정
├── api/
│   └── chat.js      ← API 프록시 (이게 핵심)
└── README.md
```

## 배포 순서

### 1. Anthropic API 키 발급
1. console.anthropic.com 접속
2. 로그인 → API Keys → Create Key
3. 키 복사해두기 (sk-ant-... 로 시작)

### 2. Vercel 배포
1. vercel.com 가입 (Google 계정)
2. "Add New → Project"
3. 이 폴더 전체를 드래그앤드롭
4. Deploy 클릭

### 3. API 키 환경변수 등록 (핵심!)
1. Vercel 대시보드 → 프로젝트 클릭
2. Settings → Environment Variables
3. Name: ANTHROPIC_API_KEY
4. Value: sk-ant-... (복사해둔 키)
5. Save → Redeploy

끝! 이제 상담 기능이 실제로 작동해요.
