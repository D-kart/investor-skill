# Changelog

本 skill 遵循 [Semantic Versioning](https://semver.org/lang/zh-CN/) 与 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/) 规范。

---

## [1.0.3] - 2026-06-10

### Changed
- **全量去聚合分数**：BP 速析、竞争格局、技术产品、投资备忘录、行业研究判断、案例库模板全线统一为**定性论证 + 事实证据**范式，不再出现"九要素打分（满分 50）""1-5 星推荐关注度""护城河评分卡""技术壁垒五维打分""合理性打分"等聚合性数字与星级。
- **BP 九要素**改为「定性研判 + 事实证据」结构，结论收敛到四档明确动作：强烈推荐推进 / 推荐推进尽调 / 可谨慎跟进，需补材料 / Pass。
- **行业研究 Step 6**重写为"赛道结论 + 推荐阶段 + 想投画像 + 劝退画像"叙事化输出。
- **投资备忘录 Block 05 / 06 / 07** 与对应 HTML 模板同步对齐：技术壁垒 / 财务合理性 / 护城河三处显式声明"用事实和定量数据论证，不输出聚合分数"。
- **README 与 SKILL.md** 同步更新对外措辞，将"打分""自检打分"等表述统一替换为"定性研判 / 定性论证"。

### Rationale
- 投资人的真实工作流里，1-5 星 / N/25 分这类聚合数字会把主观直觉藏进数字里，给阅读者一种"已被精算"的错觉。
- 专业研报范的输出需要把判断挂回事实证据，而不是数字。这次升级在六个文件中统一掉了所有残留的打分入口，让 skill 在不同触发点输出的报告风格完全一致。

---

## [1.0.2] - 2026-05-05

### Changed
- **报告独立性原则**：`memo-shell.md` 与 `references/06-investment-memo.md` 增加硬规则——禁止跨标的引用（不写"相比 XX""不同于 XX 类"等表述）。每份报告只就本标的论事实、给判断，不被其他案例干扰投资人的注意力。
- **HTML 输出标签闭合规范**：`memo-shell.md` 与 `references/06-investment-memo.md` 增加硬规则——`<div class="callout-strip">` 等深色底块必须用 `</div>` 闭合，生成后必须 grep 校验配对数量，避免出现段落继承父级深色背景的不可读情况。

### Rationale
- 投资备忘录是给投委会读的，每一份都应当只聚焦本标的；跨标的引用会削弱报告的专业感与独立性。
- HTML 报告需要保证视觉的可读性与稳健性，闭合标签的硬规则是工程化交付的基本要求。

---

## [1.0.1] - 2026-05-05

### Changed
- **重大风格升级**：`assets/design-tokens.css` 完整重写，对标专业券商研报范（深蓝主调 #1a1a4e + 米白纸面 + Times New Roman + 罗马章节 + 信笺顶 + 机密带）。
- `assets/page-shells/memo-shell.md` 由 10 Blocks 重构为 9 Sections（罗马章节 I-IX + 顶部 KPI Snap-Bar），强制蓝军反驳视角章节。
- `references/04-competitive-landscape.md` 将"护城河 5 维度评分卡"重构为定性论证范式。
- `references/05-tech-product.md` 将"技术壁垒五维打分"重构为定性论证范式。
- `references/06-investment-memo.md` 写作规则更新：未披露字段**留空 / 省略**，不再使用 `⚠️ 待补` 标签；明令禁止 1-5 星 / N/25 分等聚合打分。

### Added
- design-tokens 新增组件：letterhead · confidential band · rating pills · snap stats bar · market bar · tech pillar grid · verdict box · blue team box · comp matrix · risk table。
- memo-shell 强制章节 VII Blue Team Risk Assessment（蓝军反驳视角）。

### Rationale
- 原 10 Blocks 排版偏"工整 markdown"风，专业感不足；产业研报范才是真正给 IC 用的视觉语言。
- 技术壁垒 / 护城河的主观打分容易误导决策，应改为事实陈述与定量论证。
- 未披露字段挂 ⚠️ 标签让报告看起来"残缺"——专业研报应直接省略行或归到风险表。

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
