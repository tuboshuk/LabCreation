# 团队学习：心脏与大脑（claw0 与 deer-flow）

目的：让我们的“副业团队”具备可复制的 Agent 思维、工程化的执行框架、以及可积累的知识与工作流资产。

## 1. 学习材料

### 1.1 心脏：claw0（OpenClaw 0→1 学习仓库）

- 仓库：`https://github.com/shareAI-lab/claw0`
- 核心定位：从一个 `while True` 的 agent loop 开始，逐步搭建到“可生产的 agent gateway”。
- 结构特点：10 个渐进章节，每个章节是一个可运行的 Python 文件；代码与文档同仓。
- 章节脉络（建议只抓主线概念，不要求逐行背代码）：
  - s01 Agent Loop：`while + stop_reason`
  - s02 Tool Use：工具调度表（dispatch table）
  - s03 Sessions & Context：会话持久化与上下文溢出处理
  - s04 Channels：Telegram/飞书等渠道统一成 InboundMessage
  - s05 Gateway & Routing：路由与隔离
  - s06 Intelligence：soul/memory/skills/prompt 组装
  - s07 Heartbeat & Cron：主动 agent + 定时任务
  - s08 Delivery：可靠投递队列与退避
  - s09 Resilience：重试策略、鉴权轮换、溢出压缩
  - s10 Concurrency：命名车道（lanes）控制并发

### 1.2 大脑：deer-flow（Super Agent Harness）

- 仓库：`https://github.com/bytedance/deer-flow`
- 核心定位：一个可扩展的“超级 Agent 运行时/编排框架”，用于研究、编码、创建多步骤产物（skills、tools、subagents、memory、sandbox）。
- 关键点（我们要学的不是 UI，而是“框架能力抽象”）：
  - Skills：把工作流固化为可复用的能力模块（类似我们的 roles + SOP）。
  - Sub-Agents：复杂任务拆解与并行协作。
  - Sandbox：隔离执行环境（本地/Docker/K8s）与文件系统。
  - Memory：长期记忆与上下文工程。
  - 可观测与可运行：通过统一入口让 agent 真正“把事做完”。

## 2. 我们要产出的“可复用资产”

团队学习不以“看完”为目标，而以“沉淀可复用资产”为目标：

- 一份短笔记（1 页以内）：核心概念 + 我们项目可借鉴点 + 不适用点。
- 一个最小可运行 demo：能跑起来并截图/录屏（可作为后续演示素材）。
- 一个“迁移清单”：列出 3 条可落地到我们作品集生成器或后续产品的改进点。

## 3. 分工（每个角色看什么、交付什么）

### PM

- claw0：关注“章节如何渐进引入新概念”这种教学式产品化表达。
- deer-flow：关注“技能/子代理/记忆”的产品化表达方式与成功指标。
- 交付：`1 页对比表`（claw0 vs deer-flow：解决问题、适用场景、我们怎么用）。

### Chief TL

- claw0：重点看 s03/s05/s08/s09/s10（会话、路由、投递、韧性、并发）。
- deer-flow：重点看 sandbox/memory/skills 的边界与约束。
- 交付：一份“我们团队自己的 agent harness 最小架构草图”（Mermaid 一张图即可）。

### Frontend TL / Frontend Dev

- deer-flow：重点看“技能可视化/运行入口/产物落盘”这类交互与体验。
- 交付：列 3 条我们作品集生成器可提升的“演示/交付体验”（例如一键发布、示例模板、配置校验）。

### Backend TL / Backend Dev

- claw0：看工具调度、会话、重试、投递队列、并发控制。
- deer-flow：看模型配置与工具/技能扩展的工程化方式。
- 交付：写一份“我们自己的最小工具调度骨架”伪代码或接口草案（不必落地实现）。

### QA

- deer-flow：看它如何保证“任务完成”、如何记录可回放的过程与产物。
- 交付：给我们作品集生成器补一份“交付验收清单”建议（5-10 条即可）。

## 4. 周日之前的最低任务定义（与学习计划对齐）

- OpenClaw：本地跑通 `s01_agent_loop.py`（或等价最小章节），并写 1 页笔记。
- DeerFlow：按官方 Quick Start 跑到能打开本地页面（或完成 `make config` + 能启动的程度），并写 1 页笔记。

## 5. 评审方式（15 分钟）

- 每人 2 分钟：说“我学到的 1 个概念 + 我建议落地的 1 件事”。
- 最终输出：选出 3 个“下一迭代可落地”的改进点，进入 backlog。

