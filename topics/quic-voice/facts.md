# 팩트 시트: 음성 에이전트 전송 방식 (WebSocket · WebRTC · QUIC/WebTransport)

> 2026-09-30 QC-1 2단계 작성. 모든 항목은 이날 원문 페이지를 직접 열어 확인한 내용이다.
> 등급은 3단계(팩트체크 ①)에서 매긴다. 5단계 이후에는 이 파일에서 "사용 가능" 등급으로 확정된 사실만 쓴다.
> "1차"는 표준 문서(RFC·W3C)·회사 공식 문서, "2차"는 업체 블로그·개인 분석이다.
> 원문은 대부분 영어이며, "원문 표현"은 원문 문장을 짧게 옮긴 것이다.
> 조사 도구 한계: 표준 문서 원문을 셸로 받을 수 없어 웹 페이지 열람으로 확인했다. 3단계에서 문구를 다시 대조한다.

## 팩트 목록

### A. 세 방식의 기본 구조

| 번호 | 사실(한 줄) | 원문 표현(짧게) | 대상·기준·표본·시점 | 출처 URL | 1차/2차 | 등급 | 쓸 때 주의 |
|---|---|---|---|---|---|---|---|
| F1 | WebSocket은 TCP 위에서 동작하는 프로토콜이다 | "The WebSocket Protocol is an independent TCP-based protocol" / "layered over TCP" | RFC 6455, 2011-12 | https://www.rfc-editor.org/rfc/rfc6455.html | 1차(표준) | 확인 | |
| F2 | WebRTC 표준은 엔드포인트가 ICE(완전 구현), TURN, DTLS-SRTP 키 교환, SCTP over DTLS over ICE를 모두 지원하도록 요구한다 | "ICE MUST be supported… full ICE implementation, not ICE-Lite" / "TURN MUST be supported" / "Key exchange MUST be done using DTLS-SRTP" / "MUST support SCTP over DTLS over ICE" | RFC 8835 "Transports for WebRTC", 2021-01 | https://www.rfc-editor.org/rfc/rfc8835.html | 1차(표준) | 확인 | "무겁다"는 성민님 판단. 이 사실은 "구성 요소가 많다"까지만 뒷받침 |
| F3 | OpenAI는 WebRTC가 ICE·NAT 통과, DTLS·SRTP 암호화, 코덱 협상, RTCP 품질 제어, 에코 제거·지터 버퍼를 제공한다고 설명했다 | "ICE for connectivity establishment and NAT traversal, DTLS and SRTP… codec negotiation… RTCP… echo cancellation and jitter buffering" | OpenAI 기술 블로그, 2026-05-04 | https://openai.com/index/delivering-low-latency-voice-ai-at-scale/ | 1차(회사 발표) | 확인(회사 발표) | WebRTC의 **장점**으로 공정하게 쓸 재료 |
| F4 | QUIC 표준은 흐름 제어되는 스트림, 저지연 연결 수립, 네트워크 경로 이전을 제공한다고 정의한다 | "flow-controlled streams… low-latency connection establishment, and network path migration" | RFC 9000 초록, 2021-05, 표준 트랙 | https://www.rfc-editor.org/rfc/rfc9000.html | 1차(표준) | 확인 | |
| F5 | WebTransport는 HTTP/3 위에서 동작하며, 스트림(신뢰 전송)과 UDP 같은 데이터그램(비신뢰 전송)을 모두 지원한다. MDN은 "WebSocket의 현대적 업데이트"라고 소개한다 | "a modern update to WebSockets… using HTTP/3 Transport… reliable transport via streams and unreliable transport via UDP-like datagrams" | MDN 문서, 2026-09-25 수정본 | https://developer.mozilla.org/en-US/docs/Web/API/WebTransport_API | 1차(표준 문서 해설) | 확인 | HTTP/3는 QUIC 위에서 동작 → "WebTransport = QUIC 기반"은 F4·F5를 이어 설명 가능 |

### B. 패킷을 잃어버렸을 때

| 번호 | 사실(한 줄) | 원문 표현(짧게) | 대상·기준·표본·시점 | 출처 URL | 1차/2차 | 등급 | 쓸 때 주의 |
|---|---|---|---|---|---|---|---|
| F6 | TCP 위의 HTTP/2에서는 패킷 하나가 유실·순서 뒤바뀜을 겪으면, 그 패킷과 무관한 요청까지 모두 멈춘다 | "a lost or reordered packet causes all active transactions to experience a stall regardless of whether that transaction was directly impacted" | RFC 9114(HTTP/3) 1.1절, 2022-06 (3단계에서 절 번호 정정: 1.2→1.1) | https://www.rfc-editor.org/rfc/rfc9114.html | 1차(표준) | 확인 | 원문 맥락은 HTTP/2. WebSocket 음성에 그대로 적용하는 건 해석 → F8과 함께 쓸 것 |
| F7 | QUIC은 한 연결 안에서 여러 스트림을 돌려도 스트림 사이에 head-of-line blocking이 없다 | "run multiple streams over a single connection without head-of-line blocking between streams" | RFC 9308, 2022-09, 정보 문서 | https://www.rfc-editor.org/rfc/rfc9308.html | 1차(표준) | 확인 | "스트림 **사이**"의 막힘이 없다는 뜻. 한 스트림 안의 유실은 그 스트림에서는 기다림 |
| F8 | 한 분석(LiveKit)에 따르면, TCP는 패킷이 유실되면 스트림을 멈추고 재전송한 뒤에야 다음 데이터를 넘기며, 이는 오디오에 치명적이다 | "TCP pauses the stream and retransmits it before delivering anything that came after… for audio, it's devastating" | LiveKit 블로그(Chris Wilson), 2026-03-23 | https://livekit.com/blog/why-webrtc-beats-websockets-for-voice-ai-agents | 2차(업체 분석) | 해석 | LiveKit은 WebRTC 업체. "한 분석에 따르면" |
| F9 | QUIC 확장 표준은 유실돼도 재전송하지 않는 데이터그램을 정의하며, 오디오·비디오 스트리밍, 게임 같은 실시간 앱에 유용하다고 밝힌다 | "DATAGRAM frames are not retransmitted upon loss detection" / "useful for optimizing audio/video streaming applications, gaming applications, and other real-time network applications" | RFC 9221, 2022-03, 표준 트랙 | https://www.rfc-editor.org/rfc/rfc9221.html | 1차(표준) | 확인 | 음성에 "재전송 기다리지 않는 경로"가 있다는 근거 |
| F10 | 한 분석(moq.dev)에 따르면, WebRTC는 지연을 낮추려고 오디오 패킷을 공격적으로 버린다 | "WebRTC aggressively drops audio packets to keep latency low" | moq.dev 블로그(kixelated), 2026-05-05 | https://moq.dev/blog/webrtc-is-the-problem/ | 2차(개인 분석) | 해석 | 저자는 MoQ 개발자(이해관계). "한 분석에 따르면" |

### C. 연결 수립과 네트워크 전환

| 번호 | 사실(한 줄) | 원문 표현(짧게) | 대상·기준·표본·시점 | 출처 URL | 1차/2차 | 등급 | 쓸 때 주의 |
|---|---|---|---|---|---|---|---|
| F11 | QUIC은 암호 핸드셰이크와 전송 핸드셰이크를 합쳐 연결 수립 지연을 최소화한다 | "combined cryptographic and transport handshake to minimize connection establishment latency" | RFC 9000 7절 첫 문장, 2021-05 | https://www.rfc-editor.org/rfc/rfc9000.html | 1차(표준) | 확인 | 구체 왕복 횟수는 이 문장에 없음. rfc-editor·quicwg 두 경로에서 확인(datatracker 열람본은 이 문장이 잘려 보였음) |
| F12 | 한 분석(moq.dev)에 따르면, WebRTC 연결 수립에는 최소 8번의 왕복이 필요하고 QUIC+TLS는 1번이다 | "a minimum of 8* round trips (RTT) to establish a WebRTC connection" / "1 for QUIC+TLS" | moq.dev, 2026-05-05 | https://moq.dev/blog/webrtc-is-the-problem/ | 2차(개인 분석) | 해석 | 별표 각주 원문: "It's complicated to compute, because some protocols can be pipelined". 저자 계산이며 표준 수치 아님. 쓰려면 "한 분석에 따르면 최소 8번(계산 방식에 따라 다름)" |
| F13 | QUIC은 이전 연결을 재개할 때 0-RTT를 쓸 수 있어 재연결 지연을 줄인다 | "reconnection can use 0-RTT session resumption, reducing the latency involved with restarting the connection" | RFC 9308, 2022-09 | https://www.rfc-editor.org/rfc/rfc9308.html | 1차(표준) | 확인 | "가능할 때"(When possible) 조건 |
| F14 | QUIC 연결은 하나의 네트워크 경로에 묶이지 않으며, 연결 ID로 새 경로로 옮겨갈 수 있다 | "not strictly bound to a single network path. Connection migration uses connection identifiers" | RFC 9000 1절 개요·9절, 2021-05 | https://www.rfc-editor.org/rfc/rfc9000.html | 1차(표준) | 확인 | 와이파이↔LTE 전환은 이 사실의 **예시**로만. 원문에 그 표현 없음 |
| F15 | 연결 ID의 주된 기능은 하위 계층(UDP·IP) 주소가 바뀌어도 패킷이 엉뚱한 곳으로 가지 않게 하는 것이다 | "ensure that changes in addressing at lower protocol layers (UDP, IP) do not cause packets… to be delivered to the wrong endpoint" | RFC 9000 5.1절 | 위와 같음 | 1차(표준) | 확인 | |

### D. 운영·인프라

| 번호 | 사실(한 줄) | 원문 표현(짧게) | 대상·기준·표본·시점 | 출처 URL | 1차/2차 | 등급 | 쓸 때 주의 |
|---|---|---|---|---|---|---|---|
| F16 | OpenAI는 세션마다 포트 하나를 쓰는 전통적인 WebRTC 방식이 넓은 공개 UDP 포트 범위를 필요로 해서 쿠버네티스 환경에 잘 맞지 않는다고 밝혔다 | "one-port-per-session WebRTC model fits that environment poorly, because it depends on large public UDP port ranges that are difficult to expose, secure, and preserve" | OpenAI 기술 블로그, 2026-05-04 | https://openai.com/index/delivering-low-latency-voice-ai-at-scale/ | 1차(회사 발표) | 확인(회사 발표) | "회사 발표 기준". OpenAI는 이 문제를 **해결하고 WebRTC를 계속 씀**(F17) — 빼고 쓰면 왜곡 |
| F17 | OpenAI는 패킷 라우팅과 프로토콜 종단을 분리한 구조(릴레이+트랜시버)를 만들어 배포했다 | "splits packet routing from protocol termination… media enters through the relay first" | 위와 같음 | 위와 같음 | 1차(회사 발표) | 확인(회사 발표) | "WebRTC를 대규모로 쓰려면 별도 설계가 필요했다"까지는 사실, "그래서 무겁다"는 해석 |
| F18 | OpenAI가 밝힌 음성 인프라 요구사항: 주간 활성 사용자 9억 명 이상에 대한 전 세계 도달, 빠른 연결 수립, 낮고 안정적인 왕복 시간 | "Global reach for more than 900 million weekly active users" / "Fast connection setup…" / "Low and stable media round-trip time" | 위와 같음 | 위와 같음 | 1차(회사 발표) | 확인(회사 발표) | 9억은 OpenAI 전체 서비스 규모이지 음성 사용자 수가 아님 |
| F19 | 일부 측정 연구에 따르면 네트워크의 3~5%가 UDP 트래픽을 모두 막으며, QUIC 앱은 연결 실패를 감수하거나 다른 전송 방식으로 폴백하도록 설계해야 한다 | "between 3% [Trammell16] and 5% [Swett16] of networks block all UDP traffic" / "must either be prepared to accept connectivity failure… or be engineered to fall back" | RFC 9308 2절(2022-09)이 인용한 2016년 발표 2건: Trammell16(RIPE 72, 2016-05), Swett16(IETF96 "QUIC Deployment Experience @Google", 2016-07) | https://www.rfc-editor.org/rfc/rfc9308.html | 1차(표준)에 인용된 2차 측정 | 2차 인용 | **QUIC의 한계.** "RFC 9308에 따르면 2016년 측정에서" 식으로 출처·시점 표기 필수. 두 연구 수치를 합치거나 평균내지 말 것. 지금 비율로 쓰지 말 것 |

### E. 성숙도·지원 현황

| 번호 | 사실(한 줄) | 원문 표현(짧게) | 대상·기준·표본·시점 | 출처 URL | 1차/2차 | 등급 | 쓸 때 주의 |
|---|---|---|---|---|---|---|---|
| F20 | Safari 26.4에서 WebTransport 지원이 추가됐다 | "Safari 26.4 adds support for WebTransport" | WebKit 블로그, 2026-03-24 | https://webkit.org/blog/17862/webkit-features-for-safari-26-4/ | 1차(회사 발표) | 확인 | |
| F21 | 브라우저별 WebTransport 지원 시작 버전: Chrome 97, Firefox 114, Safari 26.4(macOS·iOS) | version_added: chrome 97 / firefox 114 / safari 26.4 (safari_ios는 safari와 같음) | MDN browser-compat-data + Can I use 교차 확인, 2026-09-30 열람 | https://github.com/mdn/browser-compat-data/blob/main/api/WebTransport.json | 1차(호환성 데이터) | 확인(범위 축소) | Edge·안드로이드·삼성 인터넷 버전은 두 출처 표기가 달라 제외(X3). 세부 기능별 지원은 다를 수 있음 |
| F22 | MDN은 WebTransport를 "Baseline 2026"으로 표시하며, 2026년 3월부터 최신 기기·브라우저에서 동작하고 구형에서는 안 될 수 있다고 적는다 | "Baseline 2026 … Since March 2026, this feature works across the latest devices and browser versions… might not work in older devices" | MDN, 2026-09-25 수정본 | https://developer.mozilla.org/en-US/docs/Web/API/WebTransport_API | 1차 | 확인 | "일부 기능은 지원 수준이 다를 수 있음" 단서 있음 |
| F23 | W3C WebTransport API 명세는 후보 권고(Candidate Recommendation) 단계다 | "W3C Candidate Recommendation Snapshot, 30 July 2026" | W3C, 2026-07-30 | https://www.w3.org/TR/webtransport/ | 1차(표준) | 확인 | 최종 권고(Recommendation) 아님 |
| F24 | IETF의 WebTransport over HTTP/3 프로토콜 문서는 아직 RFC가 아닌 인터넷 초안(-16)이며 워킹그룹 최종 검토 단계다 | "draft-ietf-webtrans-http3-16" / "In WG Last Call" | IETF datatracker, 2026-07-06 개정 | https://datatracker.ietf.org/doc/draft-ietf-webtrans-http3/ | 1차(표준화 기구) | 확인 | QUIC 자체(RFC 9000)는 2021년 표준. 구분할 것 |
| F25 | IETF MoQ 워킹그룹은 라이브 스트리밍·게임·미디어 회의용 저지연 미디어 전송을 개발 중이며, 아직 RFC가 된 문서는 없다(전송 문서 목표 2026-12) | "simple low-latency media delivery solution… live streaming, gaming, and media conferencing" | IETF datatracker MoQ WG, 2026-09-30 열람 | https://datatracker.ietf.org/group/moq/about/ | 1차(표준화 기구) | 확인 | MoQ ≠ WebTransport. Raixact와 혼동 금지 |
| F26 | 한 분석(moq.dev) 저자도 MoQ가 음성 AI에 딱 맞지는 않는다고 인정했다 | "MoQ isn't a perfect fit for Voice AI either… cache/fanout semantics are useless for 1:1 audio" | moq.dev, 2026-05-05 | https://moq.dev/blog/webrtc-is-the-problem/ | 2차(개인 분석) | 해석 | |

### F. 업계 선택 현황

| 번호 | 사실(한 줄) | 원문 표현(짧게) | 대상·기준·표본·시점 | 출처 URL | 1차/2차 | 등급 | 쓸 때 주의 |
|---|---|---|---|---|---|---|---|
| F27 | OpenAI Realtime API는 브라우저에서는 WebRTC, 서버에서는 WebSocket으로 연결하는 흐름을 안내하고, 전화용 SIP 가이드를 따로 둔다 | "The session connects over WebRTC in the browser or WebSocket on the server" | OpenAI 개발자 문서, 2026-09-30 열람 | https://developers.openai.com/api/docs/guides/realtime | 1차(회사 문서) | 확인 | |
| F28 | Google Gemini Live API는 WebSocket을 쓰는 상태 유지형 API이며, 서버·클라이언트 모두 WebSocket으로 연결한다(WebRTC는 제3자 통합으로 안내) | "The Live API is a stateful API that uses WebSockets." / "connects… using WebSockets" / "third-party integration… over WebRTC or WebSockets" | Google AI API 레퍼런스(2026-09-04 갱신) + Live API 가이드, 2026-09-30 열람 | https://ai.google.dev/api/live , https://ai.google.dev/gemini-api/docs/live | 1차(회사 문서) | 확인(수정) | 2단계 인용문("Stateful WebSocket connection (WSS)")은 재확인에서 찾지 못해 레퍼런스 문장으로 교체. 개발자용 API 기준이며 Gemini 앱 자체의 전송 방식과 다를 수 있음 |
| F29 | 한 분석(BlogGeek.me)에 따르면, 2026년 음성 AI의 실시간 전송은 거의 항상 WebRTC다 | "in 2026 that transport is almost always WebRTC" | BlogGeek.me(Tsahi Levent-Levi), 페이지에 날짜 표기 없음(본문상 2026년 작성) | https://bloggeek.me/voice-ai/ | 2차(전문가 분석) | 해석 | 저자는 WebRTC 전문 컨설턴트. "한 분석에 따르면" |
| F30 | 같은 분석은 "WebTransport는 초기 단계이고 Safari는 2026년에야 지원을 추가했다"고 평가했다 | "WebTransport is nascent. Safari only added support in 2026." | 위와 같음 | 위와 같음 | 2차(전문가 분석) | 해석 | "초기 단계"는 해석, Safari 부분은 F20으로 확인 가능 |
| F31 | 한 분석(webrtcHacks)은 음성 AI 전송 방식이 아직 정해지지 않았다고 보고, "WebSocket 위의 원시 미디어만은 아니길, 다만 WebRTC나 MoQ가 아닐 수도 있다"고 적었다 | "Hopefully something other than raw media over WebSocket, but it might not be WebRTC or MoQ" | webrtcHacks(Chad Hart), 2025-11-04 | https://webrtchacks.com/webrtc-vs-moq-by-use-case/ | 2차(전문가 분석) | 해석 | 원문 재대조 완료("My bet in 2030" 표 안의 문장). 2030년 전망임을 함께 밝힐 것 |
| F32 | 한 분석(LiveKit)은 WebSocket도 신호 교환, 텍스트 기반 AI, 실시간이 아닌 오디오 업로드에는 적합하다고 봤다 | "Signaling… Text-based AI interactions… Non-realtime audio" | LiveKit, 2026-03-23 | https://livekit.com/blog/why-webrtc-beats-websockets-for-voice-ai-agents | 2차(업체 분석) | 해석 | WebSocket의 장점으로 공정하게 쓸 재료 |

## 성민님 경험·회사 사실 (외부 출처 없음, 성민님 제공)

| 번호 | 내용 | 제공일 | 쓸 때 주의 |
|---|---|---|---|
| E1 | Raixact는 WebTransport(QUIC) 기반 통신 채널을 메인 채널로 쓴다 | 2026-09-30 | |
| E2 | 선택 이유: WebRTC는 너무 무겁고, WebSocket은 부족하다 | 2026-09-30 | 성민님 판단. 외부 사실(F2·F6·F16 등)과 섞어 "사실"처럼 쓰지 않기 |
| E3 | 팀이 동시 접속 200명 이상 화상회의 시스템을 직접 설계·개발했고, SFU도 직접 만들고 클라이언트 주요 사항도 설계했다 | 2026-09-30 | |
| E4 | 그 시스템이 현재 국내 협업 서비스의 화상회의로 쓰이고 있다 | 2026-09-30 | **서비스 실명 쓰지 않음**(계약 관계 불확실) |
| E5 | Raixact는 웹·안드로이드·아이폰 SDK를 갖추고 있다 | 2026-09-30 | |
| E6 | Raixact의 전송 방식별 성능 측정 결과는 없다 | 2026-09-30 | Raixact의 지연·끊김 우위 표현 금지. 백업 채널(폴백) 언급 안 함 |

## 제외 항목

| 번호 | 사유 |
|---|---|
| X1 | "Google Gemini Live(앱)는 raw QUIC/UDP 경로를 쓴다" — BlogGeek.me가 "appears to use"(그런 것 같다)라고만 썼고, 1차 출처를 찾지 못함. 확인 불가 |
| X2 | "WebSocket→WebRTC 전환 체험기"(dev.to 2편) — 개인 경험담, 조건이 제각각이라 팩트로 쓰지 않음 |
| X3 | WebTransport의 Edge·안드로이드 Chrome·삼성 인터넷 지원 시작 버전 — MDN 호환성 데이터와 Can I use 표기가 달라 출처 충돌. F21에서 제외 |

## 팩트체크 ① 결과

- 검증일: 2026-09-30
- 방법: 32개 항목 전부 원문을 다시 열어 인용문 존재 여부를 문장 단위로 대조. RFC는 rfc-editor.org와 datatracker.ietf.org(F11은 quicwg.org 추가) 두 경로로 확인. 브라우저 지원은 MDN 호환성 데이터와 Can I use 교차 확인.
- 결과: 32개 중 사용 가능 32개(단, 해석 8개는 "한 분석에 따르면" 필수, 2차 인용 1개는 출처·시점 표기 필수). 제외 3개(X1~X3).
  - 확인 23: F1–F7, F9, F11, F13–F18, F20–F25, F27, F28
  - 2차 인용 1: F19
  - 해석 8: F8, F10, F12, F26, F29–F32
  - 수정 3: F6 절 번호(1.2→1.1), F21 범위 축소(Edge·안드로이드 제외), F28 인용문 교체
- 성민님 승인: (대기)
