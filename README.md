<!-- Header banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,50:3B82F6,100:06B6D4&height=200&section=header&text=Venkata%20Manideep%20Patibandla&fontSize=36&fontColor=FFFFFF&fontAlignY=38&desc=LLM%20Evaluation%20%C2%B7%20Agent%20Systems%20%C2%B7%20Production%20ML%20Engineering&descSize=16&descAlignY=58&animation=fadeIn" width="100%" />

<!-- Social badges -->
<p align="center">
  <img src="https://img.shields.io/badge/Sacred%20Heart%20University-MS%20Computer%20Science-CC0000?style=for-the-badge&logo=academia&logoColor=white" />
</p>

<p align="center">
  <a href="https://venkatamanideep.com" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-venkatamanideep.com-0F172A?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
  &nbsp;
  <a href="mailto:venkatamanideep20@gmail.com">
    <img src="https://img.shields.io/badge/Email-venkatamanideep20@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://linkedin.com/in/manideep-analytics" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  &nbsp;
  <a href="https://patibandlavenkatamanideep.github.io/RealDataAgentBench/" target="_blank">
    <img src="https://img.shields.io/badge/Live%20Leaderboard-RDAB-22C55E?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0F172A&height=3&section=header" width="100%" />

<h2 align="center">⚡ What I Build</h2>

<p align="center">
  <em>Most benchmarks ask: "did the model get the right answer?"</em><br/>
  <em>I care about: "did it reason correctly, use appropriate methods, and report uncertainty?"</em><br/>
  <strong>Those are different questions. They have different answers.</strong>
</p>

<p align="center">
  I work at the intersection of <strong>LLM evaluation</strong>, <strong>agent systems</strong>, and <strong>production AI infrastructure</strong><br/>
  Data Science is my foundation — statistical rigor is the differentiator.
</p>

<br/>

---

## 🚀 Featured Project — RealDataAgentBench

<table>
<tr>
<td width="58%">

### [RealDataAgentBench (RDAB)](https://github.com/patibandlavenkatamanideep/RealDataAgentBench)

An open-source benchmark that evaluates whether LLM agents perform **statistically sound** data science — not just correct-looking output.

| | |
|---|---|
| 🧪 Tasks | **39** across 5 categories |
| 🤖 Models | **12** frontier models — GPT-4.1, Claude Sonnet 4.6, Gemini 2.5 Flash, Llama 3.3, Grok-3 mini |
| 📊 Runs | **1,180+** with full cost tracking |
| 📐 Scoring | Correctness · Code Quality · Efficiency · Stat Validity |

**Key finding:** Every frontier model scores ≤**0.25** on statistical validity on tasks where it scores **0.83–1.00** on correctness.

> Correct output ≠ sound reasoning.

</td>
<td width="42%" align="center">

<a href="https://patibandlavenkatamanideep.github.io/RealDataAgentBench/" target="_blank">
  <img src="https://img.shields.io/badge/%F0%9F%9F%A2%20LIVE%20LEADERBOARD-Open%20Now-22C55E?style=for-the-badge" />
</a>

<br/><br/>

<a href="https://github.com/patibandlavenkatamanideep/RealDataAgentBench" target="_blank">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=patibandlavenkatamanideep&repo=RealDataAgentBench&theme=tokyonight&hide_border=true&bg_color=0F172A&title_color=3B82F6&text_color=94A3B8&icon_color=06B6D4" />
</a>

</td>
</tr>
</table>

```bash
# Run in 60 seconds
git clone https://github.com/patibandlavenkatamanideep/RealDataAgentBench
pip install -e ".[dev]"
dab run eda_001 --model gpt-4.1 --budget 0.02
dab score outputs/eda_001_*.json
# → score breakdown · token usage · statistical validity gaps
```

---

## 🛡️ Production Project — CostGuard

<table>
<tr>
<td width="58%">

### [CostGuard](https://github.com/patibandlavenkatamanideep/CostGuard)

A **production-grade LLM reliability proxy** that sits between your agent and any provider. Every call is validity-scored, cost-tracked, circuit-broken, and retried — without touching your application code.

| | |
|---|---|
| 🔁 Retry | Exponential backoff for 429/503 (tenacity, 3 attempts, 1–8s) |
| ⚡ Circuit breakers | CLOSED/OPEN/HALF\_OPEN per provider, state persists across restarts |
| 📊 Observability | Prometheus metrics + Grafana dashboard, 13 metrics |
| 🔔 Alerts | 6 types — Slack + webhook, cooldown-managed |
| 🧪 Tests | 73 unit tests (CB, retry, persistence, scoring, middleware) |
| 🌐 Deploy | One-click Render · Fly.io · Koyeb · Docker Compose |

Validity scoring is RDAB-calibrated. Full RDAB evaluation via `POST /evaluate`.

</td>
<td width="42%" align="center">

<a href="https://github.com/patibandlavenkatamanideep/CostGuard" target="_blank">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=patibandlavenkatamanideep&repo=CostGuard&theme=tokyonight&hide_border=true&bg_color=0F172A&title_color=3B82F6&text_color=94A3B8&icon_color=06B6D4" />
</a>

</td>
</tr>
</table>

```python
# Drop-in proxy — works with LangGraph, CrewAI, or any agent
import httpx
resp = httpx.post("https://your-costguard.onrender.com/proxy", json={
    "model_id":         "gpt-4.1",
    "prompt":           "Analyze this dataset...",
    "fallback_models":  ["claude-sonnet-4-6", "gemini-2.5-flash"],
    "reject_threshold": 0.30,
})
print(resp.json()["content"])               # validated LLM response
print(resp.json()["cost_usd"])              # exact cost to 8 decimal places
print(resp.json()["circuit_breaker_state"]) # closed / open / half_open
```

---

## 🛠️ Tech Stack

<h4>Languages</h4>
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white" />
</p>

<h4>LLM / AI / GenAI</h4>
<p>
  <img src="https://img.shields.io/badge/Anthropic_Claude-0F172A?style=for-the-badge&logo=anthropic&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenAI_API-412991?style=for-the-badge&logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" />
  <img src="https://img.shields.io/badge/RAG_Pipelines-06B6D4?style=for-the-badge&logo=databricks&logoColor=white" />
  <img src="https://img.shields.io/badge/Groq-F55036?style=for-the-badge&logoColor=white" />
</p>

<h4>ML / Data Science</h4>
<p>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" />
  <img src="https://img.shields.io/badge/XGBoost-189AD3?style=for-the-badge&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
</p>

<h4>Infrastructure & Observability</h4>
<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
</p>

---

## 🎯 Currently Building

```
▸ RealDataAgentBench  →  39 tasks · 12 models · 1,180+ runs · arXiv paper in progress
▸ CostGuard           →  production LLM proxy · 73 unit tests · deployed on Render/Fly.io
▸ Open to roles in    →  LLM evaluation · agent reliability · production AI infrastructure
```

---

<p align="center">
  <a href="https://venkatamanideep.com" target="_blank">
    <img src="https://img.shields.io/badge/View%20Full%20Portfolio%20%E2%86%97-venkatamanideep.com-3B82F6?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
</p>

<!-- Footer banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:3B82F6,100:0F172A&height=120&section=footer&animation=fadeIn" width="100%" />
