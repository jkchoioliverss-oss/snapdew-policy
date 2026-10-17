# 제품 요구사항

제품의 사용자 경험과 지원 범위를 확인한다.

[전체 문서 색인](../index.md)

| 문서 | 경로 |
| --- | --- |
| [앨범 사진 편집 구현 요구사항 정의서](ALBUM_EDITING_REQUIREMENTS.md) | `ALBUM_EDITING_REQUIREMENTS.md` |
| [프로젝트 명세](PROJECT_SPEC.md) | `PROJECT_SPEC.md` |
| [공개 개인정보처리방침·이용약관 안내](policy/index.html) | GitHub Pages에 단독 업로드하는 `index.html`. 데이터 처리 또는 구독 구현 변경 시 재검토. |

## 정책 페이지 게시

`policy/index.html` 한 파일을 공개 저장소의 게시 루트에 `index.html`로 올린다. GitHub Pages의
게시 소스를 해당 브랜치와 `/(root)`로 설정한다. 발급된 사이트 주소를 개인정보처리방침 URL로,
페이지에 연결된 Apple 표준 EULA 주소를 이용약관 URL로 사용할 수 있다. 운영자와 문의 주소는
사용자가 제공한 값을 반영했다. 구독 관련 설명은 해당 기능을 제공하는 버전에 적용되며,
실제 결제 구현·외부 SDK·문의 보관 절차 변경 시 게시 내용도 대조한다.

2026-10-17 검증: Python `html.parser`로 태그 중첩, 고유 ID, 내부 앵커, 연락처,
미교체 자리표시자 및 외부 리소스 부재를 검사했고 통과했다. `git diff --check` 통과.
반응형 CSS를 포함했으나 브라우저 정책이 로컬 파일 접근을 차단하여 시각 검증은 미완료다.
`xcodebuild -project Snapdew.xcodeproj -scheme Snapdew -configuration Debug -destination
'generic/platform=iOS Simulator' build`는 환경의 `Operation not permitted` 오류로 실패했다.
앱 소스 변경은 없으며 Simulator·물리 기기 검증은 수행하지 않았다.
