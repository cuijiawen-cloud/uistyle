# Game UI Replacement Rules

这是一个用于沉淀“游戏工具替换 UI”的规则库。

目标：把不同游戏风格下的 UI 替换规则拆成可维护、可迭代、可审查的文档，便于后续被设计、Maker 工程、资源生产和 QA 共同使用。

## 文档目录

| 编号 | 文档 | 用途 |
|---|---|---|
| 01 | [游戏风格理解](docs/01-game-style-understanding.md) | 定义风格识别、气质、视觉关键词与禁区 |
| 02 | [背景规则](docs/02-background-rules.md) | 定义背景场景、层级、可读性与替换边界 |
| 03 | [9-slice 面板规则](docs/03-9-slice-panel-rules.md) | 定义面板切片、拉伸、边角、材质与复用规范 |
| 04 | [状态视觉规则](docs/04-state-visual-rules.md) | 定义 normal/hover/pressed/disabled/selected 等状态 |
| 05 | [装饰语义规则](docs/05-decoration-semantic-rules.md) | 定义装饰物的语义、位置、密度与不可干扰原则 |
| 06 | [Maker 工程约束](docs/06-maker-engineering-constraints.md) | 定义 Maker 可实现性、组件化与动效限制 |
| 07 | [资源预算](docs/07-asset-budget.md) | 定义图片、图集、粒子、字体、动效等预算 |
| 08 | [尺寸边界](docs/08-size-boundaries.md) | 定义最小/最大尺寸、适配、留白与安全区 |
| 09 | [QA 失败归因](docs/09-qa-failure-attribution.md) | 定义验收失败类型、归因方式与修复优先级 |

## 建议使用方式

1. 每次新增一个游戏风格时，先补充 `01-game-style-understanding.md`。
2. 再按背景、面板、状态、装饰、工程、预算、尺寸、QA 的顺序补齐规则。
3. 每个规则变更建议通过 PR 审阅。
4. QA 失败案例统一回填到 `09-qa-failure-attribution.md`，避免重复踩坑。
