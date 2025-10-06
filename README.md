# Prompt of Prompt（用“提示词的提示词”做模板）

用一个“元提示词”快速产出可复用模板，对照示例结果，自检并拿到结构化输出。

— v0.1-preview · 2025-10-06

## 它能做什么
- 从“元提示词”生成你的专属模板（含 `{{变量位}}`）。
- 提供现成模板与示例结果，帮助不懂技术也能对齐交付标准。

## 我该用哪个文件
- [PROMPT_OF_PROMPT.md](PROMPT_OF_PROMPT.md)：元提示词（拿它去问模型，生成你的模板）。
- [templates/WEBSITE_DOC_ANALYSIS.md](templates/WEBSITE_DOC_ANALYSIS.md)：网站文档分析模板。
- [templates/advanced/QUANT_TRADING_SIMONS_TEMPLATE.md](templates/advanced/QUANT_TRADING_SIMONS_TEMPLATE.md)（可选）：量化项目技术文档模板（西蒙斯理念内嵌版）。
- [samples/WEBSITE_DOC_ANALYSIS_SAMPLE.md](samples/WEBSITE_DOC_ANALYSIS_SAMPLE.md)：示例结果（用于对齐标准）。

## 3 步上手
1) 打开你常用的 AI（Claude / OpenAI 等）。
2) 发送这段话：
```
请阅读仓库中的 PROMPT_OF_PROMPT.md。我的场景是「{{你的场景}}」。请基于它生成一个可复用的提示词模板（Markdown），变量位用 {{var}} 标注。
```
3) 把生成的模板应用到目标；若是网站分析，也可直接用 [templates/WEBSITE_DOC_ANALYSIS.md](templates/WEBSITE_DOC_ANALYSIS.md)；最后对照 [samples/WEBSITE_DOC_ANALYSIS_SAMPLE.md](samples/WEBSITE_DOC_ANALYSIS_SAMPLE.md) 自检，补齐缺项再交付。

## 对齐要点（最小集）
- 结构完整：执行摘要/架构/组件/数据流/建议/风险/清单。
- 工件足量：必要的图/表/清单占位。
- 可执行：写出具体技术名与步骤。

## 常见问题
- 不会用 Playwright/MCP？不需要，手工遍历页面也可以。
- 模板需要英文名吗？建议模板文件全大写英文（如 `PROMPT_X.md`），输出结果文件不限。

## 版本与许可
- v0.1-preview（2025-10-06）；License：TBD。欢迎 PR。
