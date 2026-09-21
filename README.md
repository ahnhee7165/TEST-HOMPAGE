# 널위한 부동산

2호선 매물 소개와 방문 상담 문의 예시 페이지 (정적 HTML 1개 파일).

## 1. 메타 픽셀 ID 넣기
`index.html`에서 `YOUR_PIXEL_ID`를 검색해 실제 픽셀 ID로 바꿉니다. (2곳)

## 2. GitHub Pages로 배포
1. GitHub에서 새 저장소를 만들고 `index.html`, `README.md`를 올립니다.
2. 저장소의 Settings > Pages 로 이동합니다.
3. Source를 `Deploy from a branch`, Branch를 `main` / `/ (root)`로 지정하고 저장합니다.
4. 1~2분 뒤 `https://<계정명>.github.io/<저장소명>/` 주소로 접속됩니다.

## 3. 전송되는 픽셀 이벤트
| 시점 | 이벤트 | 전달 값 |
|---|---|---|
| 페이지 진입 | PageView | - |
| 역 선택 | ViewContent | content_name(역), content_category(2호선) |
| 매물 "문의하기" 클릭 | ViewContent | content_ids, content_name, content_category(방 종류) |
| 문의 폼 제출 완료 | Lead | content_name(매물), content_category(거래 유형) |

이름, 전화번호, 보유 자산은 픽셀로 전송하지 않습니다.

## 4. 테스트
- 크롬 확장 "Meta Pixel Helper"로 이벤트 발화를 확인합니다.
- 이벤트 관리자 > 테스트 이벤트 탭에서 실시간 수신을 확인합니다.

## 5. 주의
- 현재 문의 폼은 어디에도 저장되지 않는 예시입니다. 실제 운영 시에는 접수 내용을 받을 저장소(구글 폼, 스프레드시트, 메일 발송 등)를 연결해야 합니다.
- 실제 고객 정보를 받는다면 개인정보 수집·이용 동의 절차가 필요합니다.
