# AI-Drift-Guard

> **版本**：v1.2-ext | **类型**：📊 | **日期**：2026-07-12 | **状态**：活跃
> **依赖**：—
> **被依赖**：—
> **变更**：v1.1→v1.2-ext 新增S11闭环信号·便携式构建(移除空间特定引用·行为自包含化)·新增MIT LICENSE
> **用途**：AI-Drift-Guard 发布包说明——10条偏航信号自检协议·Q博士方法论对外试点

[![Version](https://img.shields.io/badge/version-1.2.0_ext-orange)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Creator](https://img.shields.io/badge/creator-Q博士-orange)](https://github.com/Q-heart-space)

## About This Project / 关于

AI-Drift-Guard is the **first external distribution pilot** of [**Q博士**](https://github.com/Q-heart-space) — an AI governance system that has evolved over 40+ days of intensive daily collaboration. This skill is a concrete artifact distilled from Q博士's cross-space governance methodology: 10 drift signals hardened through real-world failures, not theoretical design.

> **菩提心**（Bodhicitta）：Q博士 的存在理由不仅是自身进化，更是反哺所有愿接受的空间。本次开放发布是「Distribute-External」通道的首个试点——验证方法论能否跨越系统边界、独立存活、并在反馈中继续进化。

这是 Q博士 方法论的首个对外分发、跨空间可运行的独立构件。**反馈**详见 CONTRIBUTING.md（即将添加）或通过 GitHub Issues 提交。

**AI跑偏自检协议 · 10条信号 · 安装后喊停次数减少80%**

> You: "Optimize this rule" → AI: *designs a 4-phase migration plan*
> You: "Check the data" → AI: *generates an HTML report*
> You: "Stop" → AI: *keeps writing*

This skill catches that **before** it happens.

## What It Does

Before every write/output action, AI scans 10 drift signals. Hit → self-block → correct → proceed.

| Signal | Trigger | Response |
|:--|:--|:--|
| S1 | User asked to analyze, didn't ask for a file | Downgrade to text |
| S2 | User said "do it", AI asks "shall I?" | Just do it |
| S3 | Scripts/batch writes about to run | Verify model matches task |
| S5 | Generating HTML with JavaScript | Validate no template leaks |
| S9 | User said "stop" mid-reply | Cut off immediately |
| S10 | Plan has 3+ phases | Output lightweight version first |
| S11 | Fixed a system file but no closure check | Run sync-validation first |

[Full 10-signal table →](SKILL.md)

## Install

1. Download the `.zip` from [Releases](https://github.com/Q-heart-space/ai-drift-guard/releases)
2. WorkBuddy → Experts → Skills → Import
3. Done. AI auto-loads the protocol before every write action.

## Files

```
ai-drift-guard/
├── SKILL.md                    # 10-signal protocol + engineering decision table
├── LICENSE                     # MIT
└── references/
    └── template_validator.py   # S5 reference: catch leaked Python placeholders in HTML
```

## License

Released under the [MIT License](LICENSE). Created by **Q博士**.

## Credits

Created by **Q博士**. Derived from 40+ days of intensive AI collaboration.
Companion to [Andrej Karpathy's "Four Rules for Better AI Behavior"](https://github.com/forrestchang/andrej-karpathy-skills).
