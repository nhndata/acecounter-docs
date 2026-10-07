# 분석 스크립트 설치 확인

공통 스크립트와 환경변수 스크립트까지 모두 삽입했다면, 마지막으로 정상 작동 여부를 확인해야 합니다. 개발자 도구의 네트워크 탭을 하나하나 확인하는 대신, AceCounter 설치 확인 크롬 확장 프로그램을 사용하면 훨씬 빠르고 쉽게 검수할 수 있습니다.

### 사용 방법

{% stepper %}
{% step %}
#### 확장 프로그램 설치

크롬 웹스토어에서 [AceCounter 설치 확인 프로그램](https://chromewebstore.google.com/detail/eckkhbdopjhjafkmlbbjmnippoedjbei)을 설치합니다.
{% endstep %}

{% step %}
#### 페이지 새로고침

스크립트를 설치한 페이지로 이동한 뒤 새로고침합니다.
{% endstep %}

{% step %}
#### 항목 확인

화면에 나타나는 알림에서 아래 항목이 정상인지 확인합니다.

* 공통 스크립트 설치 여부
* acecounter.com으로 전송되는 수집 요청과 파라미터
* m\_jid, m\_ud1\~3, m\_pay 등 환경변수 값
* UTM 등 광고 파라미터
* 현재 페이지에 저장된 쿠키 목록
{% endstep %}
{% endstepper %}

{% hint style="info" %}
회원가입, 로그인, 구매처럼 이벤트가 발생하는 페이지는 해당 액션을 실제로 수행한 뒤 확인해야 정확하게 검증됩니다. (예: 구매완료 페이지에서 m\_pay 값이 실제로 잡히는지 확인)
{% endhint %}
