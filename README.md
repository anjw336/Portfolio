# jiwon.dev — 안지원 웹 포트폴리오

React + TypeScript + Vite로 만든 페이지형 개인 포트폴리오입니다.

## 구성

- **Home**: 자기소개와 `Projects / Activities / About` 이동 버튼
- **Projects**: MEMO:RE, Kotlin 게임 소개 및 각각의 상세 페이지
- **Activities**: KAIST AI × 실패 아이디어 공모전 조사, AI 협업 규칙 개선 참여
- **About**: 자기소개, 기술, GitHub, 이력서 PDF, 이메일

**스크롤형 원페이지가 아닙니다.** 버튼을 누르면 별도의 화면으로 전환됩니다. URL은 `/#/projects`, `/#/activities` 등의 해시 라우트를 사용하며, 브라우저 뒤로 가기와 새로고침도 지원합니다.

프로젝트 내부의 자세한 내용을 읽을 때만 해당 상세 페이지 안에서 스크롤합니다.

## 실행

Node.js 20.19+ 또는 22.12+ 권장.

```bash
npm install
npm run dev
```

터미널에 표시된 `http://localhost:5173` 주소를 브라우저에서 열면 됩니다.

```bash
npm run typecheck   # TypeScript 검사
npm run build       # 검사 + Vite 빌드
npm run preview     # 배포용 빌드 미리보기
```

## 수정할 곳

| 수정 내용 | 파일 |
|---|---|
| 자기소개, 프로젝트/활동 내용, 링크 | `src/App.tsx` |
| 컬러, 크기, 레이아웃, 반응형 스타일 | `src/App.css` |
| 폰트, 기본 스타일 | `src/index.css` |
| 제출용 이력서 PDF 교체 | `public/resume.pdf` |

현재 이력서 다운로드는 `public/resume.pdf`에 포함돼 있습니다. 향후 수정한 파일이 있으면 동일한 이름으로 교체하세요.

## Vercel 배포

1. GitHub에 이 프로젝트를 새 저장소로 올립니다.
2. Vercel에서 **Add New Project** → GitHub 저장소 연결.
3. Framework Preset: **Vite** / Build Command: `npm run build` / Output Directory: `dist`.
4. **Deploy**.

해시 라우트를 쓰므로 서버의 별도 rewrite 설정 없이 상세 URL이 작동합니다.

## 유의사항

- 일러스트는 실제 제품 스크린샷이 아닌 CSS로 만든 **임시 장식 이미지**입니다. 나중에 실제 화면으로 교체할 수 있습니다.
- KAIST AI 공모전은 **조사·분석 경험**으로 표기했고, 실제 LLM 시스템 구현이나 수상으로 표현하지 않았습니다.
- 팀 AGENTS.md는 **개선 의견 제안·수정 참여**로 표기했습니다. 개인 단독 제작으로 표현하지 않았습니다.
- GitHub 팀 프로젝트 내용은 기여했던 PR 링크로 확인할 수 있습니다.
