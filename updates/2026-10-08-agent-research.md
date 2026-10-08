# 2026 Agent research update — 2026-10-08

## Scope and repository audit

Base: `azure-z77/ai-agent-papers`, commit `3df3d75124a134fb7017718fec3ead22e4a3dbc9` (`update:12/15`). Git author timestamp is 2025-12-15 00:00:18 +09:00, equivalent to 2025-12-14 15:00:18 UTC / 23:00:18 Asia/Shanghai; the stated December 14 date is consistent.

The existing structure contains capability papers, application papers, agent frameworks and lectures. This update preserves it. Original README highlights end in 2025 and the inspected baseline contains none of the new canonical works below. The stale “Updated biweekly” claim is replaced by an explicit review date.

This is a selective catch-up through 2026-10-08, not an exhaustive census or a live leaderboard. Fifteen distinct works/releases are included. Full entries live in one category each; this page and related categories link to them. arXiv versions are consolidated by base identifier, and official code/model releases are attached to their paper rather than counted again. AgentENV is separate because its systems contribution is distinct from the K3 model report. Pro V2 is explicitly a 2026 revision, not a newly invented benchmark lineage.

## Reading order and research implications

1. **Kimi K3 + AgentENV:** inspect the interaction between agentic training, persistent state and environment cost. Open weights and open infrastructure are separate releases; neither establishes that all training artifacts are public.
2. **Cross-Benchmark Transfer + VPR:** ask whether better verification changes credit assignment and produces held-out transfer. Separate outcome checks, regression protection and intermediate oracles.
3. **LiteResearcher + DeepResearch Bench II:** pair cheap search-agent training with report-level evaluation. Search QA accuracy alone does not establish research-report quality.
4. **MemRL + EvoMemBench:** compare adaptive memory against strong long-context baselines under matching task streams and budgets.
5. **DynamicGUIBench + K2.5 + MAS-FIRE:** examine observation loss, parallel latency and coordination failures separately; “more agents” is not itself an explanation for gains.
6. **SafeEvolve + MAS security SoK + Pro V2:** audit runtime boundaries, useful-task performance and verifier integrity along with attack success.

These are editorial implications from the cited work, not claims of causal proof across all agents.

## Canonical additions

| First release | Work | Directions | Entry |
| --- | --- | --- | --- |
| 2026-07-27 | Kimi K3: Open Frontier Intelligence | Kimi-K3, Agentic RL, Coding, Deep Research | [notes](../application-papers/agentic-ai-system.md#kimi-k3) |
| 2026-07-27 | AgentENV: distributed execution environments for agentic RL | Agentic RL, Efficiency, Engineering | [notes](../agent-frameworks/agent-framework.md#agentenv) |
| 2026-10-01 | Cross-Benchmark Transfer from RL on Agentic Coding Tasks | Agentic RL, Coding, Evaluation | [notes](../application-papers/software-agents.md#coding-transfer) |
| 2026-05-11 | Verifiable Process Rewards for Agentic Reasoning | Agentic RL, Agentic Reasoning | [notes](../capability-papers/learning.md#vpr) |
| 2026-01-18 | A Survey of Agentic Reasoning for Large Language Models: Towards Recursively Self-Improving and Collective Agents | Agentic Reasoning, Survey | [notes](../capability-papers/reasoning.md#reasoning-survey) |
| 2026-04-20 | LiteResearcher: A Scalable Agentic RL Training Framework for Deep Research Agent | Deep Research, Agentic RL, Efficiency | [notes](../application-papers/deep-research-agents.md#literesearcher) |
| 2026-01-13 | DeepResearch Bench II: Diagnosing Deep Research Agents via Rubrics from Expert Reports | Deep Research, Evaluation | [notes](../capability-papers/evaluation.md#deepresearch-bench-ii) |
| 2026-04-28 | Benchmarking and Improving GUI Agents in High-Dynamic Environments | GUI, Evaluation | [notes](../application-papers/digital-agents.md#dynamic-gui) |
| 2026-02-02 | Kimi K2.5: Visual Agentic Intelligence | Multi-Agent, Efficiency, Model Release | [notes](../application-papers/multi-agent.md#kimi-k25) |
| 2026-02-23 | MAS-FIRE: Fault Injection and Reliability Evaluation for LLM-Based Multi-Agent Systems | Multi-Agent, Evaluation, Safety | [notes](../application-papers/multi-agent.md#mas-fire) |
| 2026-01-06 | MemRL: Self-Evolving Agents via Runtime Reinforcement Learning on Episodic Memory | Memory, Self-Evolution | [notes](../capability-papers/memory.md#memrl) |
| 2026-05-18 | EvoMemBench: Benchmarking Agent Memory from a Self-Evolving Perspective | Memory, Self-Evolution, Evaluation | [notes](../capability-papers/evaluation.md#evomembench) |
| 2026-09-02 | SafeEvolve: Harness-Policy Co-Evolution from Agent Experience for Safety Alignment | Safety, Self-Evolution, Agentic RL | [notes](../capability-papers/safety.md#safeevolve) |
| 2026-09-01 | SoK: When Safe Agents Fail Together: The Security of Multi Agent LLM Systems | Safety, Multi-Agent, Survey | [notes](../capability-papers/safety.md#mas-security) |
| 2026-09-22 | SWE-Bench Pro V2: public split and locked evaluation protocol | Coding, Evaluation, Safety | [notes](../capability-papers/evaluation.md#swe-pro-v2) |

## Evidence and comparison rules

- Paper identity, dates, versions and the claims summarized here were checked on primary arXiv landing pages, official repositories or official release pages. This pass did not reproduce experiments or audit every full-text table. Where only the abstract supports a number, that limitation is stated in the entry.
- Preserve model/checkpoint, benchmark version/split, harness, tools/network access, context management, effort, attempts, judge/verifier and cost boundary with every score. A missing setting means the number is illustrative rather than leaderboard-comparable.
- K3's official README is an October 8 retrieval snapshot; many of its underlying evaluations are July snapshots. Retrieval date is not evaluation date. For K3's reported numbers, use the linked official repository as well as the pinned report.
- Keep success rate, latency, token consumption, dollars and environment-only cost separate. Record failures, refusals and fallbacks rather than silently dropping them.
- Code linked from an official paper is evidence of an official project, not evidence of a successful installation, complete release or reproduced result. Licenses should be inspected before reuse.

## Exclusions and follow-up

- Do not re-add 2025 works such as Evo-Memory, Agent-R1 or AgentEvolver simply because they appear in 2026 discussion; this repository already tracks that period. Global cleanup of pre-existing duplicates is outside this update.
- ParaGUIBench (2607.22689), HybridDeepResearch (2609.09410), FrontierFinance (2608.11683), and Efficient GUI Agents (2609.02309) remain candidates: primary-page retrieval failed in this pass, so no substantive entries or numbers are imported from mirrors.
- The unusually broad claims in “DeepResearch Agent System” (2607.27562) were not promoted into this curated selection without a stronger artifact/protocol audit.
- SWE-Bench Pro Verified (2609.08149) is distinct from Scale's Pro V2. It remains a follow-up for a full benchmark-version comparison, not an alias to deduplicate into V2.
- Next useful validation: inspect LiteResearcher and VPR full protocols; run small-model memory/safety baselines; pin exact artifact revisions and compatible environments before attempting reproduction.

## Suggested commit

`docs: add curated 2026 agent research, releases and evaluation caveats`

Validation: normalized arXiv-ID/title deduplication against the baseline; all new local Markdown targets and anchors checked; `git diff --check`; generated patch applied successfully to a clean baseline checkout.
