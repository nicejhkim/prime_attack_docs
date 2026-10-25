# prime_attack_docs

Prime Attack 스토어·법적 문서용 GitHub Pages 저장소.

앱 저장소(`prime_attack`) Pages 소스로 연결되어 있으며, 공개 주소는 다음과 같다.

- 사이트: https://nicejhkim.github.io/prime_attack/
- 개인정보처리방침 (KO): https://nicejhkim.github.io/prime_attack/ko/privacy/
- Privacy Policy (EN): https://nicejhkim.github.io/prime_attack/en/privacy/

## 구조

| 경로 | 역할 |
|------|------|
| `store/legal/` | 방침 **원본** (KO/EN). 여기만 고치면 된다. |
| `store/appstore/`, `store/play/` | 스토어 리스팅·이미지·체크리스트. 사이트에 올리지 않음. |
| `ko/`, `en/` | 언어별 permalink 래퍼 (`include_relative`로 원본 삽입). |
| `_layouts/`, `assets/` | 공통 레이아웃·스타일. |

## 방침 수정

1. `store/legal/privacy-policy-ko.md` / `privacy-policy-en.md` 수정
2. 시행일(Effective) 갱신
3. `main`에 푸시 → Pages 반영. 스토어 Console URL은 그대로 둔다.

이용약관 등이 필요하면 `store/legal/`에 마크다운을 추가하고, `ko/`·`en/`에 같은 방식의 래퍼만 만들면 된다.
