# Luu Duc Hiep (`@bachiep`)

Software Engineering Intern Candidate focused on **Backend Engineering (Java 21 / Python FastAPI)**, **Cross-Platform Mobile (Flutter)**, and **Applied GenAI / RAG Systems**.

I build testable, concurrency-safe, container-ready applications backed by clean layered architecture, reproducible benchmarks, automated CI, and full Docker Compose smoke verification.

---

## Featured Engineering Portfolio (`v2.1.0`)

### 1. Backend Engineering (`Java 21` & `Python 3.13`)
| Project | Stack & Architecture | Key Engineering Highlights | Verification & CI |
| :--- | :--- | :--- | :--- |
| [**`flashsale-order-inventory-api`**](https://github.com/bachiep/flashsale-order-inventory-api) | Java 21 (Virtual Threads), Spring Boot 3.4, PostgreSQL 16, Redis 7, Flyway | Oversell-proof atomic SQL stock reservation, `Idempotency-Key` checkout (`SHA-256`), JWT rotation, Token-Bucket `429` rate limiting, Ops Console (`GET /`), fail-fast prod secret guard | `55/55` tests (`89%+` JaCoCo) · `0` oversells (`96.79` RPS) · [Release `v2.1.0`](https://github.com/bachiep/flashsale-order-inventory-api/releases/tag/v2.1.0) · [![CI](https://github.com/bachiep/flashsale-order-inventory-api/actions/workflows/ci.yml/badge.svg)](https://github.com/bachiep/flashsale-order-inventory-api/actions/workflows/ci.yml) |
| [**`slotguard-booking-api`**](https://github.com/bachiep/slotguard-booking-api) | Python 3.13, FastAPI, Async SQLAlchemy 2.0, Alembic, PostgreSQL 16, Redis 7 | Half-open `[start, end)` booking overlap guard, atomic reschedule, RFC-5545 `.ics` export, HMAC-SHA256 webhooks + Transactional Outbox, Timeline Lab (`GET /`) | `57/57` tests (`80.73%` `pytest-cov`) · `0` double-bookings · [Release `v2.1.0`](https://github.com/bachiep/slotguard-booking-api/releases/tag/v2.1.0) · [![CI](https://github.com/bachiep/slotguard-booking-api/actions/workflows/ci.yml/badge.svg)](https://github.com/bachiep/slotguard-booking-api/actions/workflows/ci.yml) |

### 2. Mobile Flutter (`Flutter 3.41` & `flutter_bloc`)
| App | Stack & Architecture | Key Engineering Highlights | APK & CI |
| :--- | :--- | :--- | :--- |
| [**`ledgerflow-flutter`**](https://github.com/bachiep/ledgerflow-flutter) | Clean Architecture, `flutter_bloc`, `Drift` SQLite, Supabase RLS | Offline-first fintech ledger, atomic wallet-to-wallet `transferAtomic` + `sync_outbox`, 6M `CustomPainter` trend charts, RFC-4180 formula-safe CSV export, OLED Dark | `62/62` tests · [APK `v2.1.0` (`54.7 MB`)](https://github.com/bachiep/ledgerflow-flutter/releases/tag/v2.1.0) · [![Flutter CI](https://github.com/bachiep/ledgerflow-flutter/actions/workflows/ci.yml/badge.svg)](https://github.com/bachiep/ledgerflow-flutter/actions/workflows/ci.yml) |
| [**`orderpulse-flutter`**](https://github.com/bachiep/orderpulse-flutter) | Clean Architecture, `flutter_bloc`, `Dio` Queued Refresh, WebSocket | Real-time KDS dispatch, `QueuedInterceptorsWrapper` single-flight refresh, `1s -> 16s` WS backoff, `Urgent SLA` sort + Prep-Item guard, 80mm thermal slip modal | `58/58` tests · [APK `v2.1.0` (`50.3 MB`)](https://github.com/bachiep/orderpulse-flutter/releases/tag/v2.1.0) · [![Flutter CI](https://github.com/bachiep/orderpulse-flutter/actions/workflows/ci.yml/badge.svg)](https://github.com/bachiep/orderpulse-flutter/actions/workflows/ci.yml) |

### 3. Applied AI / GenAI Engineering (`Python 3.13`, `Qdrant`, `evals/`)
| System | Pipeline & Guardrails | Key Engineering Highlights | Benchmarks & CI |
| :--- | :--- | :--- | :--- |
| [**`policylens-rag`**](https://github.com/bachiep/policylens-rag) | FastAPI, Qdrant, `fastembed` CPU ONNX, `rank-bm25` RRF | Bilingual EN/VI Hybrid RAG + Reranker, `AbstentionGuard` + citation span highlighter, A/B Retrieval Compare Studio, Colab T4 Cross-Encoder notebook | `Recall@5 = 1.0000` · `MRR@10 = 0.9821` · `Abstention = 1.0000` · [Release `v2.1.0`](https://github.com/bachiep/policylens-rag/releases/tag/v2.1.0) · [![CI](https://github.com/bachiep/policylens-rag/actions/workflows/ci.yml/badge.svg)](https://github.com/bachiep/policylens-rag/actions/workflows/ci.yml) |
| [**`orderops-agent`**](https://github.com/bachiep/orderops-agent) | FastAPI, Pydantic v2, SQLite (`BEGIN IMMEDIATE`), SSE | Bounded multi-turn tool agent, Closed-Loop HITL Supervisor queue (`session_messages` updates), `Idempotency-Key` guard, 3-Layer Prompt-Injection & Policy Gate, Colab T4 QLoRA notebook | `49/49` tests · `30/30` Eval Suite (`100%` Safety Block) · [Release `v2.1.0`](https://github.com/bachiep/orderops-agent/releases/tag/v2.1.0) · [![CI](https://github.com/bachiep/orderops-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/bachiep/orderops-agent/actions/workflows/ci.yml) |

---

## Core Tech Stack & Practices

- **Languages:** Java 21 LTS, Python 3.13, Dart 3.11, SQL (PostgreSQL 16 / SQLite WAL)
- **Frameworks:** Spring Boot 3.4, FastAPI, Flutter 3.41 (`flutter_bloc`, `Drift`, `Dio`), Pydantic v2
- **Infra & CI/CD:** Docker & multi-service `docker-compose`, GitHub Actions (`build-and-test`, `docker-smoke`, Android release APK builds), Flyway & Alembic migrations
- **Quality Bar:** Conventional Commits, Issue -> Branch -> PR review hygiene, >= 80% test coverage gates (JaCoCo & `pytest-cov`), non-root containers, offline deterministic + live evaluation harnesses

**Contact:** `hhkk77441@gmail.com` · GitHub: [@bachiep](https://github.com/bachiep)