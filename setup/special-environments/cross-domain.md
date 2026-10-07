# 크로스 도메인 분석 설치

#### 적용 대상

* PC(1사 쿠키 적용 이후), 모바일웹 모두 적용 대상
* **멀티 도메인 사용**: 하나의 에이스카운터 계정으로 서로 다른 도메인의 방문 정보를 하나의 세션으로 묶어 분석하고 싶을 때 세팅이 필요합니다.

**예시**

* 최초 유입 도메인(www.acecounter.com)과 이동한 회원가입/로그인 페이지의 도메인(member.acecounter.co.kr)이 다른 경우
* 최초 유입 도메인과 이동한 신청/예약 처리 페이지의 도메인(bbs.acecounter.co.kr)이 다른 경우
* 이벤트 페이지 도메인(event.acecounter.co.kr)과, 이벤트 페이지에서 본 사이트로 이동 시 본 사이트 도메인(www.acecounter.com)이 다른 경우

#### 공통 스크립트 내 도메인 세팅

```html
<script language='javascript'>
    var _AceCrsdm = 'dev-shop.acecounter.com,vklog.loginse.co.kr';  // 분석하고자 하는 모든 도메인
    var _AceCkdm = 'acecounter.com,loginse.co.kr';  // 분석하고자 하는 모든 도메인의 Root Domain
</script>
```

* `_AceCrsdm`: 분석하고자 하는 모든 도메인을 홑따옴표 안에 쉼표로 구분하여 띄어쓰기 없이 세팅합니다. (예: 'admin.acecounter.com,www.acecounter.co.kr')
* `_AceCkdm`: 분석하고자 하는 도메인들의 Root Domain을 같은 방식으로 세팅합니다.

{% hint style="info" %}
Root Domain이란 서브 도메인(www 포함)을 포함하지 않는 도메인 자체를 말합니다. (예: www.acecounter.com → acecounter.com, admin.acecounter.com → acecounter.com)
{% endhint %}

#### 제약 사항

1. **함수를 통한 페이지 이동**: URL에 파라미터를 붙여 세션을 연결하는 방식이므로, 함수를 통해 이동하면 파라미터가 붙지 않아 세션 유지가 불가합니다.
2. **접속 도메인에 따른 쿠키 정보 변경**: 크로스 도메인으로 연결된 두 사이트 중 한 곳에서 여러 번 방문/구매한 방문자라도, 페이지 이동 없이 다른 사이트로 먼저 접속한 뒤 원래 사이트로 이동하면 정보가 나중에 접속한 사이트 기준으로 바뀔 수 있습니다.
3. **즐겨찾기**: URL에 세션 값 파라미터가 붙은 상태로 즐겨찾기를 하면, 이후 즐겨찾기로만 접속 시 즐겨찾기 당시 값으로 돌아가 정상 분석되지 않을 수 있습니다.
