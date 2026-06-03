# 수능특강 영어 단어장 — 앱으로 설치하기

GitHub Pages에 올린 뒤, 휴대폰·아이패드 홈 화면에 앱처럼 추가하는 방법이야.

## 1. GitHub에 올리기
1. github.com 로그인 → 우측 상단 **+** → **New repository**
2. 이름 입력(예: `english-vocab`), **Public** 선택 → **Create repository**
3. **Add file → Upload files** 클릭
4. 이 폴더 안의 **모든 파일**을 드래그해서 업로드
   - `index.html`, `manifest.json`, `sw.js`
   - `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `favicon-32.png`
5. 아래 **Commit changes** 클릭

## 2. Pages 켜기
1. repository 상단 **Settings → Pages**
2. **Source**: `Deploy from a branch`
3. **Branch**: `main` / `/ (root)` → **Save**
4. 1~2분 뒤 주소가 생성됨 →
   `https://<내아이디>.github.io/english-vocab/`

## 3. 홈 화면에 추가
- **아이폰 / 아이패드**: 위 주소를 꼭 **Safari**로 열기 → 공유 버튼(□↑) → **홈 화면에 추가** → 추가
- **안드로이드**: **Chrome**으로 열기 → 메뉴(⋮) → **앱 설치** 또는 **홈 화면에 추가**

이제 홈 화면 아이콘을 누르면 주소창 없이 전체 화면 앱처럼 실행돼.

## 참고
- 처음 한 번 인터넷에 연결된 상태로 열면, 이후엔 **오프라인에서도** 열려.
- 암기 체크는 기기에 저장(localStorage)되니 같은 기기·같은 주소에서 유지돼.
- 단어장을 수정해 다시 업로드했는데 앱에 반영이 안 되면, `sw.js` 첫 줄
  `const CACHE = 'vocab-az-v1';` 의 `v1`을 `v2`로 바꿔서 올리면 돼.
- PWA·홈화면 추가는 `https`에서만 동작하는데, GitHub Pages가 https라 그대로 돼.
