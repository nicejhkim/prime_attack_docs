# App Store 출시 준비

등록 문구는 `listing-ko.md`(기본 언어), `listing-en.md`에 있다. 아래는 App Store Connect에서 채우거나 결정해야 하는 것들이다.

## 앱 개인정보 보호 (Nutrition Label)

개인정보처리방침(`store/legal/privacy-policy-ko.md`)과 같은 내용으로 신고한다. Play 데이터 보안 표(`store/play/README.md`)와도 어긋나면 안 된다.

| Apple 분류 | 수집 | 사용자에 연결 | 추적 | 목적 |
|---|---|---|---|---|
| 충돌 데이터(Crash Data) | 예 | 아니요 | 아니요 | 앱 기능 |
| 성능 데이터(Performance Data) | 예 | 아니요 | 아니요 | 앱 기능 |
| 제품 상호작용(Product Interaction) | 예 | 아니요 | 아니요 | 분석 |
| 기기 ID(Device ID) | 예 | 아니요 | 아니요 | 분석 |

- **추적(Tracking)은 전부 '아니요'다.** 광고 식별자를 쓰지 않고 데이터를 제3자와 묶지 않으므로 `NSUserTrackingUsageDescription`과 ATT 동의창이 필요 없다.
- 이름·이메일·정확한 위치·연락처·사진·금융 정보: 수집 안 함.
- Game Center 점수는 Apple이 다루는 데이터다. 앱이 따로 저장하지 않는다.

## 연령 등급

폭력·선정성·도박·약물·불쾌한 표현 없음 → **4+**. 설문에서 모두 '없음'으로 답한다. 웹 브라우징 기능 없음(스토어 링크만 외부로 연다).

## 수출 규정

`ios/Runner/Info.plist`에 `ITSAppUsesNonExemptEncryption = false`가 들어 있다. HTTPS 외의 암호화를 쓰지 않으므로 빌드마다 질문이 뜨지 않는다. 암호화 코드를 추가하면 이 값을 다시 보라.

## 스크린샷

**없음. 반드시 필요하다.** 최소 요구는 6.9"(또는 6.7") iPhone 세로다.

`TARGETED_DEVICE_FAMILY = "1"`이라 **iPhone 전용**으로 올라간다(2026-10-24 결정). iPad 스크린샷은 필요 없다. 아이패드를 지원하기로 바꾸면 `"1,2"`로 되돌리고 13" iPad 스크린샷을 따로 준비해야 한다.

찍을 장면: 시작 화면, 조준 중인 테이블, 소수 적중('소수!'와 콤보), 소인수분해 힌트, 클리어 카드(별 3개).

## 심사 노트에 적을 것

- 순위표는 Game Center 로그인이 있어야 동작한다. 로그인하지 않아도 게임은 모두 플레이할 수 있다.
- 계정·로그인·결제가 없어 심사용 데모 계정이 필요 없다.
- 인터넷 없이 플레이된다. 네트워크는 점수 제출, 충돌 리포트, 사용 분석, 버전 확인에만 쓴다.

## 개인정보 매니페스트 (PrivacyInfo.xcprivacy)

앱 타깃에는 아직 없다. Firebase·Flutter 플러그인은 각자 매니페스트를 들고 오므로 보통은 통과하지만, 업로드 뒤 Apple이 `ITMS-91053`(필수 사유 API 미신고) 메일을 보내면 앱 타깃에 `PrivacyInfo.xcprivacy`를 추가하고 해당 API의 사유를 적어야 한다. 그 메일이 오기 전에는 추측으로 적지 않는다.

## 막힌 것

- 스크린샷 (위)
- ~~개인정보처리방침 URL 호스팅~~ — https://nicejhkim.github.io/prime_attack_docs/ko/privacy/ (EN: `/en/privacy/`)

