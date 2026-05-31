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
5. 배포 주소가 열리면 앱 상단의 `Claude`, `Voice` 버튼으로 API 키를 저장합니다.

## API 키

- Claude 키: 홀 공략, 날씨, 골프장 정보, 레슨 새로고침에 사용됩니다.
- OpenAI 키: 음성 입력과 음성 읽기에 사용됩니다.
- 키는 GitHub에 업로드되지 않고, 사용자의 브라우저 `localStorage`에만 저장됩니다.

## 카카오맵

골프장 정보 화면에서 지도를 쓰려면 `index.html` 안의 `YOUR_KAKAO_KEY`를 실제 Kakao JavaScript 키로 바꾼 뒤 업로드하세요.

```html
https://dapi.kakao.com/v2/maps/sdk.js?appkey=YOUR_KAKAO_KEY&libraries=services
```

Kakao 개발자 콘솔에서 GitHub Pages 도메인도 허용 도메인에 추가해야 합니다.

## 주의

이 앱은 정적 HTML로 동작합니다. 공개 GitHub 저장소에 실제 API 키를 직접 적어 넣지 마세요.
