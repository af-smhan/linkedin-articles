# 음성 에이전트 전송 방식 조사 기록

> 2026-09-30 작성(QC-1, 1/8 선행 콘텐츠 조사). 조사 기록이며 글에 쓸 사실의 기준이 아니다.
> 아래 내용은 원문을 WebFetch 요약으로 훑은 수준이다. 사실로 쓰려면 2~3단계에서 facts.md로 옮겨 원문 대조한다.

## 선행 콘텐츠 — 많이 소비된 각도

| 출처 | 날짜 | 입장 | 요지 |
|---|---|---|---|
| [OpenAI — Delivering low-latency voice AI at scale](https://openai.com/index/delivering-low-latency-voice-ai-at-scale/) | 2026-05-04 | WebRTC | 표준성(NAT 통과·암호화·코덱·지터 버퍼 내장), 말하는 도중 스트리밍. relay+transceiver 구조로 쿠버네티스에서 UDP 포트 문제 해결 |
| [moq.dev — OpenAI's WebRTC Problem](https://moq.dev/blog/webrtc-is-the-problem/) | 2026-05-05 | QUIC/MoQ | OpenAI 글 반박. WebRTC는 지연을 위해 오디오 패킷을 공격적으로 버림 → AI엔 정확한 입력이 중요. 연결 설정 왕복 수, 포트·방화벽, CONNECTION_ID로 IP 변경 처리, QUIC-LB. 저자(kixelated, MoQ 개발자) 스스로 입장이 주관적이고 MoQ도 1:1 음성엔 완벽하지 않다고 인정 |
| [LiveKit — Why WebRTC beats WebSockets](https://livekit.com/blog/why-webrtc-beats-websockets-for-voice-ai-agents) | 2026-03-23 | WebRTC | TCP head-of-line blocking, 지터 버퍼, SFU. QUIC 언급 없음 |
| [BlogGeek.me — WebRTC for Voice AI](https://bloggeek.me/voice-ai/) | 2026-06 | WebRTC | WebRTC가 사실상 표준. WebTransport는 초기 단계(Safari 2026 지원 추가 언급). Gemini Live 네이티브 앱은 raw QUIC 사용 언급 → 2단계 확인 필요 |
| [webrtcHacks — WebRTC vs MoQ by Use Case](https://webrtchacks.com/webrtc-vs-moq-by-use-case/) | 2025-11-04 | 유보 | 음성 AI 용도는 아직 정해지지 않음. "raw media over WebSocket만은 아니길" |
| dev.to 체험기 2편([1](https://dev.to/nick_lackman/i-tested-our-websocket-audio-pipeline-with-webrtc-heres-why-i-switched-it-back-3g1j), [2](https://dev.to/aws-builders/switching-my-ai-voice-agent-from-websocket-to-webrtc-what-broke-and-what-i-learned-3dkn)) | — | 혼재 | WebSocket→WebRTC 전환기, 되돌린 경험기 |

- 해외: "WebRTC vs WebSocket" 비교는 벤더 블로그로 포화. 결론은 대부분 WebRTC.
- QUIC 쪽 주장은 MoQ 진영(moq.dev) 중심으로 소수. 음성 에이전트를 실제 운영하는 회사가 QUIC을 택한 이유를 쓴 글은 찾지 못함.
- 국내: 한국어로 이 논쟁을 정리한 글·기사는 찾지 못함(GeekNews에 관련 번역 글 흔적만). 링크드인 내부 검색은 불가 — 성민님 직접 확인 필요.

## 비어 있는 각도(후보)
- 실제 음성 에이전트를 만드는 회사가 QUIC을 택한 이유와 측정 결과(1인칭).
- 비개발자 의사결정자 언어로 번역: 끊김, 말 끊기(barge-in), 이동 중 연결 유지, 방화벽.
- 적용 범위 명확화: 콜센터 전화(PSTN/SIP) 구간과 웹·앱 음성 채널 구간의 구분.

## 2단계에서 확인할 것
- Gemini Live의 QUIC 사용 여부(1차 출처)
- 브라우저 WebTransport 지원 현황(Safari 포함, 시점)
- QUIC 연결 설정 왕복 수, connection migration, 스트림별 head-of-line blocking 해소(RFC 9000 등 1차)
- WebRTC 연결 설정 왕복 수 주장(moq.dev)의 근거
