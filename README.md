# 가위닥터 블로그

React + TypeScript + Vite로 구현한 반응형 블로그 프런트엔드입니다.

## 실행

```bash
npm install
npm run dev
```

## 프로덕션 빌드

```bash
npm run build
npm run preview
```

카테고리 필터, 제목·설명 검색, 글 상세 모달, 소개 모달, 모바일 메뉴를 지원합니다. 상세 창은 Escape로 닫을 수 있으며 키보드 포커스를 유지합니다.

게시글은 `src/main.tsx`의 `posts` 배열에서 변경할 수 있습니다. 현재 콘텐츠는 시안용 예시입니다. 서버, CMS, 로그인, 글 작성 기능은 연결되어 있지 않습니다.

사진은 Unsplash에서 가져와 `public/images`에 저장했습니다. 웹폰트는 Google Fonts에서 로드하며, 연결이 없으면 시스템 글꼴로 표시됩니다. 실제 운영 시 자체 이미지로 교체하는 것을 권장합니다.

## Vercel 배포

1. Vercel에서 **Add New → Project**를 선택합니다.
2. GitHub의 `Scissor-Doctor/blog` 저장소를 가져옵니다.
3. Framework Preset은 **Vite**, Root Directory는 저장소 루트(`.`)로 설정합니다.
4. Build Command는 `npm run build`, Output Directory는 `dist`입니다. `vercel.json`에도 선언되어 있습니다.
5. Deploy를 누르면 배포됩니다. 이후 `main`에 푸시하면 Vercel이 자동 재배포합니다.

현재 화면 배포에는 환경 변수가 필요하지 않습니다. 전화 문의는 전화 앱으로, 구매 링크는 네이버 스마트스토어로 연결됩니다. 문의 저장이나 관리자 글 작성 같은 백엔드 기능은 아직 구현하지 않았습니다. Vercel 배포 시 영구 데이터 저장은 별도의 데이터베이스 연결이 필요합니다.

메인 배너의 `public/images/dog-grooming-scissors-bright.png`는 AI로 생성한 애견 미용가위 이미지이며, 실제 판매 제품 사진이 아닙니다.

01번 글의 `public/images/dog-grooming-scissors-care.png`는 가위 관리 주제에 맞춘 AI 생성 이미지입니다.

02번 글의 `public/images/dog-grooming-inspection.png`는 반려견과 미용사의 가위 점검 모습을 담은 AI 생성 이미지입니다.

03번 글의 `public/images/dog-grooming-scissors-selection.png`는 손에 맞는 애견 미용가위를 고르는 모습을 담은 AI 생성 이미지입니다.

04번 글의 `public/images/dog-grooming-cleanup.png`는 애견 미용가위를 닦고 도구를 정리하는 모습을 담은 AI 생성 이미지입니다.
