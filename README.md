<h1 align="center">Venkata Manideep Patibandla</h1>

<p align="center">
  <strong>LLM Evaluation · Agent Systems · Production ML Engineering</strong>
</p>

<p align="center">
  MS Computer Science @ University at Buffalo
  &nbsp;·&nbsp;
  <a href="https://venkatamanideep.com">venkatamanideep.com</a>
  &nbsp;·&nbsp;
  <a href="https://linkedin.com/in/manideep-analytics">LinkedIn</a>
</p>

---

## What I build

I work at the intersection of **LLM evaluation**, **agent systems**, and **statistically rigorous AI** — the part of ML where getting the right answer isn't enough. The reasoning has to hold up too.

Most benchmarks ask: *did the model output the correct number?*  
I care about: *did it reason correctly, use appropriate methods, and report uncertainty?*  
Those are different questions. They have different answers.

---

## Featured project

### [RealDataAgentBench](https://github.com/patibandlavenkatamanideep/RealDataAgentBench) &nbsp;·&nbsp; [Live Leaderboard ↗](https://patibandlavenkatamanideep.github.io/RealDataAgentBench/)

An open-source benchmark for evaluating whether LLM agents can perform real-world data science workflows with statistical rigor.

| | |
|---|---|
| **Tasks** | 23 across EDA, feature engineering, modeling, inference, ML engineering |
| **Models benchmarked** | 10 — GPT-5, GPT-4.1, Claude Opus/Sonnet/Haiku, Gemini 2.5, Grok, Llama, and more |
| **Runs** | 163 with full cost tracking |
| **Scoring** | 4 dimensions: correctness · code quality · efficiency · statistical validity |

**Key finding:** Every frontier model — including GPT-5 — scores ≤0.25 on statistical validity on tasks where it scores 0.83–1.00 on correctness. Correct output ≠ sound reasoning.

```bash
# Try it in 60 seconds
git clone https://github.com/patibandlavenkatamanideep/RealDataAgentBench
cd RealDataAgentBench && pip install -e ".[dev]"
dab run eda_001 --model gpt-4.1 --budget 0.02
dab score outputs/eda_001_*.json
```

---

## Stack

**Languages** &nbsp; Python · TypeScript · SQL  
**LLM / AI** &nbsp; Anthropic API · OpenAI API · Groq · LangChain · RAG pipelines  
**ML** &nbsp; scikit-learn · XGBoost · LightGBM · PyTorch  
**Infra** &nbsp; GitHub Actions · Docker · Streamlit · FastAPI  
**Evaluation** &nbsp; Custom scoring engines · Statistical validity testing · Benchmark design

---

## What I'm focused on

- Building evaluation infrastructure that surfaces *how* models reason, not just *what* they output
- Extending RDAB: 30+ tasks, human baselines, arXiv writeup
- Roles in LLM evaluation, agent systems, and production AI infrastructure

---

<p align="center">
  <a href="https://github.com/patibandlavenkatamanideep/RealDataAgentBench">
    <img src="https://img.shields.io/badge/RealDataAgentBench-open--source-3B82F6?style=flat-square&logo=github" />
  </a>
  &nbsp;
  <a href="https://patibandlavenkatamanideep.github.io/RealDataAgentBench/">
    <img src="https://img.shields.io/badge/leaderboard-live-22C55E?style=flat-square" />
  </a>
  &nbsp;
  <a href="https://linkedin.com/in/manideep-analytics">
    <img src="https://img.shields.io/badge/LinkedIn-connect-0A66C2?style=flat-square&logo=linkedin" />
  </a>
</p>
