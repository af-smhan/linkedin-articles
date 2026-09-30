# 타코벨 드라이브스루 AI 조사 보고서

> 2026-09-22 작성, 2026-09-30 Claude Docs에서 이관. 이 문서는 조사 기록이며 글에 쓸 사실의 기준은 `facts.md`(팩트체크 ① 통과 목록)다.
> 2026-09-30 정정: Intouch 조사 수치(83%·62%·+14%p)는 타코벨 단독이 아닌 3개 브랜드 조사이며, 62%와 +14%p의 의미는 아래 표기처럼 제한적으로만 쓸 수 있다.

## 요약

타코벨의 AI 음성주문 드라이브스루는 2022년경 비공개 테스트로 시작해 2026년 7월 기준 미국 38개 주 890곳 이상으로 확대됐다. 중간인 2025년 8월 "물 18,000잔" 장난 영상이 퍼지며 경영진이 속도 조절을 공개적으로 인정했지만, 철수하지 않고 사람 개입을 전제로 한 하이브리드 운영으로 방향을 틀었다.

- **2022~2023년:** 약 2년간 내부 테스트. 2023년 11월 Yum 경영진이 캘리포니아 일부 매장 테스트를 처음 공개 언급. 음성 AI 업체 Omilia와 협력 시작.
- **2024년:** 1분기 캘리포니아 5곳 → 7월 13개 주 100곳 이상 → 11월 300곳 이상, 누적 200만 건 주문 처리.
- **2025년:** 3월 Nvidia와 제휴 발표. 8월 500곳 이상 도입 상태에서 WSJ 보도와 바이럴 영상으로 "재검토" 국면.
- **2026년:** 4월 차량별로 바뀌는 AI 메뉴판 테스트 공개. 7월 Omilia 계약 확대와 함께 890곳 이상으로 확장. 회사는 직원 유지율 개선과 속도 유지를 성과로 제시.

참고로 영문 위키백과는 AI 드라이브스루가 "중단됐다"고 적고 있으나, 2026년 7월 확대 발표와 맞지 않는 오류로 보인다.

## 배경: 드라이브스루 중심 전략의 역사

타코벨은 매출 대부분이 드라이브스루에서 나오는 브랜드라, AI 도입 전부터 드라이브스루 형태 자체를 계속 실험해 왔다 ([QSR Magazine](https://www.qsrmagazine.com/story/taco-bell-now-has-drive-thru-ai-ordering-in-about-900-locations/)).

| 시기 | 사건 | 내용 |
|---|---|---|
| 2025년 10월 | QSR 드라이브스루 리포트 5년 연속 1위 | 평균 256.81초(전년 255.78초). 업계 최대 규모 AI 도입 사례로 언급 ([QSR](https://www.qsrmagazine.com/story/taco-bell-is-once-again-the-fastest-drive-thru-in-america/), [Intouch Insight](https://www.intouchinsight.com/blog/drive-thru-trends)) |
| 2022년 6월 7일 | [Taco Bell Defy](https://www.tacobell.com/newsroom/taco-bell-defy-concept-opens-june-7-one-of-the-most-innovative-drive-thru-experiences-yet) 개장 | 미네소타주 브루클린파크. 4개 차선·2층 구조, 음식을 내려보내는 수직 리프트, 2층 직원과의 양방향 영상·음성. 목표 2분 이내. 가맹사 Border Foods ([MPR News](https://www.mprnews.org/story/2022/06/07/twostory-fourlane-taco-bell-drivethru-restaurant-opening-in-brooklyn-park), [Axios](https://www.axios.com/2022/06/06/taco-bell-defy-brooklyn-park-minnesota)) |
| 2020년 8월 20일 | [Go Mobile](https://www.tacobell.com/newsroom/taco-bell-go-mobile) 콘셉트 발표 | 모바일 주문 전용 차선을 포함한 이중 드라이브스루, 커브사이드 픽업. 2021년 1분기 직영 2곳 개장 계획 ([CNBC](https://www.cnbc.com/2020/08/20/taco-bell-unveils-new-design-with-more-drive-thrus-as-pandemic-permanently-shifts-how-we-order.html), [Restaurant Dive](https://www.restaurantdive.com/news/taco-bell-is-launching-a-mobile-focused-double-drive-thru-model-in-2021/583856/)) |
| 2015년 9월 | Cantina 매장 | 시카고 위커파크에서 시작한 주류 판매 도심형 매장 ([Wikipedia](https://en.wikipedia.org/wiki/Taco_Bell)) |
| 1980년경 | 드라이브스루 보편화 | 1962년 첫 매장은 워크업 창구만 있었고, 드라이브스루는 1980년에야 일반화 ([Wikipedia](https://en.wikipedia.org/wiki/Taco_Bell)) |
| 1962년 3월 21일 | 창업 | 글렌 벨이 캘리포니아 다우니에 1호점 개장 ([Wikipedia](https://en.wikipedia.org/wiki/Taco_Bell)) |

모회사 Yum! Brands는 2021년 Dragontail Systems를 인수하고 POS(Poseidon)·매장 관리 앱(SuperApp)을 자체 개발해 이를 "Byte by Yum!" 플랫폼으로 묶었다. AI 음성주문은 이 플랫폼 위에 올라간 기능이다 ([Restaurant Business](https://www.restaurantbusinessonline.com/technology/taco-bell-parent-yum-brands-future-ai)).

## AI 음성주문 상세 타임라인

가장 최근 사건이 위에 오도록 정렬했다. 매장 수는 발표 시점 기준이다.

| 날짜 | 사건 | 핵심 내용 |
|---|---|---|
| 2026-08-20 | 업계 비교 분석 보도 | 미스터리 쇼퍼 120회 방문 기준 직원 개입률: 타코벨 30%, 웬디스 33%, 보장글스 3% ([The Next Web](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion)) |
| 2026-07-30 | Yum 2분기 실적 | 실적은 예상 상회. 다만 7월 중순 타코벨 관련 사이클로스포라 식중독 사태가 트래픽에 영향 ([Quartz](https://qz.com/yum-brands-q2-2026-earnings-taco-bell-cyclospora-073026)) |
| 2026-07-07 | Omilia 계약 확대 발표 | 38개 주 890곳 이상. 속도 동등 이상, AI 매장 직원 유지율 개선, 불만은 비AI 매장과 동등 이하 ([Business Wire](https://www.businesswire.com/news/home/20260707542838/en/Omilia-Powers-Taco-Bells-Expansion-of-Voice-AI-Across-890-U.S.-Drive-Thrus), [Restaurant Dive](https://www.restaurantdive.com/news/taco-bell-omilia-drive-thru-ai-deployment/824564/), [NRN](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants)) |
| 2026-04-29 | Yum 1분기 실적 | 타코벨 미국 동일매장 매출 +8%. 차량별로 레이아웃·콘텐츠가 바뀌는 AI 드라이브스루 메뉴판 A/B 테스트, 전국 확대 계획 ([Yahoo Finance](https://finance.yahoo.com/markets/stocks/articles/yum-brands-q1-earnings-call-190733000.html), [Yahoo Finance](https://finance.yahoo.com/sectors/technology/articles/taco-bell-drive-thru-menu-091601379.html)) |
| 2025-10-06 | QSR 드라이브스루 리포트 | 5년 연속 속도 1위. 음성 AI 500~600곳 가동, 고사용 매장 이직률 감소 언급 ([QSR](https://www.qsrmagazine.com/story/taco-bell-is-once-again-the-fastest-drive-thru-in-america/)) |
| 2025-10-01 | Yum CEO 교체 | CFO 크리스 터너가 데이비드 깁스 후임 CEO 취임(6월 발표) ([Yum! Brands](https://investors.yum.com/news-events/financial-releases/news-details/2025/Yum-Brands-Appoints-Chris-Turner-as-Chief-Executive-Officer-Effective-October-1-2025/default.aspx)) |
| 2025-09-24 | 회사 공식 입장 | "학습·개선·확장에 계속 집중" 입장, 바쁜 매장은 사람이 주문 받는 방안 검토 ([Food On Demand](https://foodondemand.com/09242025/it-seems-every-brand-wants-to-use-voice-ai-yet-taco-bell-is-pulling-back/)) |
| 2025-08-29 | WSJ 보도 · "물 18,000잔" 확산 | CDTO 데인 매튜스: "솔직히 많이 배우고 있다… 실망할 때도, 놀랄 때도 있다." 시간대·매장별 사람 모니터링 권고. 당시 500곳 이상, 누적 200만 건 ([TechCrunch](https://techcrunch.com/2025/08/30/taco-bell-is-having-second-thoughts-about-relying-on-ai-at-the-drive-through/), [Futurism](https://futurism.com/taco-bells-ai-drive-thru), [Cybernews](https://cybernews.com/entertainment/taco-bell-ai-drive-thru-prank/)) |
| 2025-06~07 | Intouch Insight 현장 조사 | 타코벨·버거킹·웬디스 3개 브랜드 AI 주문 120건 평가(타코벨 단독 수치 아님). 틀린 AI 주문의 62%가 "하나의 반복되는 문제"와 연결, 직원이 개입해 바로잡았을 때 정확도 14%p 상승(기준점 미공개), 만족도는 일반 드라이브스루보다 6%p 높음 ([Intouch Insight](https://www.intouchinsight.com/blog/drive-thru-trends)) |
| 2025-03-18 | Yum–Nvidia 제휴 | Nvidia Riva·NIM 기반 음성 AI·컴퓨터 비전을 2025년 2분기 약 500개 매장(타코벨·피자헛·KFC·해빗버거)에 적용 계획 ([CNBC](https://www.cnbc.com/2025/03/18/taco-bell-parent-yum-brands-partners-with-nvidia-to-speed-up-use-of-ai.html), [Restaurant Dive](https://www.restaurantdive.com/news/yum-brands-nvidia-ai-taco-bell-pizza-hut-kfc-deal/742926/)) |
| 2024-11-11 | "라지 마운틴듀" 영상 바이럴 | TikTok @haleyduffhehe. AI가 음료를 계속 다시 물어 운전자가 폭발, 조회수 790만 ([Daily Dot](https://dailydot.com/taco-bell-ai-fail)) |
| 2024-11-05 | Yum 3분기 실적 | 300곳 이상, 누적 200만 건. "세계 최대 QSR 음성 AI 브랜드" 자평. AI 인력 스케줄링 5,000곳 ([PYMNTS](https://www.pymnts.com/restaurant-innovation/2024/yum-brands-leverages-voice-ai-and-data-for-personalized-service/), [CX Dive](https://www.customerexperiencedive.com/news/taco-bell-puts-ai-drive-thru-strategy-staff-scheduling-q3/732283/)) |
| 2024-07-31 | 본격 확대 발표 | 13개 주 100곳 이상 가동, 연내 "수백 곳" 목표. KFC 호주 5곳 테스트. "2년 넘게 미세조정" ([Yum! Brands](https://www.tacobell.com/newsroom/yum-brands-to-expand-voice-ai-technology), [NBC News](https://www.nbcnews.com/business/business-news/taco-bell-roll-ai-drive-thru-ordering-hundreds-locations-end-year-rcna164524), [NRN](https://www.nrn.com/quick-service/taco-bell-is-expanding-its-drive-thru-voice-ai-test)) |
| 2024-05 | 30곳 확대 | 캘리포니아 5곳 → 30곳 ([NBC News](https://www.nbcnews.com/business/business-news/taco-bell-roll-ai-drive-thru-ordering-hundreds-locations-end-year-rcna164524)) |
| 2024 1분기 | 공식 파일럿 | 캘리포니아 5곳 ([Restaurant Dive](https://www.restaurantdive.com/news/taco-bell-expands-drive-thru-artificial-intelligence-hundreds-US-units/722874/)) |
| 2023-11-02 | 첫 공개 언급 | Yum CFO 터너가 "캘리포니아 몇몇 매장" 음성 AI 테스트 공개. 속도·생산성 향상, 자동 업셀 ([NRN](https://www.nrn.com/quick-service/yum-brands-is-testing-voice-ai-beverage-automation)) |
| 2023 | Omilia 협력 시작 | 그리스 출신 대화형 AI 업체 ([Business Wire](https://www.businesswire.com/news/home/20260707542838/en/Omilia-Powers-Taco-Bells-Expansion-of-Voice-AI-Across-890-U.S.-Drive-Thrus)) |
| 2022년경 | 내부 테스트 추정 시점 | 2024년 7월 "2년 넘게 테스트" 발언에서 역산. 정확한 시작일은 미공개 |

출처마다 시작 시점이 다르다. 회사는 "2년 테스트", Cybernews는 "2023년부터 도입", Restaurant Dive는 "2024년 1분기 파일럿"이라고 쓴다. 내부 테스트→비공개 매장 테스트→공식 파일럿의 단계 차이로 보인다.

## 기술·파트너·성과 지표

핵심 엔진은 Omilia의 음성 AI이고, Yum의 자체 플랫폼 Byte by Yum!과 POS에 연결돼 돌아간다. Nvidia는 2025년 Yum 전체 브랜드의 AI 인프라 파트너로 별도 발표됐다.

| 구성 요소 | 내용 | 출처 |
|---|---|---|
| Omilia (음성 AI) | 자체 소형 언어모델, 초저지연, 드라이브스루 소음 필터링, 한정 메뉴·재고 실시간 반영, 슬랭·복잡한 커스터마이징 이해 | [Business Wire](https://www.businesswire.com/news/home/20260707542838/en/Omilia-Powers-Taco-Bells-Expansion-of-Voice-AI-Across-890-U.S.-Drive-Thrus) |
| Nvidia | Riva·NIM 기반 드라이브스루·콜센터 음성 AI, 주방 컴퓨터 비전, 매장 분석(Accelerated Restaurant Intelligence). Nvidia의 첫 외식업 협력 | [Restaurant Dive](https://www.restaurantdive.com/news/yum-brands-nvidia-ai-taco-bell-pizza-hut-kfc-deal/742926/) |
| Byte by Yum! | Poseidon POS, SuperApp, Dragontail 주방 최적화, AI 인력 스케줄링(5,000곳), 디지털 메뉴판(6,000곳+) | [Restaurant Business](https://www.restaurantbusinessonline.com/technology/taco-bell-parent-yum-brands-future-ai), [CX Dive](https://www.customerexperiencedive.com/news/taco-bell-puts-ai-drive-thru-strategy-staff-scheduling-q3/732283/) |
| AI 메뉴판 (2026) | 차량마다 레이아웃·콘텐츠·비주얼을 바꾸는 A/B 테스트, 2026년 전국 확대 계획 | [Yahoo Finance](https://finance.yahoo.com/sectors/technology/articles/taco-bell-drive-thru-menu-091601379.html) |

**회사 측 성과 주장**

- 거래 속도: 사람 주문 접수와 동등하거나 더 빠름 ([NRN](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants))
- 직원: AI 매장의 직원 유지율이 더 높음. 직원들은 AI를 "여분의 손"이라고 부른다는 것이 터너의 설명 ([CX Dive](https://www.customerexperiencedive.com/news/taco-bell-puts-ai-drive-thru-strategy-staff-scheduling-q3/732283/), [Entrepreneur](https://www.entrepreneur.com/buying-a-franchise/taco-bell-is-replacing-drive-thru-workers-with-ai))
- 고객: 만족도는 더 높고, 불만은 비AI 매장과 동등 이하

**독립 측정치**

| 지표 | 값 | 출처 |
|---|---|---|
| AI 주문 정확도 vs 사람 (3개 브랜드 평균, 2차 인용) | 83% vs 87% | [AI Adopters Club](https://aiadopters.club/p/wendys-beat-taco-bell-at-customer) (Intouch 인용, Intouch 원문에서는 미확인) |
| 틀린 AI 주문 중 "하나의 반복되는 문제"와 연결된 비율 (출처 간 설명 충돌: AI Adopters Club은 "AI 오류의 62%에 직원 개입"으로 인용) | 62% | [Intouch Insight](https://www.intouchinsight.com/blog/drive-thru-trends) |
| 타코벨 직원 개입률 | 30% | [The Next Web](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion) |
| "쉬우고 매끄러웠다" 응답 | 57% | [The Next Web](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion) |

The Next Web 기사는 경쟁사 Hi Auto(보장글스 파트너) 중심으로 쓰여, 비교 수치를 감안해서 봐야 한다.

## 논란과 사건

가장 큰 전환점은 2025년 8월 29일 WSJ 보도다. 이미 돌던 장난·오작동 영상들이 경영진의 "재검토" 발언과 결합하며 전 세계 기사로 번졌다.

### 1. "물 18,000잔" 장난

- **내용:** 한 고객이 AI에게 물 18,000잔을 주문해 시스템을 멈추게 했고, 결국 사람 직원이 개입했다. 사람과 통화하려고 일부러 한 것이라는 해석도 있다 ([TechCrunch](https://techcrunch.com/2025/08/30/taco-bell-is-having-second-thoughts-about-relying-on-ai-at-the-drive-through/), [Cybernews](https://cybernews.com/entertainment/taco-bell-ai-drive-thru-prank/))
- **플랫폼:** Futurism은 Facebook, Jalopnik은 YouTube로 전한다. 최초 게시자·날짜는 어느 출처에서도 확인되지 않는다 ([Futurism](https://futurism.com/taco-bells-ai-drive-thru), [Jalopnik](https://www.jalopnik.com/1956939/taco-bell-drive-through-18000-waters/))
- **기록:** AI Incident Database에 Incident 1274로 등재. 개발사는 Omilia로 명시 ([AIID](https://incidentdatabase.ai/cite/1274/))

### 2. "라지 마운틴듀" 영상

- 2024년 11월 TikTok @haleyduffhehe. 음료를 말했는데도 AI가 "음료는요?"를 반복해 운전자가 소리를 지르고 떠난다. 조회수 790만 ([Daily Dot](https://dailydot.com/taco-bell-ai-fail))
- Instagram에도 라지 마운틴듀를 시킨 고객에게 "같이 드실 음료"를 묻는 영상이 퍼졌다 ([Jalopnik](https://www.jalopnik.com/1956939/taco-bell-drive-through-18000-waters/))

### 3. 기타 오작동 사례

- 주문 루프, 타코벨에서 맥도날드 메뉴 주문을 받아준 사례가 TikTok에 올라왔다 ([AOL/CNET](https://www.aol.com/2-million-ai-orders-taco-213600853.html))
- CNET 편집장 데이비드 카츠마이어는 직접 주문해 보니 대부분 틀렸고, 목소리를 높이자 "처음부터 듣고 있었다"며 직원이 끼어들었다고 적었다 ([AOL/CNET](https://www.aol.com/2-million-ai-orders-taco-213600853.html))
- Intouch 조사 중 한 고객: "칩스와 웍을 원했는데 AI가 치즈와 칩스로 알아듣고 수정해주지 않았다" ([Intouch Insight](https://www.intouchinsight.com/blog/drive-thru-trends))

### 4. 경영진 발언과 대응

- 데인 매튜스(CDTO): "솔직히 말해 많이 배우고 있다. 다들 그렇듯 실망할 때도, 놀랄 때도 있다." "가맹점과 함께 매우 활발히 논의 중" ([AOL/CNET](https://www.aol.com/2-million-ai-orders-taco-213600853.html))
- 대응: 매장·시간대별로 AI 사용 또는 사람 모니터링을 코칭하고, 초바쁜 매장은 사람이 받는 하이브리드 방식을 검토 ([TechCrunch](https://techcrunch.com/2025/08/30/taco-bell-is-having-second-thoughts-about-relying-on-ai-at-the-drive-through/))
- 철수 여부: 많은 헤드라인이 "철수·중단"으로 썼지만, 회사는 확장 계획을 거두지 않았고 2026년 7월 890곳으로 늘렸다 ([Food On Demand](https://foodondemand.com/09242025/it-seems-every-brand-wants-to-use-voice-ai-yet-taco-bell-is-pulling-back/), [NRN](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants))

## 소셜미디어·여론 반응

여론의 중심은 조롱과 피로감이지만, 현장 직원 쪽에서는 "사람이 감독하는 AI"라면 환영한다는 목소리도 나온다.

| 채널 | 반응 | 출처 |
|---|---|---|
| TikTok | "라지 마운틴듀" 영상 790만 뷰. "100% 정당한 폭발", "그냥 마운틴듀가 갖고 싶었을 뿐" 등 공감 댓글. 관련 태그·모방 영상 다수 | [Daily Dot](https://dailydot.com/taco-bell-ai-fail), [TikTok 태그](https://www.tiktok.com/discover/taco-bell-ai-drive-thru-mtn-dew) |
| Facebook·YouTube·Instagram | "물 18,000잔", "음료와 함께 음료" 등 장난·오작동 클립 확산. 밈 커뮤니티에서 BBC 기사 공유 | [Futurism](https://futurism.com/taco-bells-ai-drive-thru), [Jalopnik](https://www.jalopnik.com/1956939/taco-bell-drive-through-18000-waters/), [Facebook](https://www.facebook.com/groups/feralneurodivergentragingmemeposting/posts/1246514607382015/) |
| Hacker News | BBC 기사 "Taco Bell rethinks AI drive-through after man orders 18,000 waters" 토론 스레드 | [Hacker News](https://news.ycombinator.com/item?id=45065391) |
| Stacker News | 여러 드라이브스루를 사람이 원격 감독하는 "감독형 AI" 제안, 현직 직원의 "AI 환영, 단 사람 감독은 필요" 의견, 자동화 회의론 | [Stacker News](https://stacker.news/items/1198493) |
| 포럼 | TigerDroppings 등 일반 커뮤니티에서도 BBC 기사 확산 | [TigerDroppings](https://www.tigerdroppings.com/rant/o-t-lounge/taco-bell-rethinks-ai-drive-through-after-man-orders-18000-waters/119890320/) |
| 언론 논조 | AV Club은 "타코벨이 AI가 좀 별로라고 인정"이라고 풍자. The Register는 "결국 인건비 문제"라고 비판 | [AV Club](https://www.avclub.com/taco-bell-ai-drive-thru-bad), [The Register](https://www.theregister.com/2024/08/01/ai_taco_bell/) |

**소비자 설문 데이터**

- 응답자 1,004명 중 선호 주문 방식: 사람 34%, 모바일 앱 31%, AI 음성 14% ([Kiosk Industry](https://kioskindustry.org/voice-ai-drive-thru-guests/), 2026-07)
- Intouch 2025: AI 음성주문을 싫다는 응답 45%, 실제 이용 경험 19% (같은 출처)

## 논문·분석·업계 비교

학술 연구는 아직 드물고, 타코벨 사례는 주로 컨설팅·업계 분석에서 "AI 도입 실패·교훈" 사례로 인용된다.

**학술 논문**

- [From human to AI: Understanding the impact of voice AI on consumers' food choices](https://www.sciencedirect.com/science/article/abs/pii/S0278431925004657) — Peng·Yu·Mattila, *International Journal of Hospitality Management* 134권(2026). 음성 AI로 주문하면 사람에게 주문할 때보다 고칼로리 메뉴를 더 고른다. 원인은 인지적 고갈, 아바타를 붙이면 효과가 줄어든다. 타코벨 특정 연구는 아니다. 실험 수는 초록 5개, Penn State 보도자료 3개로 다르다 ([Penn State](https://www.psu.edu/news/health-and-human-development/story/fries-ordering-ai-linked-selecting-more-indulgent-foods))

**분석·칼럼**

- [Taco Bell, 18,000 Waters & Why Benchmarks Don't Matter](https://www.cutter.com/article/taco-bell-18000-waters-why-benchmarks-don%E2%80%99t-matter) — Arthur D. Little(Cutter), 2025-10-13. 모델 성능보다 업무 규칙·데이터·워크플로 통합 실패가 문제라는 주장
- [Wendy's beat Taco Bell at customer-facing AI](https://aiadopters.club/p/wendys-beat-taco-bell-at-customer) — Kamil Banc, 2026-05-07. 웬디스는 사람 에스컬레이션을 처음부터 설계에 넣었고, 타코벨은 개입을 실패로 본 것이 차이라는 분석
- [AI Incident Database #1274](https://incidentdatabase.ai/cite/1274/) — 사건 공식 기록
- 그 외(검색으로만 확인, 본문 미열람): [Medium 분석](https://medium.com/@ashutosh_veriprajna/someone-ordered-18-000-cups-of-water-from-a-taco-bell-ai-and-it-said-yes-10bebdbcde0d), [Forbes](https://www.forbes.com/sites/kolawolesamueladebayo/2026/02/03/how-voice-ai-went-from-taking-notes-to-running-drive-thrus/), [Winsome Marketing](https://winsomemarketing.com/ai-in-marketing/tacobell-rethinks-ai-after-man-orders-18000-waters)

**경쟁사 비교**

| 브랜드 | 파트너 | 상태 | 출처 |
|---|---|---|---|
| 타코벨 | Omilia (+Nvidia) | 890곳+ (2026-07), 하이브리드 운영 | [NRN](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants) |
| 웬디스 | Google | 2025년 500곳+, 자율 처리 86% 주장 | [AI Adopters Club](https://aiadopters.club/p/wendys-beat-taco-bell-at-customer) |
| 맥도날드 | IBM | 2024년 6월 100곳+ 테스트 종료. 이후 새 음성 AI 재도전 보도 | [NBC News](https://www.nbcnews.com/business/business-news/taco-bell-roll-ai-drive-thru-ordering-hundreds-locations-end-year-rcna164524), [Entrepreneur](https://www.entrepreneur.com/buying-a-franchise/taco-bell-is-replacing-drive-thru-workers-with-ai) |
| 보장글스 | Hi Auto | 400곳+, 개입률 3% 주장 | [The Next Web](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion) |

## 추가 조사 (9월 23일)

2026년 확대를 가능하게 한 기술은 "더 큰 모델"이 아니라 드라이브스루 전용 소형 언어모델과 운영 방식 변경이었다. 위 본문에 없던 디테일만 모았다.

**Omilia 기술 디테일 (2026년 7월 발표)**

- 자체 소형 언어모델로 초저지연·문맥 기반 인식, 응답은 1초 미만 ([Restaurant Dive](https://www.restaurantdive.com/news/taco-bell-omilia-drive-thru-ai-deployment/824564/), [NRN](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants))
- 슬랭·농담·주문 중간 변경·복잡한 커스터마이징을 정해진 스크립트 메뉴 없이 처리
- 도로 소음 필터링, 억양 적응, 매장별 메뉴와 실시간 재고 반영
- 2023년부터 38개 주 890곳+ 운영. 데인 매튜스: "일부 매장에서 규모의 검증을 끝냈다"

**경영진 발언 원문 (2025년 8~9월)**

- "I think like everybody, sometimes it lets me down, but sometimes it really surprises me" — 데인 매튜스 CDTO ([Benzinga](https://www.benzinga.com/news/restaurants/25/09/47436703/taco-bell-rethinks-drive-thru-voice-ai-after-prank-order-requests-18000-water-cups))
- "We'll help coach teams on when to use voice AI and when it's better to monitor or step in" — 같은 인터뷰
- 당시 발표한 변경: 매장별 AI 사용 맞춤화, 피크 시간 사람 개입 유지, 200만 건+ 주문 데이터로 효과 있는 곳과 없는 곳 구분

**업계 비교 보강 (The Next Web 보도 기준, 2차 인용)**

> 검증 필요: Intouch 원문 요약은 조사 대상을 버거킹·타코벨·웬디스로 적고 있어, 보장글스가 포함된 이 표가 같은 조사에서 나온 것인지 확인되지 않았다. 팩트체크 ① 전까지 사용 금지.

| 브랜드 | 파트너 | 직원 개입률 | "쉽고 매끄러웠다" |
|---|---|---|---|
| 보장글스 | Hi Auto | 3% | 67% |
| 타코벨 | Omilia | 30% | 57% |
| 웨디스 | Google | 33% | 23% |

Hi Auto는 약 1,000개 QSR 매장에서 연 1억 건+ 주문을 처리하고 대기 시간 40초 단축을 주장한다. 출처인 [The Next Web](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion) 기사는 Hi Auto 중심이라 비교 해석은 감안해야 한다. 웨디스의 낮은 만족도는 위 AI Adopters Club의 "웨디스가 앞섰다" 분석과 엇갈리므로, 글에서 웨디스를 모범 사례로 쓸 때는 "설계 철학"에만 한정하는 게 안전하다.

## 선행 콘텐츠 조사: 누가 이미 썼나

"물 18,000잔 = AI 실패"는 이미 많이 소비됐고, 2026년 890곳 확대라는 반전을 다룬 한국어 콘텐츠는 찾지 못했다. 구글에 노출된 글 기준이며, 링크드인 내부 검색은 직접 확인이 필요하다.

| 채널 | 시기 | 주로 다룬 각도 | 예시 |
|---|---|---|---|
| 해외 링크드인 | 2026년 7월 | 890곳 확대 뉴스 공유 수준(Omilia 직원, 외식업 기자) | [Danny Klein](https://www.linkedin.com/posts/dannyklein14_voice-ai-ordering-in-the-drive-thru-every-activity-7480960175668076544-OBog), [Brian Barr](https://www.linkedin.com/posts/brian-barr-47a529177_ai-voiceai-tacobell-activity-7480640507937812481-i6bO) |
| 해외 링크드인 | 2025년 8~9월 | 18,000잔 밈 + "사람 개입 필요", "AI 거버넌스" 교훈 | [Meredith Bailey](https://www.linkedin.com/posts/meredithabailey_humanintheloop-aigovernance-activity-7368321498836606979-UQgN), [W. Edwards](https://www.linkedin.com/posts/wedwards3_taco-bell-just-admitted-their-drive-thru-activity-7368678435184922624-a9J4), [Restaurant AI Podcast](https://www.linkedin.com/posts/restaurant-ai-podcast_someone-ordered-18000-cups-of-water-at-an-activity-7368991005015998468-1gJx) |
| 국내 언론 | 2025년 12월 | "음성 AI 드라이브스루가 뜻대로 안 되는 이유" 분석 | [네이트 뉴스 Case Story](https://m.news.nate.com/view/20251219n20327) (본문 미열람) |
| 국내 언론 | 2025년 9월 | "물 18000컵" 해프닝, "음성 AI 기대 이하" | [서울신문](https://www.seoul.co.kr/news/newsView.php?id=20250902500045), [디지털투데이](https://www.digitaltoday.co.kr/news/articleView.html?idxno=588712), [더피알](https://www.the-pr.co.kr/news/articleView.html?idxno=54056) |
| 국내 링크드인 | — | 검색되는 한국어 게시물 없음 | — |

**비어 있는 각도 (연재의 차별점)**

- 실패 이후의 이야기: 진단 → 재설계 → 890곳으로 이어지는 "진화" 관점
- 한국어로 된 정리
- 드라이브스루 음성주문을 직접 만든 사람의 관점(빠른국대버거 데모)

## 출처 목록

본문을 직접 열어 확인한 자료는 유형별로, 검색 결과로만 확인한 자료는 따로 묶었다.

**공식 발표·IR**

- [Yum! Brands to Expand Voice AI (Taco Bell Newsroom, 2024-07-31)](https://www.tacobell.com/newsroom/yum-brands-to-expand-voice-ai-technology)
- [Omilia Powers Taco Bell's Expansion (Business Wire, 2026-07-07)](https://www.businesswire.com/news/home/20260707542838/en/Omilia-Powers-Taco-Bells-Expansion-of-Voice-AI-Across-890-U.S.-Drive-Thrus)
- [Taco Bell Defy Concept Opens June 7 (Taco Bell, 2022)](https://www.tacobell.com/newsroom/taco-bell-defy-concept-opens-june-7-one-of-the-most-innovative-drive-thru-experiences-yet)
- [Yum! Appoints Chris Turner as CEO (Yum!, 2025)](https://investors.yum.com/news-events/financial-releases/news-details/2025/Yum-Brands-Appoints-Chris-Turner-as-Chief-Executive-Officer-Effective-October-1-2025/default.aspx)

**업계지·경제 기사**

- [NRN — Yum testing voice AI (2023-11-02)](https://www.nrn.com/quick-service/yum-brands-is-testing-voice-ai-beverage-automation)
- [NRN — Expanding voice AI test (2024-07-31)](https://www.nrn.com/quick-service/taco-bell-is-expanding-its-drive-thru-voice-ai-test)
- [NRN — Nearly 900 restaurants (2026-07-08)](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants)
- [NBC News (2024-07)](https://www.nbcnews.com/business/business-news/taco-bell-roll-ai-drive-thru-ordering-hundreds-locations-end-year-rcna164524)
- [Restaurant Dive — hundreds of US units (2024-07-31)](https://www.restaurantdive.com/news/taco-bell-expands-drive-thru-artificial-intelligence-hundreds-US-units/722874/)
- [Restaurant Dive — Yum·Nvidia (2025-03-19)](https://www.restaurantdive.com/news/yum-brands-nvidia-ai-taco-bell-pizza-hut-kfc-deal/742926/)
- [Restaurant Dive — Omilia deployment (2026-07-07)](https://www.restaurantdive.com/news/taco-bell-omilia-drive-thru-ai-deployment/824564/)
- [CX Dive (2024-11-08)](https://www.customerexperiencedive.com/news/taco-bell-puts-ai-drive-thru-strategy-staff-scheduling-q3/732283/)
- [PYMNTS (2024-11-05)](https://www.pymnts.com/restaurant-innovation/2024/yum-brands-leverages-voice-ai-and-data-for-personalized-service/)
- [Restaurant Business — Yum's future is AI](https://www.restaurantbusinessonline.com/technology/taco-bell-parent-yum-brands-future-ai)
- [TechCrunch (2025-08-30)](https://techcrunch.com/2025/08/30/taco-bell-is-having-second-thoughts-about-relying-on-ai-at-the-drive-through/)
- [Food On Demand (2025-09-24)](https://foodondemand.com/09242025/it-seems-every-brand-wants-to-use-voice-ai-yet-taco-bell-is-pulling-back/)
- [QSR Magazine — fastest drive-thru (2025-10-06)](https://www.qsrmagazine.com/story/taco-bell-is-once-again-the-fastest-drive-thru-in-america/)
- [QSR Magazine — about 900 locations (2026-07-08)](https://www.qsrmagazine.com/story/taco-bell-now-has-drive-thru-ai-ordering-in-about-900-locations/)
- [Entrepreneur (2026-07-09)](https://www.entrepreneur.com/buying-a-franchise/taco-bell-is-replacing-drive-thru-workers-with-ai)
- [Yahoo Finance — Q1 2026 call](https://finance.yahoo.com/markets/stocks/articles/yum-brands-q1-earnings-call-190733000.html)
- [Yahoo Finance — AI 메뉴판 (2026-04-30)](https://finance.yahoo.com/sectors/technology/articles/taco-bell-drive-thru-menu-091601379.html)
- [Quartz — Q2 2026 (2026-07-30)](https://qz.com/yum-brands-q2-2026-earnings-taco-bell-cyclospora-073026)
- [The Next Web (2026-08-20)](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion)
- [CNBC — Go Mobile (2020-08-20)](https://www.cnbc.com/2020/08/20/taco-bell-unveils-new-design-with-more-drive-thrus-as-pandemic-permanently-shifts-how-we-order.html)

**테크·대중 매체**

- [Futurism (2025-08-29)](https://futurism.com/taco-bells-ai-drive-thru)
- [Cybernews (2025-08-29)](https://cybernews.com/entertainment/taco-bell-ai-drive-thru-prank/)
- [Jalopnik (2025-09-02)](https://www.jalopnik.com/1956939/taco-bell-drive-through-18000-waters/)
- [AV Club (2025-08-29)](https://www.avclub.com/taco-bell-ai-drive-thru-bad)
- [AOL/CNET — After 2 Million AI Orders](https://www.aol.com/2-million-ai-orders-taco-213600853.html)
- [The Register (2024-08-01)](https://www.theregister.com/2024/08/01/ai_taco_bell/)
- [Daily Dot (2024-11-11)](https://dailydot.com/taco-bell-ai-fail)

**조사·논문·분석**

- [Intouch Insight 2025 Drive-Thru Study](https://www.intouchinsight.com/blog/drive-thru-trends)
- [Kiosk Industry — consumer survey (2026-07-16)](https://kioskindustry.org/voice-ai-drive-thru-guests/)
- [IJHM 논문 (ScienceDirect)](https://www.sciencedirect.com/science/article/abs/pii/S0278431925004657) · [Penn State 보도자료](https://www.psu.edu/news/health-and-human-development/story/fries-ordering-ai-linked-selecting-more-indulgent-foods)
- [Cutter / Arthur D. Little (2025-10-13)](https://www.cutter.com/article/taco-bell-18000-waters-why-benchmarks-don%E2%80%99t-matter)
- [AI Adopters Club (2026-05-07)](https://aiadopters.club/p/wendys-beat-taco-bell-at-customer)
- [AI Incident Database #1274](https://incidentdatabase.ai/cite/1274/)
- [Wikipedia — Taco Bell](https://en.wikipedia.org/wiki/Taco_Bell)

**소셜·커뮤니티**

- [Stacker News 토론](https://stacker.news/items/1198493)

**검색으로만 확인(본문 미열람 또는 접근 차단)**

- [BBC — Taco Bell rethinks AI drive-through](https://www.bbc.com/news/articles/ckgyk2p55g8o) · [Hacker News 스레드](https://news.ycombinator.com/item?id=45065391) · [TigerDroppings](https://www.tigerdroppings.com/rant/o-t-lounge/taco-bell-rethinks-ai-drive-through-after-man-orders-18000-waters/119890320/) · [Facebook 그룹 게시물](https://www.facebook.com/groups/feralneurodivergentragingmemeposting/posts/1246514607382015/)
- [CNBC 2024-07-31](https://www.cnbc.com/2024/07/31/taco-bell-to-roll-out-ai-drive-thru-ordering-in-hundreds-of-locations.html) · [CNBC 2025-03-18 Nvidia](https://www.cnbc.com/2025/03/18/taco-bell-parent-yum-brands-partners-with-nvidia-to-speed-up-use-of-ai.html) · [CNBC Q1 2026](https://www.cnbc.com/2026/04/29/yum-brands-yum-q1-2026-earnings.html)
- [MPR News — Defy](https://www.mprnews.org/story/2022/06/07/twostory-fourlane-taco-bell-drivethru-restaurant-opening-in-brooklyn-park) · [Axios — Defy](https://www.axios.com/2022/06/06/taco-bell-defy-brooklyn-park-minnesota) · [Taco Bell — Go Mobile](https://www.tacobell.com/newsroom/taco-bell-go-mobile) · [Restaurant Dive — Go Mobile](https://www.restaurantdive.com/news/taco-bell-is-launching-a-mobile-focused-double-drive-thru-model-in-2021/583856/)
- [TikTok 태그 페이지](https://www.tiktok.com/discover/taco-bell-ai-drive-thru-mtn-dew) · [Omilia 뉴스](https://omilia.com/resources/news/omilia-powers-taco-bells-expansion-of-voice-ai-across-890-us-drive-thrus/) · [Food On Demand 2026-07-29](https://foodondemand.com/07292026/taco-bell-expands-voice-ai-to-nearly-900-restaurants/) · [Omilia Series B (2026-08)](https://theaiinsider.tech/2026/08/19/omilia-secures-67m-in-series-b-funding-to-accelerate-global-expansion-of-its-agentic-self-learning-cx-platform-for-large-enterprises/)

**9월 23일 추가 출처**

- [Benzinga — Taco Bell rethinks drive-thru voice AI after 18,000 water cups](https://www.benzinga.com/news/restaurants/25/09/47436703/taco-bell-rethinks-drive-thru-voice-ai-after-prank-order-requests-18000-water-cups) (2025-09-01)
- [Restaurant Dive — Omilia deployment](https://www.restaurantdive.com/news/taco-bell-omilia-drive-thru-ai-deployment/824564/) (2026-07-07, 재확인)
- [NRN — Nearly 900 restaurants](https://www.nrn.com/quick-service/taco-bell-s-drive-thru-voice-ai-expands-to-nearly-900-restaurants) (2026-07-08, 재확인)
- [The Next Web — voice AI expansion](https://thenextweb.com/news/taco-bell-voice-ai-drive-thru-expansion) (2026-08-20, 재확인)
- 링크드인·국내 기사(검색 결과로만 확인): 위 "선행 콘텐츠 조사" 표의 링크
