# 특수 환경 대응

기본 분석 스크립트 외에 사이트의 기술적 구조나 사용자 이동 흐름(Redirect, 크로스 도메인)에 따라 정교한 분석을 위해 추가 설정이 필요한 가이드 모음입니다.

비즈니스 환경 및 웹사이트 구조에 해당하는 항목을 선택하여 세팅을 진행해 주세요.



**📌 세부 설정 가이드**

* [첫 페이지에서 강제 이동하는 사이트 (Redirect 대응)](https://acecounter.gitbook.io/guide/script-setting/special-script/redirect)
  * 대상: 접속 시 특정 URL로 자동 리다이렉트되거나 도메인 주소가 변경되는 사이트
  * 주요 내용: 첫 페이지 강제 이동 과정에서 유입 출처(Referrer) 및 방문 데이터가 유실되지 않도록 보완하는 스크립트 적용 방법
* [크로스 도메인 (Cross-Domain) 세팅](https://acecounter.gitbook.io/guide/script-setting/special-script/crossdomain)
  * 대상: 결제, 로그인, 이벤트 페이지 등에서 서로 다른 도메인(예: `a.com` `b.com`)으로 연속 이동하는 사이트
  * 주요 내용: 여러 도메인을 하나의 방문자 세션으로 연결하여 이탈률 및 전환 성과를 정확하게 측정하는 가이드

