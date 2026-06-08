# Hi, I'm Venkata Manideep 👋

**AI/ML Engineer · Forward Deployed Engineer · LLM Evaluation · Agentic AI Systems · Production AI Infrastructure**

I build AI systems that go beyond demos — systems that can be evaluated, monitored, routed safely, and trusted when they interact with tools or data.

My current work sits around:

* **LLM evaluation** — testing reasoning quality, statistical validity, and agent behavior
* **Agentic AI systems** — scoped tools, routing, RAG, guardrails, and human escalation
* **Production AI infrastructure** — reliability, cost control, observability, and deployment
* **Data science foundations** — statistical rigor, modeling, and evaluation design

I care about one question a lot:

> Did the system only produce the right-looking answer, or did it actually reason correctly and make a safe decision?

---

## What I'm Building

Right now, I’m focused on building and evaluating AI agents that are safer, cheaper, and more reliable in production settings.

Some themes I keep coming back to:

* agents that know when **not** to act
* evals that measure **reasoning**, not just final answers
* routing systems that optimize for **safety, reliability, and cost**
* RAG systems with **citations and groundedness checks**
* model/provider abstraction so systems are not locked to one LLM
* guardrails that are tested with adversarial cases, not just described in docs

---

## Featured Projects

### RealDataAgentBench

**LLM agent benchmark for statistically sound data science.**

RealDataAgentBench evaluates whether LLM agents can perform valid data science workflows — not just produce plausible-looking outputs.

**Highlights**

* 39 tasks across 5 data-science categories
* 12 frontier/open models
* 1,180+ benchmark runs
* full cost tracking
* scoring across correctness, code quality, efficiency, and statistical validity

**Key lesson**

Correct output does not always mean sound reasoning.

Repo: https://github.com/patibandlavenkatamanideep/RealDataAgentBench

---

### RelayOps

**Production-shaped AI customer-support agent for telecom/subscription support.**

RelayOps is an end-to-end vertical slice of a safer support agent. It handles customer turns through deterministic access control, scoped tools, intent routing, RAG, guardrails, and escalation.

**Highlights**

* deterministic access gate before model/tool execution
* scoped account/device tools
* tiered intent router
* fine-tuned Qwen2.5-1.5B LoRA classifier
* calibrated route-safety evals
* hybrid RAG with citations
* guardrails for pricing, offers, and PII
* live Streamlit demo on Railway

**Key lesson**

For agents that can take actions, route safety matters more than raw answer accuracy.

Repo: https://github.com/patibandlavenkatamanideep/relayops
Live demo: https://relayops-production.up.railway.app
HF adapter: https://huggingface.co/venkatamanideep/relayops-intent-qwen

---

### CostGuard

**LLM reliability and cost proxy for production AI systems.**

CostGuard sits between an application and LLM providers to track cost, validate responses, retry failures, and protect systems with circuit breakers.

**Highlights**

* provider-level circuit breakers
* retry and fallback logic
* cost tracking
* response validation
* Prometheus metrics
* Grafana dashboard
* alerting hooks
* 70+ unit tests

**Key lesson**

Production AI needs reliability controls around the model, not just better prompts.

Repo: https://github.com/patibandlavenkatamanideep/CostGuard

---

## About Me

I’m a Computer Science graduate student with a strong foundation in **data science, machine learning, and AI systems**.

My background started with statistical ML and data analysis, but over time I became more interested in a harder question:

> How do we make AI systems reliable when they are connected to tools, data, users, and real-world decisions?

That question led me toward LLM evals, agent safety, RAG reliability, model routing, and production AI infrastructure.

I enjoy building projects that combine:

* applied ML
* backend systems
* evaluation frameworks
* LLM/agent workflows
* deployment and observability
* honest documentation of limitations

---

## Tech Stack

**Languages & ML**
Python · SQL · scikit-learn · PyTorch · NumPy · Pandas · SciPy

**LLMs & Agents**
OpenAI · Claude · Gemini · Qwen · Llama · LangChain · LangGraph · RAG · LoRA · Unsloth

**Backend & Infrastructure**
FastAPI · Streamlit · Docker · Railway · GitHub Actions · REST APIs

**Data & Evaluation**
LLM evaluation · statistical validity · adversarial evals · route-safety metrics · cost tracking · observability

---

## Connect

GitHub: https://github.com/patibandlavenkatamanideep
LinkedIn: https://www.linkedin.com/in/patibandlavenkatamanideep
Email: [pvmanideep.analytics@gmail.com](mailto:pvmanideep.analytics@gmail.com)
