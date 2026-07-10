# 강의 시간표 자동 생성기

소방안전설비과 강의 시간표를 자동으로 배정·생성하는 정적 웹 앱입니다.
빌드 과정이 없는 순수 HTML/CSS/JS 단일 페이지로, `index.html` 하나만 배포하면 됩니다.

## 로컬 실행
`index.html`을 브라우저로 열면 바로 실행됩니다.
앱 전체가 이 파일 하나에 들어 있으므로, 수정할 곳도 항상 `index.html` 하나뿐입니다.

## Vercel 배포

### 방법 1) Vercel CLI (가장 빠름)
```bash
cd "c:\time table"
npx vercel@latest --prod
```
- 최초 실행 시 로그인(이메일/GitHub)을 진행합니다.
- 이후 물어보는 설정(scope, 프로젝트 이름, 디렉터리)은 기본값(Enter)으로 진행하면 됩니다.
- 완료되면 `https://<프로젝트명>.vercel.app` 주소가 출력됩니다.

### 방법 2) GitHub 연동
1. 이 폴더를 GitHub 저장소로 push
2. https://vercel.com/new 에서 저장소 Import → Deploy (설정 변경 없이 그대로)

## 구성
- `index.html` — 앱 본체(배포 대상). 유일한 소스 파일입니다.
- `vercel.json` — 정적 배포 설정
- 프레임워크/빌드 명령 없음 (Framework Preset: **Other**)
