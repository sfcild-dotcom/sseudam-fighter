# 쓰담파이터 홈페이지

마누스(Manus)로 처음 제작된 후, GitHub Pages에서 독립적으로(마누스 구독 없이) 운영할 수
있도록 정리한 버전입니다.

## 로컬에서 미리보기

```bash
npm install
npm run dev
```

## 빌드

```bash
npm run build
```

빌드 결과물은 `docs/` 폴더에 생성됩니다 (GitHub Pages가 이 폴더를 바로 읽을 수 있어요).

## GitHub Pages 배포

1. 이 폴더를 GitHub 저장소에 push
2. 저장소 Settings → Pages → Source를 "Deploy from a branch"로 설정
3. Branch: `main` (또는 사용 중인 브랜치), 폴더: `/docs` 선택 후 저장
4. 몇 분 후 `https://<username>.github.io/<repo>/`에서 접속 가능
5. 커스텀 도메인(fighterclean.cloud)을 계속 쓰려면 같은 Pages 설정 화면에서
   "Custom domain"에 입력 — 도메인 등록업체(가비아 등)에서 CNAME/A 레코드를
   GitHub Pages로 연결해야 합니다.

## 참고: 원래 있던 관리자 갤러리 기능

원본 마누스 버전에는 로그인 후 갤러리 사진을 올리고 관리하는 관리자 페이지가
있었지만, 이 기능은 마누스 서버(로그인, 데이터베이스, 이미지 스토리지)에
의존하고 있어서 이번 정적 사이트 버전에서는 제외했습니다. 대신 실제 작업
사진은 `client/public/images/`에 고정된 파일로 들어가 있고, 코드
(`client/src/pages/Gallery.tsx`)에서 직접 항목을 추가·수정할 수 있습니다.

## 로고

`client/public/images/sseudam_logo.png`가 실제 로고 파일입니다 (마누스에서 받은
원본을 웹용으로 480px 크기로 최적화했어요). 나중에 로고를 새로 바꾸고 싶으시면
같은 파일명으로 덮어쓰거나, `client/src/components/Layout.tsx`와
`client/src/pages/SimpleLanding.tsx`의 `LOGO_URL` 경로를 새 파일명으로 바꿔주세요.
