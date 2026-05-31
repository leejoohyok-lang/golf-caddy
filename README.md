# 범이의 골프

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
- Kakao JavaScript 키: 골프장 지도와 실제 주변 맛집 검색에 사용됩니다.
- OpenAI와 Claude 키는 GitHub에 업로드하지 말고, 앱 화면에서 입력해 브라우저에만 저장하세요.

## AI 검색 방식

앱은 OpenAI Responses API의 웹 검색을 먼저 사용합니다. OpenAI 요청이 실패하고 Claude 키가 저장되어 있으면 Claude 웹검색으로 자동 재시도합니다.

## 카카오맵

Kakao JavaScript 키는 `index.html`의 `KAKAO_JS_KEY` 상수에 고정으로 넣을 수 있습니다.

Kakao Developers에서 다음 설정도 필요합니다.

- 카카오맵 사용 설정: ON
- JavaScript SDK 도메인: GitHub Pages 주소 등록

예:

```text
https://사용자명.github.io
https://사용자명.github.io/저장소명/
```

`file://`로 직접 열면 Kakao 지도와 장소검색이 차단될 수 있습니다. 최종 확인은 GitHub Pages 주소에서 하세요.

## 업로드 파일

GitHub에 다시 올릴 때는 보통 아래 두 파일만 교체하면 됩니다.

- `index.html`
- `README.md`

`.nojekyll`은 이미 있으면 다시 올리지 않아도 됩니다.
