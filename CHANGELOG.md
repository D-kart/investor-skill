# Changelog

本 skill 遵循 [Semantic Versioning](https://semver.org/lang/zh-CN/) 与 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/) 规范。

---

## [1.0.2] - 2026-05-05

### Fixed
- **HTML 标签闭合 bug 修复**：写报告时容易把 `<div class="callout-strip">` 错配成 `</p>` 闭合，导致后续 `<p>` 段落继承父级深色背景出现"黑字深底"不可读。`memo-shell.md` 与 `references/06-investment-memo.md` 增加硬规则：深色底块必须用 `</div>` 闭合，生成后必须 grep 校验。

### Changed
- **报告独立性原则**：`memo-shell.md` 与 `references/06-investment-memo.md` 增加硬规则——禁止跨标的引用（不写"相比 XX""不同于 XX 类"等表述）。每份报告只就本标的论事实、给判断，不被其他案例干扰投资人的注意力。

### Rationale
- 用户在清研微视报告中发现两处问题：① "本报告结论"段因父级 callout-strip 闭合错配显示成黑字深底不可见；② 段中提到了"不同于聆思类纯市场驱动"，跨项目引用降低专业度。两处都已落地为 skill 的硬规则，避免下次重犯。

---

## [1.0.1] - 2026-05-05

### Changed
- **重大风格升级**：`assets/design-tokens.css` 完整重写，对标专业券商研报范（深蓝主调 #1a1a4e + 米白纸面 + Times New Roman + 罗马章节 + 信笺顶 + 机密带）。
- `assets/page-shells/memo-shell.md` 由 10 Blocks 重构为 9 Sections（罗马章节 I-IX + 顶部 KPI Snap-Bar），强制蓝军反驳视角章节。
- `references/04-competitive-landscape.md` 删除"护城河 5 维度评分卡"，改为定性论证范式。
- `references/05-tech-product.md` 删除"技术壁垒五维评估打分"，改为定性论证范式。
- `references/06-investment-memo.md` 写作规则更新：未披露字段**留空 / 省略**，不再使用 `⚠️ 待补` 标签；明令禁止 1-5 星 / N/25 分等聚合打分。

### Added
- design-tokens 新增组件：letterhead · confidential band · rating pills · snap stats bar · market bar · tech pillar grid · verdict box · blue team box · comp matrix · risk table。
- memo-shell 强制章节 VII Blue Team Risk Assessment（蓝军反驳视角）。

### Rationale
- 用户反馈：原 10 Blocks 排版偏"工整 markdown"风，专业感不足；产业研报范才是真正给 IC 用的。
- 用户反馈：技术壁垒 / 护城河打分主观且容易误导决策，应改为事实陈述。
- 用户反馈：未披露字段挂 ⚠️ 标签让报告看起来"残缺"——专业研报应直接省略行或归到风险表。

---

## [1.0.0] - 2026-05-05

### Added
- 首个公开版本。
- META 层：`SKILL.md`、`CHANGELOG.md`、`GLOSSARY.md`、`README.md`、`LICENSE`。
- ASSETS 层：`design-tokens.css`、`page-shells/memo-shell.md`、三份核心模板（行研 / 尽调 / 投资备忘录）。
- REFERENCES 层：六项技能 SOP（行研 / 尽调 / BP 分析 / 竞争格局 / 技术产品 / 投资备忘录）+ case-studies 模板。
- 兼容性声明：Claude Skills / WorkBuddy / OpenClaw / Hermes / SkillHub 全平台可用。

### Design Principles
- 遵循 agentskills.io 开放规范，frontmatter 覆盖关键触发词。
- 三层架构（META / ASSETS / REFERENCES），按需加载降低 token 成本。
- 所有 SOP 产出物结构化，支持直接进入投委会流程。

---

## [Unreleased]

### Planned
- 增加中文专业语料的 few-shot 示例。
- 补充 2-3 个完整的脱敏 case-study。
- 补齐港股 / 美股一级市场的 carve-out 版本。
