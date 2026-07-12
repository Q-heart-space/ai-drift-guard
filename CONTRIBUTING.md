> **版本**：v1.0 | **类型**：📋 | **日期**：2026-07-12 | **状态**：活跃
> **变更**：v1.0 首建——自动注入标准头（header_auto_inject·铁律AR R3 落地）
> **依赖**：asset_health_check.py（豁免/目录策略真相源）
> **被依赖**：每日22:00治理（health 前置步骤）
> **用途**：本文件由 header_auto_inject 自动补头；请补充真实用途/依赖

# Contributing / 参与指引

感谢你关注 AI-Drift-Guard！这是 [**Q博士**](https://github.com/Q-heart-space) 方法论的首个对外试点。

## How to Contribute / 如何参与

### 🐛 Report Issues
Found a false positive? A signal that should fire but doesn't? [Open an Issue](https://github.com/Q-heart-space/ai-drift-guard/issues).

Please include:
- Your AI platform / environment
- The trigger condition that should have been caught
- What actually happened

### 💡 Suggest Improvements
- **New signal**: Describe the drift pattern you've observed, with real examples
- **Better signal response**: If a response is too vague or too aggressive, suggest refinements
- **Portability**: Any instructions still referencing a specific tool/platform → file an Issue

### 🔧 Submit Changes
1. Fork the repo
2. Make your changes in `SKILL.md` or `references/`
3. Submit a Pull Request with a clear description

### 📢 Share Your Experience
Use it in your own AI workspace? Open an Issue with your feedback — good or bad. Every signal that caught or missed real drift helps harden the protocol.

## Version Strategy

| Label | Meaning |
|:--|:--|
| `v1.x-ext` | External portable build — the published version |
| Internal `v1.x` | Q博士 workspace source of truth (unpublished, has full context) |

External builds are **snapshot ports** of the internal version. They may lag by one minor version. `CHANGELOG.md` documents all external-facing changes.

## License

This project is [MIT](LICENSE) licensed. Contributions are accepted under the same license.
