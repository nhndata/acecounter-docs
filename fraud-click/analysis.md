# 부정클릭 분석하기

#### 검색광고 중복유입 확인하기

[**\[분석통계 > 검색광고효과 > 중복유입 간격\]**](https://www.acecounter.com/stat/view/statview4_15.amz) 리포트에서 조회 기간 내 유입한 방문자의 Unique ID를 분석해 중복 유입 내역과 종합 정보를 제공합니다.

{% hint style="info" %}
**Unique ID란?** 기기를 구분하기 위해 에이스카운터가 부여한 고유 값입니다. CPC 광고 클릭 후 방문 시 Unique ID로 동일 방문자 여부를 판단하므로, IP가 변동되어도 동일 방문자임을 알 수 있습니다.
{% endhint %}

예를 들어 한 방문자가 10분 이내 광고를 10회 유입했고 모든 유입이 첫 페이지 확인 후 이탈(평균 페이지뷰 1)했다면, 부정클릭으로 의심해 볼 수 있습니다.

{% hint style="warning" %}
의심되는 IP의 광고 클릭을 원치 않는다면 광고사가 제공하는 광고노출 제한 기능을 활용하세요. 무효클릭으로 의심되는 경우 매체별 무효클릭 신고 가이드를 참고해 신고할 수 있습니다.
{% endhint %}

#### 검색광고 의심유입 분석하기

CPC 검색광고가 기준 시간 동안 반복 유입된 경우 의심으로 진단하는 '의심 유입 분석' 리포트를 제공합니다.

{% stepper %}
{% step %}
#### 의심유입 진단 설정하기

[**\[설정 > 검색광고 모니터링 > 의심유입 진단\]**](https://www.acecounter.com/stat/view/manager3_1.amz) 메뉴에서 설정합니다.
{% endstep %}

{% step %}
#### 의심유입 진단 확인하기

[**\[분석통계 > 검색광고효과 > 의심유입 분석\]**](https://www.acecounter.com/stat/view/statview4_17.amz) 리포트에서 Unique ID 기준으로 확인합니다.
{% endstep %}
{% endstepper %}

**의심유입 분석 리포트 용어**

<table><thead><tr><th width="159">용어</th><th>설명</th></tr></thead><tbody><tr><td>최초 유입 일시</td><td>쿠키에 저장된, 검색광고로 최초 유입한 일시입니다. 쿠키 삭제 시 다음 유입에서 새 Unique ID와 최초 유입 일시가 생성됩니다.</td></tr><tr><td>누적 유입수</td><td>최초 유입 일시부터 조회 기간까지의 총 유입수입니다. 높을수록 검색광고 유입이 지속적으로 시도되고 있음을 의미합니다.</td></tr><tr><td>기간내 유입수</td><td>조회 기간 동안의 Unique ID별 검색광고 유입수입니다.</td></tr><tr><td>의심 유입수</td><td>의심유입 진단 설정에 따라 의심으로 분석된 유입수입니다. (예: 30분 내 3회 이상 유입 시 의심으로 분석) <a href="https://www.acecounter.com/stat/view/manager3_1.amz"><strong>[검색광고 모니터링 > 의심유입 진단]</strong></a>에서 설정한 내용에 따라 진단합니다.</td></tr></tbody></table>
