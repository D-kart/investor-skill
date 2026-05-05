# 投资备忘录 / Equity Research 模板（Investment Memo · v1.0.2）

> 本模板严格对齐 `assets/page-shells/memo-shell.md` 的 9 Sections 罗马章节结构 + 顶部 KPI Snap-Bar。
> HTML 输出请同时引入 `assets/design-tokens.css`（专业券商研报视觉令牌）。
>
> **硬性规则提醒**：
> - 未披露字段 **直接省略行或写"未披露"**，禁用 `⚠️ 待补`、`--`。
> - 技术壁垒 / 护城河 / 产品力 **用事实定量论证**，禁用 1-5 星 / N/25 分聚合数。
> - 每份报告只就本标的论事实，禁止跨标的引用（"相比 XX""不同于 XX 类"）。
> - HTML 输出：深色底块（callout-strip / verdict-box / blueteam-box）必须用 `</div>` 闭合，严禁与 `</p>` 错配。

---

## 顶部结构

### 信笺顶 Letterhead
```
[机构名 + skill 版本]                         [机密 · 日期 · 版本 · 分析师]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  STRICTLY CONFIDENTIAL — FOR INTERNAL & QUALIFIED INVESTOR USE ONLY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Title Block
- 类别：Equity Research · 一级市场深度投资研究报告
- 大标题：公司中文名 · 英文名
- 副标题：一句话定位 + 本轮融资轮次

### Rating Pills（3 个）
- 投资评级 Pill（积极跟进 / 谨慎跟进 / Pass）
- 阶段 Pill（轮次 + 融资额）
- 关键关注 Pill（最需尽调的一点）

### Snap-Bar KPI 横条（5 个核心数字）
示例：本轮融资 / 当前营收 / 预期营收 / 市场规模 / 关键运营指标

---

## 9 Sections 内容指引

### I · Executive Summary · 投资核心摘要
- 2-3 段正文：是什么 · Why Now · 团队 · 商业落地 · 核心结论
- 中间嵌一条 `callout-strip` 金句条（深蓝底白字，必须 `</div>` 闭合）
- 段尾给出整体评级

### II · Company Overview · 公司基本面
- `data-table` 双列：全称 / 成立 / 注册地 / 主营 / 资质 / IP / 团队规模 / 行业声誉 / 子公司
- 字段未披露则**直接删行**

### III · Industry & Market · 行业与市场机遇
- 一段赛道定义论证
- `market-bar` 4 个核心数字横条
- `note-text` 注明来源
- `ws-list` 4-6 条 Why Now 驱动力（每条挂事实 + 年份）

### IV · Technology / Product Deep Dive · 技术与产品深度解析
- 一段技术逻辑论证（不打分）
- `tech-pillar-grid` 三立柱核心技术
- `note-text` 注明第三方验证状态
- **技术壁垒定性论证** —— 6 条叙事化条目（事实证据 + 复制难度 + 威胁来源）
- 章末 1-2 段总结（不输出聚合分数）

### V · Competitive Landscape · 竞争格局
- **A · 核心参数对标表** comp-table
- **B · 技术方案对标表** comp-table
- **C · 同赛道生态位表** comp-table
- 标的公司置最后一行用 `highlight-row` 高亮
- `highlight-grid` 双栏：差异化优势 / 最大威胁

### VI · Business Model & Financials · 商业模式与财务
- 一段商业模式论证
- 三张数据表：A 营收预测 / B 历轮融资 / C 本轮用途
- `ws-list` 商业落地证据（含客户名 + 数据 + 时间）

### VII · Blue Team Risk Assessment · 蓝军反驳视角
- `blueteam-box` 视角说明（红色边框 + 浅红底）
- `risk-table` ≥ 6 行（风险类别 / 蓝军核心论点 / 等级 / 验证路径）
- 等级 CRITICAL / HIGH / MEDIUM / LOW-MED / LOW

### VIII · Investment Recommendation · 投资建议
- `verdict-box` 4-5 段综合评价
- `verdict-rating` 明确三选一（积极跟进 / 谨慎跟进 / Pass）
- `highlight-grid` 双栏：看多催化剂 / 下行风险场景

### IX · Key Milestones & Action Items · 跟踪节点与待办
- `data-table` 8-10 行尽调待办（维度 / 具体指标 / 目标时间 / 重要性）
- 时间用"14 天内 / 30 天内 / 45 天内 / 持续跟踪"

---

## 尾部

### Analyst Signature
- 左：分析师名 + skill 版本 + 机构 + 研究方向
- 右：报告日期 + 版本 + 密级

### Footer 免责声明
- 数据真实性未独立核实
- 第三方数据存在估计误差
- 蓝军视角为情景演练
- 投资决策请结合专业顾问意见
- 版权声明

---

## 交付前自检清单

- [ ] 9 章节罗马编号 I-IX 齐全？
- [ ] Snap-Bar 5 个数字，每个有 label / value / sub？
- [ ] Section VII 蓝军视角至少 6 条，含至少 1 条 CRITICAL？
- [ ] `<div class="callout-strip">`、`<div class="verdict-box">`、`<div class="blueteam-box">` 均用 `</div>` 闭合？
- [ ] grep `⚠️\|待补` = 0？
- [ ] grep `★\|N/25\|打分` = 0？
- [ ] grep 确认无跨标的引用（"相比 XX""不同于 XX 类"）？
- [ ] 未披露字段已留空 / 省略，而非挂标签？
