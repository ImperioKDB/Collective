# Collective - Project State

| Field | Value |
|---|---|
| Document ID | DOC-STATE |
| Last updated | 2026-11-18 |
| Updated by | Claude (P0.1 drafting session) |
| Rule | Update at the end of every task. Never mark work complete unless it was completed and verified. |

## 1. Current position

- **Current phase:** Phase 0 - Foundation
- **Current task:** P0.1 - Repository Reconnaissance and Product Requirements
- **P0.1 status:** **DRAFTED - IN REVIEW. NOT COMPLETE.** The four documents were drafted. Repository reconnaissance has not been performed (see section 4). Founder review and approval are pending.

## 2. Completed work

| Item | Status | Note |
|---|---|---|
| `CLAUDE.md` drafted | Drafted, not reviewed | Permanent engineering instructions |
| `docs/PROJECT_BRIEF.md` drafted | Drafted, not reviewed | Concise overview |
| `docs/PROJECT_STATE.md` drafted | Drafted, not reviewed | This file |
| `docs/PRODUCT_REQUIREMENTS.md` drafted | Drafted, not reviewed | 142 requirements: P0 58, P1 59, P2 19, P3 6 |
| Structural checks on the PRS | Performed | Scripted: unique IDs, valid priority and category values, five fields per requirement row, no references to undefined requirement, assumption or question IDs |

**Not performed:** any technical validation of any assumption; any test, benchmark or prototype; repository reconnaissance.

## 3. Decisions

### 3.1 Confirmed [DECISION] (from founder instructions)

1. Collective is a public SaaS platform with room for future enterprise deployment.
2. Modular, provider-neutral architecture.
3. Agent roles are model-independent.
4. Managed model access and BYOK.
5. Native and external agents.
6. Hybrid cloud and local execution.
7. Persistent project memory with permission-aware access.
8. Independent verification; permission-controlled autonomy.
9. Initial development is cloud-based; the founder uses an Android device and has no local computer.
10. Initial deployment on low-cost infrastructure.
11. Phase 0 includes no application feature implementation.

### 3.2 Awaiting validation (candidates, not final)

| Area | Candidate | Validate in |
|---|---|---|
| Frontend | Next.js, TypeScript | P0.2 |
| Backend | Python, FastAPI, Pydantic | P0.2 |
| Orchestration | LangGraph | P0.2 |
| Database and auth | Supabase PostgreSQL and Auth | P0.2 |
| Queue | PostgreSQL-backed queue or Supabase Queues | P0.2 |
| Tool protocol | MCP | P0.2 |
| External agent protocol | A2A | Before P2 |
| Hosting | Vercel; low-cost Python hosting | P0.2 |
| Execution | Isolated workers or sandboxes; authenticated local runner | P0.2 (cloud), later (local) |

No ADR exists yet. ADR creation begins in P0.2.

### 3.3 Proposed in P0.1, awaiting founder approval [RECOMMENDATION]

See section 5.

## 4. Known blockers and outstanding work

| ID | Item | Blocks |
|---|---|---|
| B-1 | **Repository reconnaissance not performed.** The drafting session had no access to the private repository. Existing branches, files, conventions and conflicts are unknown. Perform it with the publishing script's read-only check or manually, record findings in this file, and reconcile any conflict with the four documents before approval. | Approval of P0.1; any commit that could overwrite existing work |
| B-2 | OQ-002: operator keys first or BYOK in the MVP | P0.2 credential design |
| B-3 | OQ-004: monthly infrastructure and model-spend ceiling | P0.2 hosting decision |
| B-4 | OQ-005: durable long-running execution on low-cost hosting | P0.2 |
| B-5 | OQ-001 and OQ-008: reference scenario; meaning of "full autonomy" | P0.2 tool and security scope |
| B-6 | Founder review of the PRS, including the P0 set (58 of 142) | P0.1 approval |

Full question list: `docs/PRODUCT_REQUIREMENTS.md`, section 22.

## 5. Items requiring founder approval

1. The MVP definition and the sharpened proof (PRS section 19), including MVP-EVAL-001..003 and their provisional thresholds.
2. Sequencing BYOK after the MVP and using operator-held keys for invited users (MDL-007, MDL-008, EX-004). BYOK stays a confirmed product decision.
3. Sequencing the local runner to P2 (EXE-007, EX-002). Hybrid execution stays a confirmed direction.
4. The exclusion list (PRS section 20).
5. All provisional numeric targets marked *(prov.)*.
6. The reference scenario (OQ-001).
7. Using `docs/PROJECT_STATE.md` as the interim central document index (section 7). The master instructions require a central index; P0.1 specified four documents only. Approve this arrangement or approve a dedicated index file in P0.2.
8. Names and file locations of the four documents.

## 6. Next approved task

**P0.2 - Architecture evaluation and decision records. Approved subject to P0.1 review. Not started.**

Do not begin P0.2 until the founder approves P0.1.

## 7. Document index (interim, authoritative)

| ID | Path | Purpose | Status |
|---|---|---|---|
| DOC-CLAUDE | `CLAUDE.md` | Permanent engineering instructions for Claude sessions | Draft v0.1 |
| DOC-BRIEF | `docs/PROJECT_BRIEF.md` | Concise project overview | Draft v0.1 |
| DOC-STATE | `docs/PROJECT_STATE.md` | Continuity: phase, task, decisions, blockers, index | Draft v0.1 |
| DOC-PRS | `docs/PRODUCT_REQUIREMENTS.md` | Product requirements specification | Draft v0.1 |

No other project documents exist as of 2026-11-18, as far as this session could determine. Repository contents were not inspected (B-1).

## 8. Change log

| Date | Task | Change |
|---|---|---|
| 2026-11-18 | P0.1 | Initial drafts of the four documents. |
