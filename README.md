# Golf Caddy

GitHub Pages에 바로 올려 사용할 수 있는 단일 파일 골프 캐디 앱입니다.

## GitHub Pages 배포

1. 새 GitHub 저장소를 만듭니다.
2. 이 폴더의 파일을 저장소 루트에 업로드합니다.
   - `index.html`
   - `.nojekyll`
   - `README.md`
3. GitHub 저장소에서 `Settings` -> `Pages`로 이동합니다.
4. `Deploy from a branch`를 선택하고 `main` / `/root`를 지정합니다.
5. 배포 주소가 열리면 앱 상단의 `OpenAI`, `Claude`, `Kakao` 버튼으로 API 키를 저장합니다.

## API 키

- OpenAI 키: 홀 공략, 날씨, 골프장 정보, 레슨 새로고침, 음성 입력과 음성 읽기에 사용됩니다.
- Claude 키: OpenAI 실패 시 백업 검색에 사용됩니다.
- Kakao JavaScript 키: 골프장 정보 화면의 지도 표시에 사용됩니다.
- 키는 GitHub에 업로드되지 않고, 사용자의 브라우저 `localStorage`에만 저장됩니다.

## AI 검색 방식

앱은 OpenAI Responses API의 웹 검색을 먼저 사용합니다. OpenAI 요청이 실패하고 Claude 키가 저장되어 있으면 Claude 웹검색으로 자동 재시도합니다.

## 카카오맵

Kakao JavaScript 키는 고정으로 넣어도 됩니다. `index.html`에서 아래 줄의 빈 문자열에 키를 넣으세요.

```js
const KAKAO_JS_KEY='';
```

키를 코드에 넣지 않은 경우에는 앱 상단의 `Kakao` 버튼에 입력해도 지도가 표시됩니다.

Kakao 개발자 콘솔에서 GitHub Pages 도메인을 허용 도메인에 추가해야 합니다.
예: `https://사용자명.github.io`

## 주의

이 앱은 정적 HTML로 동작합니다. 공개 GitHub 저장소에 실제 API 키를 직접 적어 넣지 마세요.
