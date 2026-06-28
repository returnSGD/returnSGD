# Hi there, I'm Xu Zheng (许政) 👋

**Data Science & Big Data Technology** @ University of Jinan (2024–2028)

I build things at the intersection of **recommendation systems**, **user growth**, and **AI agents**. My work spans from research to production — training LLM-based recommenders, shipping open-source PRs to projects with 190K+ stars, and competing in mathematical modeling contests.

---

## 🔬 Research

**LLM-Enhanced Recommendation with P5 + Reinforcement Learning + Memory** `2025.5–present`
- Reproduced P5 (Pretrain-Prompt-Predict) on T5 backbone for sequential recommendation (Amazon Beauty, 22K users)
- Designed a POMDP-based RL policy network + FAISS long/short-term memory system to replace Beam Search
- Proposed lightweight co-occurrence matrix embedding (128-dim in ~1s on CPU, no GPU needed)
- HR@10 reached 2.4%, ~14× over random baseline; ablation confirmed RL policies adapt to memory configs
- [Repo](https://github.com/returnSGD/LLMRec_recommendation)

---

## 🧩 Selected Projects

### OneTrans & MixFormer: Unified Recommendation via Transformer `2026.3–5`
*Tencent Advertising Algorithm Competition × KDD Cup*
End-to-end single-stage recommendation unifying sequence modeling & feature interaction. Designed unified tokenization for heterogeneous features, hybrid parameterization (shared for sequence tokens, independent for non-sequence), and a pyramid stacking structure with KV-cache reuse reducing self-attention from O(L²) to O(L).

### Game Player Churn Prediction & Persona Platform `2025.3–4`
*National E-commerce "Three-Creation" Competition*
26 behavioral features → XGBoost churn prediction (AUC 0.999) + KMeans persona clustering + BERT sentiment analysis on 46K reviews. Built a "persona ↔ sentiment" linkage for closed-loop churn intervention.
- [Repo](https://github.com/returnSGD/User_growth_monitoring)

### Claude MD Editor — AI-Powered Desktop Markdown Editor `2026.5`
Electron + React + TypeScript desktop app integrating CodeMirror 6, KaTeX, Mermaid, and an embedded Claude Code AI terminal (xterm.js + node-pty). One-click export to HTML/PDF/DOCX/image. 3 ⭐ on GitHub.
- [Repo](https://github.com/returnSGD/claude-md)

### arXiv MCP Server with DeepSeek Translation `2026.4`
MCP-protocol academic search: Chinese query → DeepSeek translation → arXiv retrieval → FlagReranker semantic re-ranking → Chinese abstract generation. FastAPI + fastapi-mcp SSE endpoint, plug-and-play for Claude Desktop.
- [Repo](https://github.com/returnSGD/arxiv_MCP)

### AI Customer Service with LoRA + RAG + LLM `2025.3–4`
Three-layer architecture: RAG (Sentence-Transformers + FAISS) → DeepSeek candidate generation → LoRA-tuned Chinese-MacBERT-Base (rank=8, 1M conversations) for reply ranking. Designed for e-commerce phone consulting.
- [Repo](https://github.com/returnSGD/AI_customer_service)

### Cat Language System for "Whispers of the Heart" 🐱 `2026.4–present`
*Tencent Game Creation Competition*
Three-tier cat AI: RL strategy layer (Transformer + FiLM, 422-dim state → 15 intents, BC + PPO), custom behavior tree engine, and local DeepSeek-R1-Distill-Qwen-1.5B (Q4_0, ~1GB) for emotional monologues. Personality filter + dual memory (working 20 + long-term 500 + vector retrieval) for consistent character evolution.
- [Repo](https://github.com/returnSGD/TGA2026/tree/main/cat_control)

### GameGPT: Ensemble Learning for Player Decision Prediction `2026.5`
55-dim features from 289K game log samples (274GB). XGBoost + Random Forest + GBDT with soft voting ensemble for player intent & action prediction in Delta Force.
- [Repo](https://github.com/returnSGD/TGA2026)

---

## 🤝 Open Source Contributions

| Project | Stars | Contribution |
|---|---|---|
| [LightRAG](https://github.com/HKUDS/LightRAG/pull/3269) | 36.6K | Refactored NDJSON streaming parser (DRY), fixed a bug redirecting stream errors to login page. Added 973 lines of tests, removed 290 redundant lines. **Merged.** |
| [TensorTrade](https://github.com/tensortrade-org/tensortrade/pull/499) | 6.3K | Added short-selling support to OMS & Action Schemes. Minimal-invasive design, fully backward-compatible. 23 new tests, 120 existing tests zero regression. **Submitted.** |
| [n8n](https://github.com/n8n-io/n8n/pull/32629) | 193K | Fixed v2.24.0 regression crash in Form Trigger node (missing default value). **Merged.** |
| [AI_HR_Project](https://github.com/Begapunk/AI_HR_project/pull/3) | — | Batch resume screening module: hard-filter → LLM scoring → ranking. Anthropic Messages API integration. **Merged.** |
| [WeMD](https://github.com/tenngoxars/WeMD/pull/82) | — | Removed hardcoded font-size in table renderer for proper theme support. **Merged.** |

---

## 🏆 Competitions

- **MCM/ICM 2026** — Bayesian hierarchical model (MCMC) for latent variable estimation, AUC 0.838
- **CUMCM 2025** — IRODDPSO + constrained KMeans clustering + Monte Carlo error analysis
- **Lanqiao Cup 2025** — C/C++ track, Provincial Second Prize
- **National College Computer Competence Challenge 2025** — Deep learning for flower recognition (Transformer + CNN)

---

## 🛠 Tech Stack

`Python` `C/C++` `TypeScript` `PyTorch` `Transformers` `Scikit-learn` `XGBoost` `LangChain` `FAISS` `FastAPI` `Electron` `React` `Docker` `Git`

---

<p align="center">
  <i>Always open to collaboration on recsys, LLM agents, and open-source. Reach me at 2208499028@qq.com</i>
</p>
