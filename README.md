# AetherForge

**Enterprise AI control plane — twelve production systems, one coherent product.**

AetherForge turns the twelve AI-engineer builds that actually get $150k–$200k interviews into a single installable platform. It is not twelve toy repos. It is one operating system: a gateway in front, cost and cache in the hot path, RAG / SQL / prompts as features, and regression, forensics, arbitration, docs, fine-tunes, and flags as the control plane that keeps those features honest after deploy.

Source reel: [Bashiri Smith — 12 AI Engineer projects](https://www.facebook.com/share/r/1ERDzwWu2f/) (Facebook video `1413290347355555`).

## The twelve products

| # | Product | What ships |
| --- | --- | --- |
| 1 | **Model Regression Detection** | Golden-set CI for prompts and models. Alerts before users see a quality drop. |
| 2 | **LLM Cost Autopilot** | Routes each request to the cheapest model that still clears a quality floor. |
| 3 | **Failure Forensics** | Traces multi-step pipelines, pins the first bad span, grows an eval set from failures. |
| 4 | **Self-Healing Docs** | Diffs public code symbols against markdown and drafts a correction patch. |
| 5 | **Output Arbitration** | Competing critic models → one confidence-scored verdict with callouts. |
| 6 | **Hybrid RAG** | Dense + sparse retrieval, rerank, citation-bearing answers over internal docs. |
| 7 | **Semantic Cache** | Serves near-duplicate prompts from cache. Cuts latency and vendor spend. |
| 8 | **Text-to-SQL Guardrails** | Natural language → `SELECT` only. Blocks destructive SQL. Checks schema grounding. |
| 9 | **Prompt Versioning / A/B** | Prompts as versioned artifacts. Traffic split. Wilson-score winner declaration. |
| 10 | **LoRA Fine-Tune Pipeline** | Domain dataset → adapter artifact + base-vs-tuned lift report. |
| 11 | **LLM Gateway** | Per-team rate limits, daily budgets, provider fallback, request traces. |
| 12 | **AI Feature Flags** | Percentage rollout for model-backed features. Auto-rollback on quality drop. |

## Quick start

```bash
python -m venv .venv && source .venv/bin/activate
pip install -e ".[dev]"
python -m aetherforge.cli demo
pytest
python -m aetherforge.cli serve --port 8080
```

Apache-2.0. Engineering reference platform, not a hosted service.
