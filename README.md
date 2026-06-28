# Hi there, I'm Xu Zheng (许政) 👋

**Data Science & Big Data Technology** @ University of Jinan (2024–2028)
**数据科学与大数据技术** · 济南大学 (2024–2028)

I build things at the intersection of **recommendation systems**, **user growth**, and **AI agents**. My work spans from research to production — training LLM-based recommenders, shipping open-source PRs to projects with 190K+ stars, and competing in mathematical modeling contests.
我的兴趣方向是**推荐系统**、**用户增长**与 **AI Agent**，工作覆盖从科研到工程——训练 LLM 推荐模型、向 19 万 Star 级项目提交 PR、参加数学建模竞赛。

---

## 🛠 Tech Stack / 技术栈

`Python` `C/C++` `TypeScript` `PyTorch` `Transformers` `Scikit-learn` `XGBoost` `LangChain` `FAISS` `FastAPI` `Electron` `React` `Docker` `Git`

---

## 🔬 Research / 科研经历

**LLM-Enhanced Recommendation with P5 + Reinforcement Learning + Memory** `2025.5–至今`
**LLM 增强推荐系统研究（P5 + 强化学习 + 记忆架构）**

> Reproduced P5 (Pretrain-Prompt-Predict) on T5 backbone for sequential recommendation (Amazon Beauty, 22K users). Designed a POMDP-based RL policy network + FAISS long/short-term memory system to replace Beam Search, solving policy collapse. Proposed lightweight co-occurrence matrix embedding (128-dim in ~1s on CPU, no GPU needed). HR@10 reached 2.4%, ~14× over random baseline; ablation confirmed RL policies adapt to memory configs.
>
> 基于 T5 骨干网络复现 P5 推荐框架，在 Amazon Beauty 数据集上进行序列推荐实验。针对 Beam Search 效率低且易产生策略崩塌的问题，设计 POMDP 强化学习策略网络结合 FAISS 长短期记忆系统的混合架构。提出基于共现矩阵的轻量级 Item Embedding 方案，仅需 CPU 约 1 秒即可构建 128 维稠密向量，无需 GPU 训练。HR@10 达 2.4%，约为随机基线的 14 倍，消融实验表明 POMDP 框架能根据记忆配置学习差异化的行为策略。

- [Repo / 仓库](https://github.com/returnSGD/LLMRec_recommendation)

---

## 🧩 Selected Projects / 项目经历

### OneTrans & MixFormer: Unified Recommendation via Transformer `2026.3–5`
### 针对大规模数据推荐的序列建模与特征交互统一化推荐系统

> *Tencent Advertising Algorithm Competition × KDD Cup*
> End-to-end single-stage recommendation unifying sequence modeling & feature interaction. Designed unified tokenization for heterogeneous features, hybrid parameterization (shared for sequence tokens, independent for non-sequence), and a pyramid stacking structure with KV-cache reuse reducing self-attention from O(L²) to O(L). Validated on million-scale interaction data.
>
> *腾讯广告算法大赛 × KDD Cup 赛题*
> 基于统一 Transformer 架构将序列建模与特征交互整合为端到端单阶段处理。设计统一分词策略将异构特征映射至同一语义空间；引入混合参数化方案；提出金字塔堆叠结构，逐层剪枝配合 KV 缓存复用，将自注意力计算复杂度从 O(L²) 降至 O(L)。在百万级交互数据上验证了架构有效性。

---

### Game Player Churn Prediction & Persona Platform `2025.3–4`
### 游戏玩家流失预测与用户画像分析平台

> *National E-commerce "Three-Creation" Competition*
> 26 behavioral features → XGBoost churn prediction (AUC 0.999) + KMeans persona clustering + BERT sentiment analysis on 46K reviews. Built a "persona ↔ sentiment" linkage for closed-loop churn intervention.
>
> *第十六届全国大学生电子商务"三创赛"*
> 从 6 大维度 26 项行为指标出发构建流失预警体系：XGBoost 预测玩家流失程度，AUC 达 0.999；KMeans 聚类完成用户分群画像；基于 4.6 万余条玩家评论，利用 BERT 进行情感分析与主题挖掘。构建了"用户画像—舆情关联分析"机制，形成从预警到干预的完整运营闭环。

- [Repo / 仓库](https://github.com/returnSGD/User_growth_monitoring)

---

### Claude MD Editor — AI-Powered Desktop Markdown Editor `2026.5`
### Claude MD Editor：AI 驱动的桌面 Markdown 编辑器

> Electron + React + TypeScript desktop app integrating CodeMirror 6, KaTeX, Mermaid, and an embedded Claude Code AI terminal (xterm.js + node-pty). One-click export to HTML/PDF/DOCX/image. Supports Windows/macOS/Linux. 3 ⭐ on GitHub.
>
> 独立完成的桌面端 Markdown 编辑器，采用 Electron + React + TypeScript 架构，集成 CodeMirror 6 编辑器内核、KaTeX 数学公式渲染及 Mermaid 图表支持。核心特色是内嵌了 Claude Code AI 对话终端，用户无需切换工具即可与 AI 交互。支持一键导出 HTML/PDF/DOCX/图片，三平台打包发布。获得 3 Star 与 1 Fork。

- [Repo / 仓库](https://github.com/returnSGD/claude-md)

---

### arXiv MCP Server with DeepSeek Translation `2026.4`
### 接入 DeepSeek 的 arXiv 个性化检索 MCP 服务

> MCP-protocol academic search: Chinese query → DeepSeek translation → arXiv retrieval → FlagReranker semantic re-ranking → Chinese abstract generation. FastAPI + fastapi-mcp SSE endpoint, plug-and-play for Claude Desktop. Solves the language barrier for non-native English-speaking researchers.
>
> 基于 MCP 协议的全流程自动化学术检索服务：中文查询 → DeepSeek 翻译为英文并提取核心关键词 → arXiv API 检索 → FlagReranker 语义重排序 → 英文摘要翻译为中文返回。采用 FastAPI + fastapi-mcp 挂载为 SSE 端点，可作为 Claude Desktop 的即插即用工具。

- [Repo / 仓库](https://github.com/returnSGD/arxiv_MCP)

---

### AI Customer Service with LoRA + RAG + LLM `2025.3–4`
### 集成 LoRA 微调、RAG 检索与大模型的智能对话 AI 客服系统

> Three-layer architecture: RAG (Sentence-Transformers + FAISS) → DeepSeek candidate generation → LoRA-tuned Chinese-MacBERT-Base (rank=8, 1M conversations) for reply ranking. Effectively combines external knowledge injection with model fine-tuning for e-commerce phone consulting.
>
> "RAG 知识检索 → DeepSeek 生成候选回复 → LoRA 打分排序"三层智能客服架构。RAG 层使用 Sentence-Transformers + FAISS 确保回答准确性；推理层基于 DeepSeek 结合检索结果与对话历史生成候选回复；排序层以 Chinese-MacBERT-Base 为基座注入 LoRA 适配器（rank=8），在 100 万条电商对话数据上训练，自动筛选最优回复。

- [Repo / 仓库](https://github.com/returnSGD/AI_customer_service)

---

### Cat Language System for "Whispers of the Heart" 🐱 `2026.4–至今`
### 腾讯游戏创作大赛作品《猫语心声》猫咪 AI 决策控制与语言系统

> *Tencent Game Creation Competition*
> Three-tier cat AI architecture: RL strategy layer (Transformer + FiLM, 422-dim state → 15 intents, BC + PPO), custom lightweight behavior tree engine (Selector/Sequence/Parallel/Decorator), and local DeepSeek-R1-Distill-Qwen-1.5B (Q4_0 quantized, ~1GB) for emotional monologues. Personality filter + dual memory (working 20 + long-term 500 + vector semantic retrieval) for consistent character evolution.
>
> *腾讯游戏创作大赛*
> 猫咪决策控制与语言生成模块，设计为 RL 策略层 → BT 行为树层 → LLM 文本层三层架构。策略层基于 Transformer Encoder + FiLM 性格调制，接收 422 维状态空间，输出 15 种宏观意图决策；行为树层自研轻量行为树引擎；文本层本地部署 DeepSeek-R1-Distill-Qwen-1.5B（Q4_0 量化，仅约 1GB）生成情感化猫咪内心独白。通过性格过滤器与双层级记忆系统确保全链路性格一致性。

- [Repo / 仓库](https://github.com/returnSGD/TGA2026/tree/main/cat_control)

---

### GameGPT: Ensemble Learning for Player Decision Prediction `2026.5`
### 基于集成学习和长时序上下文的 GameGPT 玩家决策预测系统

> 55-dim features engineered from 289K game log samples (274GB) of Delta Force. XGBoost + Random Forest + GBDT with soft voting ensemble for player intent & action prediction. Validated ensemble stability improvement on 280K+ samples.
>
> 针对《三角洲行动》游戏内 289,201 个样本（274GB）的 20 秒历史日志数据，提取 55 维结构化特征。采用 XGBoost、随机森林、GBDT 三种集成学习算法，通过软投票集成策略融合多模型预测结果，在 28 万+ 样本上验证了集成策略对预测稳定性的提升效果。

- [Repo / 仓库](https://github.com/returnSGD/TGA2026)

---

## 🤝 Open Source Contributions / 社区贡献

| Project / 项目 | Stars | Contribution / 贡献 |
|---|---|---|
| [LightRAG](https://github.com/HKUDS/LightRAG/pull/3269) | 36.6K | Refactored NDJSON streaming parser (DRY refactoring), fixed a bug redirecting stream errors to login page. Added 973 lines of tests, removed 290 redundant lines. **Merged.** / 重构 NDJSON 流式解析模块，修复流错误被误归类为认证失败的 Bug。新增 973 行测试，删除冗余代码 290 行。**已合并。** |
| [TensorTrade](https://github.com/tensortrade-org/tensortrade/pull/499) | 6.3K | Added short-selling support to OMS & Action Schemes. Minimal-invasive design, fully backward-compatible. 23 new tests, 120 existing tests zero regression. **Submitted.** / 为 OMS 和 Action Schemes 添加做空支持，最小侵入式设计，完全向后兼容。新增 23 个专项测试，原有 120 个单测零回归。**已提交。** |
| [n8n](https://github.com/n8n-io/n8n/pull/32629) | 193K | Fixed v2.24.0 regression crash in Form Trigger node (missing default value). **Merged.** / 修复 v2.24.0 回归导致旧版 Form Trigger 节点因缺少默认值而崩溃的问题。**已合并。** |
| [AI_HR_Project](https://github.com/Begapunk/AI_HR_project/pull/3) | — | Batch resume screening: hard-filter → LLM scoring → ranking. Anthropic Messages API integration. **Merged.** / 设计并实现批量简历筛选模块，构建"硬性条件筛选 → LLM 多维评分 → 智能排序"三阶段候选人推荐流程。**已合并。** |
| [WeMD](https://github.com/tenngoxars/WeMD/pull/82) | — | Removed hardcoded font-size in table renderer for proper theme support. **Merged.** / 移除表格渲染器硬编码 font-size，改为由主题 CSS 控制。**已合并。** |

---

## 🏆 Competitions / 竞赛经历

| Competition / 竞赛 | Description / 简介 |
|---|---|
| **MCM/ICM 2026** | Bayesian hierarchical model (MCMC) for latent variable estimation, AUC 0.838. / 构建 Gamma 分布先验的贝叶斯层次模型，采用 MCMC 进行后验推断，AUC 达 0.838。 |
| **CUMCM 2025** | IRODDPSO + constrained KMeans clustering + Monte Carlo error analysis. / 改进 IRODDPSO 粒子群优化算法，实现医学约束 K-means 聚类，完成蒙特卡洛模拟误差分析。 |
| **Lanqiao Cup 2025** | C/C++ track, Provincial Second Prize. / 蓝桥杯全国软件和信息技术专业人才大赛 C/C++ 赛道，省级二等奖。 |
| **NCCCC 2025** | Deep learning for flower recognition (Transformer + CNN). / 第七届全国高校计算机能力挑战赛-大数据挑战赛，使用 Transformer 及 CNN 进行花卉识别。 |

---

<p align="center">
  <i>Always open to collaboration on recsys, LLM agents, and open-source. / 欢迎交流推荐系统、LLM Agent 与开源合作。📧 2208499028@qq.com</i>
</p>
