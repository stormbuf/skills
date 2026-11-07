# PRD 需求文档规范

> 定位：管「需求怎么结构化」——EARS 需求语法与 Gherkin 验收场景。措辞层（背景、目标、方案取舍等解释文字）按本 skill 的 `google` / `hybrid` 规则执行。
> 优先级：本文件的形式语法优先于 `ste.md` 的表层句法（如 5.3 祈使句）；STE 只借底层原则：条件在前、一句一条、明确施事、不用含糊词、术语全文一致。
> 迁移来源：用户级 AGENTS.md「产品需求文档（PRD）」章节（2026-11-07 迁入）。

## 适用范围

用户要求写 PRD、需求文档、需求分析结论、用户故事、验收标准时，读取并应用本文件。

## EARS 需求语法

- 每份 PRD 必须使用 EARS（Easy Approach to Requirements Syntax，简易需求描述法）描述需求行为。
- 每条行为需求选用适用的 EARS 模式：
  - 普适（Ubiquitous）：`The <system> shall <response>.`
  - 事件驱动（Event-driven）：`When <trigger>, the <system> shall <response>.`
  - 状态驱动（State-driven）：`While <state>, the <system> shall <response>.`
  - 非期望行为（Unwanted behavior）：`If <unwanted condition>, then the <system> shall <response>.`
  - 可选功能（Optional feature）：`Where <feature is included>, the <system> shall <response>.`
- 需求依赖多个条件时，组合使用多种模式。
- 需求必须原子化、可测试、无歧义，并分配稳定的需求 ID。

## Gherkin 验收场景与验收标准

- 每份 PRD 必须用 Gherkin 列出验收场景与验收标准。
- 使用关键字 `Feature`、`Scenario`、`Given`、`When`、`Then`；需要时用 `And` 或 `But`。
- 每条有行为意义的 EARS 需求必须映射到至少一个 Gherkin 场景。
- 每个 Gherkin 场景必须标注它所验证的需求 ID。
- 适用处应覆盖正常流程、边界条件、相关失败路径，以及恢复/幂等场景。
- 只有当映射的 Gherkin 场景具体到无需臆造缺失行为即可自动化或人工执行时，验收标准才算完整。

## 与本 skill 其他规则的配合

- PRD 里的解释文字（背景、目标、痛点、方案取舍）是解释块，按 `google` 风格；需求条目与验收场景按本文件的形式语法。
- STE 原则照常约束需求条目的措辞：一词一义（1.1、1.3）、不用含糊词（中文：适当、基本、显著、大幅；英文：appropriate、significantly、various）、条件在前（5.4）、明确施事（3.6）、需求 ID 与术语全文一致（9.4）。
- 中文 PRD：EARS 与 Gherkin 关键字保留英文原文（`The system shall`、`Feature`、`Given`）；条件与动作内容用中文写，中文与英文、数字之间加空格。
- 交付前核对：每条 EARS 需求有稳定 ID；每条需求至少映射一个 Gherkin 场景；场景标注所验证的需求 ID；含糊词为零容忍项。
