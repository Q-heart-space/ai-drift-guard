# AI-Drift-Guard

[![Version](https://img.shields.io/badge/version-1.1.0-blue)](CHANGELOG.md)
[![Creator](https://img.shields.io/badge/creator-Q博士-orange)](https://github.com/Q-heart-space)

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

[Full 10-signal table →](SKILL.md)

## Install

1. Download the `.zip` from [Releases](https://github.com/Q博士/ai-drift-guard/releases)
2. WorkBuddy → Experts → Skills → Import
3. Done. AI auto-loads the protocol before every write action.

## Files

```
ai-drift-guard/
├── SKILL.md                    # 10-signal protocol + engineering decision table
└── references/
    └── template_validator.py   # S5 reference: catch leaked Python placeholders in HTML
```

## Credits

Created by **Q博士**. Derived from 40+ days of intensive AI collaboration.
Companion to [Andrej Karpathy's "Four Rules for Better AI Behavior"](https://github.com/forrestchang/andrej-karpathy-skills).
