---
name: ai-drift-guard
description: "AI-Drift-Guard / AI跑偏守卫：10-signal self-check protocol that catches AI drift before execution. 在AI写方案、生成文件、批量修改前自动扫描10种跑偏信号，发现即阻断。Prevents over-engineering (optimize-this-rule → 4-phase-migration), format-creep (check data → HTML report), scope-bloat (fix-one → fix-all). Reduces 'stop' commands by 80%. 安装后AI每次动手前先自检。"
version: 1.1.0
agent_created: true
creator: Q博士
tags: [guard, anti-drift, over-engineering, quality, self-check, bilingual]
---

# AI-Drift-Guard — AI跑偏自检协议 / Drift Self-Check Protocol

> EN: A 10-signal protocol that catches AI drift BEFORE execution.
> 中：10条偏航信号，在AI跑偏之前拦下来。

## Pain Points You Know Too Well / 你一定遇到过的痛点

| EN | 中 |
|:--|:--|
| "Optimize this rule" → AI designs a 4-phase migration | "优化一下规则" → 它给了个4阶段迁移方案 |
| "Check the data" → AI generates an HTML report | "看看数据" → 它自动生成了HTML报告 |
| "Do it" → AI asks "Shall I?" | "执行" → 它反问"可以吗？" |
| "Stop" → AI keeps writing | "停" → 它还在继续输出 |

**EN: Root cause: AI's default tendency is "go maximal". This skill self-checks BEFORE acting — no need to yell "stop".**
**中：根因：AI的默认倾向是"做重做全"。这个技能在AI动手之前先自检——不用你喊停。**

## When It Triggers / 触发时机

| EN | 中 |
|:--|:--|
| Outputting a multi-step plan or design | 输出多步骤计划或设计方案 |
| Generating files (HTML, PDF, scripts) | 生成文件（HTML/PDF/脚本） |
| Batch writes or bulk modifications | 批量写入或大规模修改 |
| Modifying global config or rule files | 修改全局配置或规则 |
| Saying "done" after fixing one thing | 修一个问题就说"完成了" |

## The 10 Signals / 10条偏航信号

> EN: Scan before any write/output action. Hit → Block → Correct → Retry.
> 中：每次写操作/输出前扫描。命中 → 阻断 → 修正 → 重试。

| # | Trigger Pattern (EN) | 触发模式（中） | Response / 命中后果 |
|:--|:--|:--|:--|
| **S1** | User said "analyze/look/check" but did NOT ask for a file | 用户说"分析/看看"但没说要文件 | ⛔ Downgrade to text. / 降级为文字摘要 |
| **S2** | User said "do it" but AI asks "shall I?" | 用户说"执行"但AI反问"可以吗？" | ⛔ Just execute. / 直接执行 |
| **S3** | Scripts/batch writes about to execute | 脚本/批量写入即将执行 | ⛔ Verify model matches task. / 检查模型匹配 |
| **S4** | Modified a global rule file | 修改了全局规则文件 | ⛔ Complete association scan first. / 先做关联扫描 |
| **S5** | Generating HTML with JavaScript/Chart.js | 生成含JS的HTML文件 | ⛔ Validate no template placeholder leaks. / 校验占位符 |
| **S6** | Fixed one issue, about to say "done" | 修了一个问题就说"完成了" | ⛔ Sweep for similar issues first. / 先扫同类问题 |
| **S7** | User confirmed briefly ("yes"/"ok") | 用户简短确认("对""嗯") | ⚠️ Confirm intent, then act. / 确认意图后再动 |
| **S8** | Multi-step task, skipping intermediate steps | 多步骤中途跳过中间步骤 | ⛔ Return to first incomplete step. / 回到未完成步骤 |
| **S9** | User said "stop" / "停" mid-reply | 用户喊"停"，AI正在长篇回复 | ⛔ Cut off immediately. No analysis. / 立即截断 |
| **S10** | Plan ≥3 phases OR ≥2 new files OR ≥5 steps | 方案≥3阶段/≥2文件/≥5步骤 | ⚠️ Output lightweight version first. / 先出轻量版 |

## Engineering vs. Gradualism / 工程化 vs 渐进式

> EN: Not every fix needs a system. Not every cleanup needs structure.
> 中：不是每个改进都要建系统，不是每个清理都要搭架构。

| Trigger Profile (EN) | 触发特征（中） | Right Approach / 正确做法 |
|:--|:--|:--|
| Systemic risk, cross-project, recurring | 系统性风险·跨项目·多次发生 | ✅ Build it properly / 该工程化 |
| One-off, single-point fix | 单点小问题·一次性场景 | ❌ Over-engineering / 过度工程化 |
| Clear verification path, reusable | 有验证路径·可跨场景复用 | ✅ Build it properly / 该工程化 |
| Pure hypothesis, unverified | 纯假设·未验证 | ❌ Over-engineering / 过度工程化 |
| User said "build a system" | 用户说"建一个系统" | ✅ Full design / 全量设计 |
| User said "optimize/fix/clean" | 用户说"优化/修复/清理" | ⚠️ Start minimal / 先最小可行 |

## Installation / 安装

1. Download `ai-drift-guard.zip` from [Releases] / 下载压缩包
2. WorkBuddy → Experts → Skills → Import / 专家 → 技能 → 导入
3. Done. AI auto-loads the protocol / 完成，AI自动加载

**Reference script** / 参考脚本：`references/template_validator.py` — S5 implementation for catching leaked Python `{}` placeholders in generated HTML.

## Expected Impact / 预期效果

- "Stop" commands reduced by 50%+ / 喊停次数减少50%+
- Over-engineered plans: near zero / 过度工程化方案：趋近零
- Every self-block logged for retrospective / 每次自阻断记录到日志

## Credits / 致谢

Created by **Q博士** / **Q博士**创作。
基于40+天高频AI协作中观察和系统化的真实跑偏模式。
Companion to [Andrej Karpathy's Four Rules](https://github.com/forrestchang/andrej-karpathy-skills).
