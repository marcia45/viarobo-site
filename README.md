# via robo 홈페이지 (viarobo.net)

한 페이지짜리 회사 소개 사이트입니다. GitHub Pages로 배포하고, 도메인 viarobo.net은 Cloudflare DNS에서 연결합니다.

- `index.html`: 페이지 전체(스타일·스크립트 포함)
- `img/`: 3D 오브젝트 이미지(three.js로 직접 렌더링)
- 문의 게시판: Supabase Edge Function `site-inquiry`에 글을 저장하고, 새 글이 오면 Resend로 알림 메일을 보냅니다.
  - 글 목록에는 제목, 이름 일부(가운데 가림), 날짜, 상태만 보입니다.
  - 내용과 연락처는 Supabase 표 `site_inquiries`에서 확인합니다. `status`를 `answered`로 바꾸면 "답변 완료"로 표시됩니다.
