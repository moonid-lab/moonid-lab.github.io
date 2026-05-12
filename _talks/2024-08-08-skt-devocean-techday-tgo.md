---
title: "AI Travel Agent, Travel GO(TGO) — SKT 데보션 테크데이 발표"
collection: talks
type: "Tech Day / Demo Booth"
permalink: /talks/2024-08-08-skt-devocean-techday-tgo/
venue: "제6회 SKT DEVOCEAN Tech Day"
date: 2024-08-08
location: "SKT타워 수펙스홀, 서울"
lang: ko
excerpt: "12주간의 데보션 오픈랩 LLMOps 스터디에서 출발한 AI 여행 에이전트 TGO(Travel GO)를 소개했습니다."
header:
  teaser: talks/skt-devocean-techday-tgo/demo-booth.jpg
links:
  - label: "행사 기사"
    url: "http://www.worktoday.co.kr/news/articleView.html?idxno=56197"
  - label: "발표 자료 PDF"
    url: "https://devocean.sk.com/vlog/TechDay/20240808_03.pdf"
---

<style>
.tgo-hero {
  margin: 0 0 2rem;
  padding: clamp(1.25rem, 3vw, 2rem);
  border-radius: 24px;
  background:
    radial-gradient(circle at 10% 10%, rgba(70, 140, 255, .32), transparent 32%),
    linear-gradient(135deg, #07152f 0%, #0d315f 48%, #176f8f 100%);
  color: #fff;
  box-shadow: 0 24px 60px rgba(7, 21, 47, .22);
}
.tgo-hero h2 {
  margin: .25rem 0 .75rem;
  color: #fff;
  font-size: clamp(1.85rem, 5vw, 3rem);
  letter-spacing: -.04em;
}
.tgo-eyebrow {
  margin: 0;
  color: #9fe8ff;
  font-size: .82rem;
  font-weight: 800;
  letter-spacing: .12em;
  text-transform: uppercase;
}
.tgo-hero p { color: rgba(255,255,255,.88); }
.tgo-badges, .tgo-actions {
  display: flex;
  flex-wrap: wrap;
  gap: .55rem;
  margin-top: 1rem;
}
.tgo-badge {
  display: inline-flex;
  align-items: center;
  border: 1px solid rgba(255,255,255,.26);
  border-radius: 999px;
  padding: .35rem .7rem;
  background: rgba(255,255,255,.10);
  color: #fff;
  font-size: .78rem;
  font-weight: 700;
}
.tgo-actions a {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  padding: .65rem .95rem;
  background: #fff;
  color: #0d315f;
  font-size: .85rem;
  font-weight: 800;
  text-decoration: none;
}
.tgo-actions a.secondary {
  background: rgba(255,255,255,.12);
  color: #fff;
  border: 1px solid rgba(255,255,255,.28);
}
.tgo-photo-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1rem;
  margin: 1.6rem 0 2rem;
}
.tgo-photo-grid figure {
  margin: 0;
  overflow: hidden;
  border-radius: 18px;
  background: #f6f8fb;
  box-shadow: 0 14px 35px rgba(20, 38, 70, .12);
}
.tgo-photo-grid img {
  display: block;
  width: 100%;
  aspect-ratio: 16 / 10;
  object-fit: cover;
}
.tgo-photo-grid figcaption {
  padding: .8rem .9rem;
  color: #536171;
  font-size: .82rem;
}
.tgo-card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(210px, 1fr));
  gap: 1rem;
  margin: 1.25rem 0 2rem;
}
.tgo-card {
  padding: 1rem;
  border: 1px solid #e8eef7;
  border-radius: 18px;
  background: linear-gradient(180deg, #fff, #f8fbff);
}
.tgo-card strong {
  display: block;
  margin-bottom: .35rem;
  color: #12365d;
}
.tgo-flow {
  padding: 1.2rem;
  border-left: 5px solid #1f8fd1;
  border-radius: 16px;
  background: #f3f9ff;
}
.tgo-source-note {
  color: #667085;
  font-size: .82rem;
}
</style>

<div class="tgo-hero">
  <p class="tgo-eyebrow">DEVOCEAN OpenLab · LLMOps Study Seminar</p>
  <h2>여행 준비의 복잡함을 AI Agent 팀으로 풀어낸 TGO</h2>
  <p>
    TGO(Travel GO)는 목적지 탐색, 장소 추천, 질문 답변, 일정표 생성을 하나의 여행 경험으로 묶는
    AI Travel Agent 프로젝트입니다. 데보션 오픈랩에서 12주간 쌓은 LLMOps·RAG·Agent 워크플로우를
    실제 서비스 프로토타입으로 연결해 <strong>제6회 SKT DEVOCEAN Tech Day</strong>에서 소개했습니다.
  </p>
  <div class="tgo-badges">
    <span class="tgo-badge">2024.08.08</span>
    <span class="tgo-badge">SKT타워 수펙스홀</span>
    <span class="tgo-badge">발표: 김하림</span>
    <span class="tgo-badge">AI Travel Agent</span>
    <span class="tgo-badge">GraphRAG · LLMOps</span>
  </div>
  <div class="tgo-actions">
    <a href="https://devocean.sk.com/vlog/TechDay/20240808_03.pdf" target="_blank" rel="noopener">발표 자료 보기</a>
    <a class="secondary" href="http://www.worktoday.co.kr/news/articleView.html?idxno=56197" target="_blank" rel="noopener">행사 기사 보기</a>
  </div>
</div>

<div class="tgo-photo-grid">
  <figure>
    <img src="/images/talks/skt-devocean-techday-tgo/demo-booth.jpg" alt="제6회 데보션 테크 데이 TGO 데모 부스 설명 현장">
    <figcaption>데보션 오픈랩 참여자들이 데모 부스에서 TGO(Travel GO)를 소개하는 현장.</figcaption>
  </figure>
  <figure>
    <img src="/images/talks/skt-devocean-techday-tgo/group-photo.jpg" alt="제6회 데보션 테크 데이 발표자 단체 사진">
    <figcaption>SKT타워 수펙스홀에서 진행된 제6회 데보션 테크 데이 발표자 단체 사진.</figcaption>
  </figure>
</div>

## 발표 배경

여행 준비는 목적지 추천, 일정 최적화, 숙박·교통 검색, 예산, 날씨, 체크리스트, 현지 정보, 실시간 후기처럼 서로 다른 정보가 동시에 필요한 문제입니다. 발표에서는 이 정보 과잉과 선택의 어려움을 **Agent가 목표를 이해하고, 필요한 도구를 호출하며, 피드백을 반영하는 워크플로우**로 해결하는 접근을 소개했습니다.

이번 행사는 SKT의 개발자 커뮤니티 DEVOCEAN이 운영한 오픈랩 결과 공유 자리였습니다. 기사에 따르면 102명의 개발자가 약 12주 동안 생성형 AI, 오픈 LLM, LLMOps 등 10개 스터디 프로그램에 참여했고, 테크데이에서는 TGO를 포함한 여러 AI 프로젝트 데모가 소개되었습니다.

## TGO가 해결하려는 문제

<div class="tgo-card-grid">
  <div class="tgo-card">
    <strong>정보 과잉 줄이기</strong>
    흩어진 여행 정보를 사용자 프로필과 의도에 맞게 선별합니다.
  </div>
  <div class="tgo-card">
    <strong>신뢰 가능한 추천</strong>
    DB에 저장된 실제 장소 정보와 검색·RAG 기반 근거를 활용해 추천 이유를 설명합니다.
  </div>
  <div class="tgo-card">
    <strong>여행 맥락 유지</strong>
    목적지, 출발지, 동행, 날짜, 관심사를 기억하고 다음 행동으로 자연스럽게 연결합니다.
  </div>
  <div class="tgo-card">
    <strong>서비스화 가능성</strong>
    OTA·여행사 연계, 원클릭 결제, 맞춤형 상품 제안 등 비즈니스 확장 시나리오를 검토했습니다.
  </div>
</div>

## Agent Team 구성

TGO는 하나의 거대한 챗봇이 아니라 역할이 나뉜 **Agent Team**으로 설계되었습니다.

1. **TGO 팀장 Agent** — 사용자 요청을 해석하고 적합한 전문 Agent에게 작업을 위임합니다.
2. **장소 추천 Agent** — 실제 장소 DB와 검색 정보를 바탕으로 숙소·관광지·맛집을 추천합니다.
3. **질문 답변 Agent** — 예약 가능 여부, 현지 정보 등 여행 관련 질문에 신뢰 가능한 답을 제공합니다.
4. **일정표 생성 Agent** — 동선과 관심사를 고려해 최적화된 일정, 체크리스트, 여행 팁을 생성합니다.

<div class="tgo-flow">
  <strong>Workflow</strong><br>
  사용자 요청 → TGO 팀장 Agent의 의도 분류 → 전문 Agent 위임 → DB/인터넷 검색 및 GraphRAG → 추천·답변·일정 생성 → 사용자 피드백 반영
</div>

## 데모 시나리오 하이라이트

- **도쿄 가족 여행 숙소 추천**: 아이와 함께하는 여행, 날짜, 관심사, SKT 고객 혜택을 함께 고려해 가족 친화 호텔과 할인 가능 숙소를 제안했습니다.
- **교토 식당 예약 가능 여부 질의응답**: 여행 관련 질문인지 먼저 판단하고, 수집한 정보의 출처를 확인한 뒤 예약 방법과 사전 예약 팁을 안내했습니다.
- **오키나와 탐조 여행 일정표 생성**: 탐조 관심사를 중심으로 장소를 찾고, 동선을 고려한 일정과 맞춤형 체크리스트를 구성하는 흐름을 시연했습니다.

## 느낀 점

TGO 발표의 핵심은 “LLM을 공부했다”에서 멈추지 않고 **실제 사용자가 겪는 여행 준비의 불확실성**을 서비스 관점에서 재구성했다는 점입니다. Agent, RAG, LLMOps, 비용 최적화, 모니터링 같은 기술 주제를 하나의 고객 여정으로 엮으면서, 학습 프로젝트가 프로덕트 실험으로 확장될 수 있음을 보여준 사례였습니다.

## 참고 자료

- [SKT 데보션 테크데이 행사 기사](http://www.worktoday.co.kr/news/articleView.html?idxno=56197)
- [TGO 스터디 세미나 발표 자료 PDF](https://devocean.sk.com/vlog/TechDay/20240808_03.pdf)

<p class="tgo-source-note">사진 출처: 워크투데이 행사 기사 제공 이미지. 페이지 내용은 공개 기사와 DEVOCEAN 발표 자료를 바탕으로 정리했습니다.</p>
