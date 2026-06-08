# Venkata Manideep Patibandla

**AI/ML Engineer · LLM Evaluation · Agentic AI Systems · Production AI Infrastructure**

I build AI systems where correctness is not the only metric.

My work focuses on:

* evaluating whether LLM agents reason correctly, not just whether they produce the right-looking answer
* building safer agent systems with scoped tools, routing, guardrails, and human escalation
* designing production AI infrastructure for reliability, cost control, and observability

Data science is my foundation. Statistical rigor is the differentiator.

---

## Featured Projects

### RealDataAgentBench

**LLM agent benchmark for statistically sound data science.**

RealDataAgentBench evaluates whether LLM agents perform valid data science workflows, not just produce plausible outputs.

* 39 tasks across 5 categories
* 12 frontier/open models
* 1,180+ benchmark runs
* cost tracking across models
* scoring for correctness, code quality, efficiency, and statistical validity

**Key lesson:** correct output does not always mean sound reasoning.

Repo: https://github.com/patibandlavenkatamanideep/RealDataAgentBench

---

### RelayOps

**Production-shaped AI customer-support agent for telecom/subscription support.**

RelayOps is an end-to-end vertical slice of a safer support agent:

* deterministic access gate before model/tool execution
* scoped account/device tools
* tiered intent router
* fine-tuned Qwen2.5-1.5B LoRA classifier
* hybrid RAG with citations
* guardrails for pricing, offers, and PII
* human escalation for billing, unsafe, or low-confidence turns
* adversarial route-safety evals

**Key lesson:** for agents that can take actions, route safety matters more than raw answer accuracy.

Repo: https://github.com/patibandlavenkatamanideep/relayops
Live demo: https://relayops-production.up.railway.app
HF adapter: https://huggingface.co/venkatamanideep/relayops-intent-qwen

---

### CostGuard

**LLM reliability and cost proxy for production AI systems.**

CostGuard sits between an application and LLM providers to track cost, validate responses, retry failures, and protect systems with circuit breakers.

* provider-level circuit breakers
* retry and fallback logic
* cost tracking
* response validation
* Prometheus metrics
* Grafana dashboard
* alerting hooks
* 70+ unit tests

**Key lesson:** production AI needs reliability controls around the model, not just better prompts.

Repo: https://github.com/patibandlavenkatamanideep/CostGuard

---

## Technical Focus

**LLM Evaluation**
Agent benchmarks · statistical validity · adversarial evals · route-safety metrics · LLM-as-judge · cost-aware evaluation

**Agentic AI Systems**
Tool-use agents · RAG · intent routing · scoped tools · deterministic policy gates · guardrails · human escalation

**Production AI Infrastructure**
FastAPI · Streamlit · Docker · Railway · CI/CD · observability · retries · circuit breakers · model/provider abstraction

**Machine Learning**
Python · SQL · scikit-learn · PyTorch · LoRA fine-tuning · Unsloth · Qwen · Llama · OpenAI · Claude · Gemini

---

## What I’m Building Toward

I’m interested in AI systems that are useful beyond demos:

* agents that know when not to act
* evals that measure reasoning quality, not just final answers
* routing systems that optimize for safety, reliability, and cost
* RAG systems with citations and groundedness checks
* infrastructure that makes model behavior observable and controllable

---

## Contact

GitHub: https://github.com/patibandlavenkatamanideep
LinkedIn: https://www.linkedin.com/in/patibandlavenkatamanideep
Email: [pvmanideep.analytics@gmail.com](mailto:pvmanideep.analytics@gmail.com)
