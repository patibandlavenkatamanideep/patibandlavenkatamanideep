# Venkata Manideep Patibandla

**AI/ML Engineer — LLM evaluation, agent reliability, production AI infrastructure**
New Haven, CT · [venkatamanideep.com](https://venkatamanideep.com/) · [LinkedIn](https://linkedin.com/in/manideep-analytics)

I work on one question:

> Did the system actually reason correctly, or did it just produce a right-looking answer?

Most of what I build is infrastructure for answering that honestly — evals that measure
repeatability rather than a single score, agents with scoped tools and audit trails, and
benchmarks that admit their own limits.

## What I'm building

| Project | What it does |
|---|---|
| **[evalseal](https://github.com/patibandlavenkatamanideep/evalseal)** · `pip install evalseal` | Reproducibility receipts for LLM evals. Runs an eval N times, reports per-case flip rates with confidence intervals, and seals the result — including the judge prompt, rubric and model — into a hash-linked, Ed25519-signed ledger. |
| **[memoryops-ai](https://github.com/patibandlavenkatamanideep/memoryops-ai)** | Governed memory runtime for AI assistants: policy-before-storage, context admission, deletion proofs, leakage evals. |
| **[RealDataAgentBench](https://github.com/patibandlavenkatamanideep/RealDataAgentBench)** | Benchmark for LLM data-science agents, scoring correctness, code quality, efficiency and statistical validity. 500 recorded runs across 14 models. |
| **[relayops](https://github.com/patibandlavenkatamanideep/relayops)** | Control plane for AI support agents: scoped routing, policy broker, approval queue, replay verification, human handoff. |
| **[trust-rag-finance](https://github.com/patibandlavenkatamanideep/trust-rag-finance)** | Financial RAG assistant with hybrid retrieval, citations, groundedness checks and audit logging. |
| **[CostGuard](https://github.com/patibandlavenkatamanideep/CostGuard)** · **[Tether](https://github.com/patibandlavenkatamanideep/Tether)** | LLM cost/reliability proxy with circuit breakers and provider fallback; durable execution with checkpoint and resume for long-running agents. |

## Things this work has actually shown

Not claims — measurements from the repos above, reproducible from committed recordings.

**The grader is often the unstable part, not the model.** Running the same eval five times:
an LLM-judged suite flipped the verdict on 5 of 20 cases, while the same model on
numerically-graded questions flipped 0 of 40. A single run reports one of those outcomes
and tells you nothing about which.

**A benchmark can rot without anyone touching it.** Auditing my own leaderboard: 24% of 500
recorded runs could no longer be reproduced — a provider had retired a model family, and an
SDK had removed a parameter the harness still sent. Nothing in the harness noticed, so the
leaderboard kept rendering those rows as if they still meant something.

**Most "model failures" I chase turn out to be eval defects.** Unanswerable questions,
ambiguous wording, and a scorer that counted markdown backticks as a wrong answer — each
looked like model instability until the runs were repeated and inspected.

## Stack

**Languages & ML** Python · SQL · PyTorch · scikit-learn · pandas · NumPy · SciPy
**LLMs & agents** OpenAI · Anthropic · Gemini · Llama · LangChain · LangGraph · RAG · LoRA
**Infrastructure** FastAPI · Docker · GitHub Actions · Postgres · Streamlit · Railway
**Evaluation** statistical validity · adversarial evals · cost tracking · observability · provenance

## Contact

[pvmanideep.analytics@gmail.com](mailto:pvmanideep.analytics@gmail.com) ·
[LinkedIn](https://linkedin.com/in/manideep-analytics) ·
[dev.to](https://dev.to/manideep_patibandla)
