# 홀로섬 MCP 서버 (준비 중)

> 상태: **준비 중** · 아직 연결할 수 없습니다. 도구 주소와 연결법은 공개 전에 확정합니다.
> 이 저장소의 내용은 참고용입니다. 계산 결과는 법령 원문과 계약 조건에 따라 달라질 수 있으며, 최종 판단과 책임은 이용자에게 있습니다.

## 홀로섬이란

홀로섬은 부동산 중개와 건물 관리 실무를 돕는 도구 모음입니다. 집합건물 관리 규약, 정족수 확인, 관리비와 유지보수비 같은 반복 업무를 화면과 AI 도구로 다룹니다.

English: Holosum is a set of tools for real-estate brokerage and building management in Korea. The MCP server exposes a small set of read-only calculation and lookup tools. The server is not yet open for use.

## 도구 (다섯)

| 번호 | 도구 이름(초안) | 무엇을 하나 | 미결 근거 | 상세 |
|---|---|---|---|---|
| 1 | 중개보수 한도 조회 | 거래 종류 · 거래 방식 · 금액을 넣으면 상한 기준 한도액을 돌려줍니다 | ②596 | [TOOLS.md](TOOLS.md) |
| 2 | 정족수 확인 | 구분소유자 수와 전유부분 면적 비율로 결의 정족수 충족 여부를 돌려줍니다 | ②596 목록 「정족수」 | [TOOLS.md](TOOLS.md) |
| 3 | 유지보수비 조회 | 참고용 유지보수비 비율을 돌려줍니다 | ②596 목록 「유지보수비」 · ②551 | [TOOLS.md](TOOLS.md) |
| 4 | 회원권 가치 환산 | 호텔 회원권의 수익형 · 시세 · 실가치를 한 화면에서 종합해 돌려줍니다 | ②597 | [TOOLS.md](TOOLS.md) |
| 5 | 안양 도시개발 추정 지도 | 지역 번호를 넣으면 지도 자료의 추정 범위를 돌려줍니다 | ②251 | [TOOLS.md](TOOLS.md) |

※ 미확인: 미결 ②596 은 «도구 다섯»이라고 하면서 괄호에 여섯 항목을 적었습니다. 「유지보수비」와 ②551(리츠 · 아파트 유지보수비 비율)을 한 도구로 볼지 두 도구로 볼지 사장님께 여쭙니다. 위 표는 한 도구로 본 초안입니다.
※ 도구 이름과 칸은 공개 전에 사장님이 확정합니다.

## MCP 연결법 (준비 중 · 초안)

공개 후에 다음 순서로 연결합니다. 실제 주소는 공개 때 적습니다.

### 클로드 (Claude)

1. 클로드 설정에서 커넥터(Connectors) 추가 화면을 엽니다.
2. 이름에 `홀로섬`, 주소에 MCP 서버 주소(`https://<공개 주소>/mcp`)를 넣습니다.
3. 인증이 필요하면 발급받은 열쇠를 넣습니다. 열쇠는 이용자 본인만 보관합니다.
4. 도구 목록이 보이면 연결이 끝난 것입니다.

### 챗지피티 (ChatGPT)

1. 설정의 앱(또는 커넥터) 항목에서 새 MCP 서버를 추가합니다.
2. 같은 주소와 열쇠를 넣습니다.
3. 대화창에서 도구를 고르고 질문합니다.

※ 두 화면의 메뉴 이름은 앱 업데이트에 따라 바뀔 수 있습니다. 공개 전에 최신 화면으로 다시 확인합니다.

## 예시 질문과 예시 결과 (꼴만 보여 줍니다)

예시 질문: "매매 거래로 주택 가격이 얼마일 때 중개보수 한도가 얼마인가요?"

예시 결과 꼴:

```
도구: 중개보수 한도 조회
입력: 거래 종류 = 주택, 거래 방식 = 매매, 거래 금액 = (이용자 입력)
출력: 상한 요율 = (확인 후 표시), 한도액 = (확인 후 표시)
안내: 참고용입니다. 최종 금액은 중개 계약과 관계 법령을 확인하십시오.
```

※ 실제 숫자 예시와 계산식은 싣지 않습니다. 결과 화면에는 계산 근거 요약만 표시합니다.

## 이용 조건

- 이 서비스는 참고용입니다. 법률 자문, 세무 자문, 투자 권유가 아닙니다.
- 결과를 근거로 한 거래와 신고의 책임은 이용자에게 있습니다.
- 요청 횟수에는 제한이 있습니다. 짧은 시간에 많이 요청하면 일시적으로 막힐 수 있습니다.
- 바깥 공공 자료를 쓰는 도구는 각 자료의 이용 조건을 따릅니다.
- 이용자가 입력한 값은 계산에만 씁니다. 개인을 알아볼 수 있는 정보(이름, 주소, 연락처)는 입력받지 않습니다.
- 처리 방침은 [PRIVACY.md](PRIVACY.md) 를 봅니다.

## 문의

- 이메일: ceopark@holosum.kr

## English summary

Holosum MCP server (not yet open). Five tools: brokerage fee ceiling lookup, quorum check for condominium resolutions, maintenance cost reference, public-data lookup with source and date, and site link guide. Results are for reference only. Personal information is not collected as input. Contact: ceopark@holosum.kr.
