# Private Product

개인 용도로 만든 데모와 재료를 링크로 열어볼 수 있게 모아둔 저장소다.
전부 파일 하나로 동작하며 서버가 필요 없다.

발행 주소 — https://lsh-osiris76.github.io/Private-Product/

| 경로 | 내용 |
|---|---|
| `/leadform/` | 리드폼+ 광고 콘솔 — 광고 노출 → 폼 참여 → 쿠폰 발급 → 상담 → 브랜드 앱까지 이어지는 참여형 광고 데모 |
| `/ui-kit/` | 중립 기본형 UI 킷 — 색·타이포·프레임·컴포넌트를 복사용 코드와 함께 정리 |

## 원칙

- **데모 데이터는 전부 가상이다.** 실제 브랜드명·계정·개인정보를 쓰지 않는다
- 공개 저장소이므로 올리기 전에 비식별을 확인한다
- 각 페이지는 외부 참조가 구글 폰트뿐이다. CDN 스크립트를 추가하지 않는다

## 갱신 방법

`/leadform/` 은 별도 프로젝트에서 빌드해 나온 결과물이다.

```
npm run build:public          # dist-public/index.html 생성 (비식별 + 금칙어 검사)
```

`/ui-kit/` 원본은 `_shared-ui-kit/index.html` 이다. 아티팩트용 파일이라
GitHub Pages 에 올릴 때는 `<!doctype html>` 껍데기를 씌워야 한다.

## GitHub Pages 설정

Settings → Pages → Source `Deploy from a branch` → Branch `main` / `/ (root)`.
`.nojekyll` 이 있어 Jekyll 처리를 건너뛴다.
