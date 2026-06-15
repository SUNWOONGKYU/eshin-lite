# 에신-라이트

Claude Code용 **경량 에이전트 제조 스킬** ★ 별칭 **에신-라이트** — 본체 [에신](https://github.com/SUNWOONGKYU/llm-dependent-agent-create)의 경량판.

> 가볍고 단순한 **단일·로컬·저위험** LLM 에이전트를 빠르게 만들고 **자가검증으로 끝낸다.**
> 무거운 것(별도 Verification·고위험 도메인·포털·배치·운영 감시)은 만들지 않고 **본체 `/에신`으로 라우팅**한다.

## 본체 에신과의 차이
| | 에신-라이트 | 본체 [에신](https://github.com/SUNWOONGKYU/llm-dependent-agent-create) |
|---|---|---|
| 대상 | 단일·로컬·저위험·부품≤2 | 배치·포털·고위험·다부품 포함 전부 |
| 문답 | 간소(사소하면 생략) | 10라운드+α |
| 검증 | 자가검증 종결 | 별도 Verification·이중검증 |
| 인프라 | B(로컬 .py + 구독 CLI) | A(Supabase) / B |
| 산출 | 로컬 데스크톱 에이전트 | 9가지 구동 방식 |

→ **비중 있거나 위험하면 라이트가 아니라 본체.**

## 핵심 원칙
- **제작·검증은 항상 구독 LLM**(Claude Code 본체). API 키·크레딧은 *배포용 런타임*에만. (제작 ↔ 런타임 분리)
- **싸고 필수인 안전은 생략 안 함**: 실호출 1회 검증 · 보안 · BOM 안전진단(라이선스·시크릿) · 출력 정직 · 승인 게이트 · 에스컬레이션 트리거.
- **공정 L0→L6**: 적합성 판정 → 간소 문답(Trivial Fast-Path) → 승인 → 발굴·BOM → 제조 → 자가검증 → 출하.

## ⚡ 가장 빠른 설치 — Claude Code에게 시키기
본인 Claude Code 세션에 아래 한 줄을 붙여넣으세요.

> **"`SUNWOONGKYU/eshin-lite` 설치해 줘."**

## 직접 설치
```bash
git clone https://github.com/SUNWOONGKYU/eshin-lite.git
# macOS·Linux
cp -r eshin-lite/에신-라이트 ~/.claude/skills/
# Windows: cp -r eshin-lite/에신-라이트 "$env:USERPROFILE\.claude\skills\"
```
ZIP: 저장소 접속 → 녹색 `Code` → `Download ZIP` → `에신-라이트` 폴더를 `~/.claude/skills/` 안으로 복사.

## 설치 확인
```bash
ls ~/.claude/skills/ | grep 에신-라이트
```
새 세션에서 `/에신-라이트 [만들 에이전트 설명]`이 인식되면 정상.

## 라이선스
[MIT](LICENSE) — 자유롭게 fork·수정·재배포 가능.

---
🤖 Generated and maintained with Claude Code.
