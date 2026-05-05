# 投资备忘录 / Equity Research · 页面骨架壳（memo-shell · v1.0.1）

> 本文件定义投资备忘录 / 一级市场研报的**视觉/结构骨架**。
> 风格基准：专业券商深度研报（Times New Roman + 深蓝主调 + 米白纸面 + 罗马章节）。
> 任何 HTML 输出都严格映射到这 9 个章节。

---

## 骨架结构（罗马章节 · 9 Sections + 顶部 KPI 横条）

```
┌──────────────────────────────────────────────────────────────────┐
│ [信笺顶 Letterhead]    机构名 · 研究类别 │ 机密 · 日期 · 版本    │
│ [机密带 Confidential band]                                       │
│ [报告标题 Title]    报告类别 · 大标题 · 副标题                   │
│ [评级三标 Rating]    评级 · 阶段 · 风险等级（彩色 Pill）         │
│ [快照 KPI Snap-Bar]  4-5 个核心数字横条                          │
├──────────────────────────────────────────────────────────────────┤
│ I.   Executive Summary · 投资核心摘要                            │
│ II.  Company Overview · 公司基本面                               │
│ III. Industry & Market · 行业与市场机遇                          │
│ IV.  Technology / Product Deep Dive · 技术与产品深度解析         │
│ V.   Competitive Landscape · 竞争格局（含定量对标矩阵）          │
│ VI.  Business Model & Financials · 商业模式与财务                │
│ VII. Blue Team Risk Assessment · 蓝军反驳视角与风险              │
│ VIII.Investment Recommendation · 投资建议（含 Verdict Box）      │
│ IX.  Key Milestones / Action Items · 跟踪节点与待办              │
├──────────────────────────────────────────────────────────────────┤
│ [分析师签 Analyst Signature] · [免责声明 Footer]                 │
└──────────────────────────────────────────────────────────────────┘
```

---

## 章节内容指引

### I · Executive Summary
- 2-3 段正文，覆盖：是什么 · 为什么现在 · 团队 · 商业落地 · 核心结论
- 中间嵌一条 **Callout Strip**（金句条）
- 段尾给出整体评级（"积极跟进 / 谨慎观察 / Pass"）

### II · Company Overview
- `data-table` 双列：公司全称 / 注册地 / 阶段 / 核心产品 / 核心技术 / 目标客户 / 研发合作 / 联系方式

### III · Industry & Market
- `market-bar` 4 个核心数字横条（TAM / CAGR / 细分规模 / 上下游需求）
- 数据源行（Research and Markets · Gartner · TrendForce · IoT Analytics 等）
- `ws-list` 4-6 条要点：Token 需求 / AI 服务器 / 国产替代 / 模型架构演进等驱动力

### IV · Technology / Product Deep Dive
- 一段技术逻辑论证文字（**不打分**，用产业事实和定量描述说话）
- `tech-pillar-grid` 三立柱：核心技术支柱（每柱 = 标题 + 正文 + 性能标签 perf badge）
- `note-text` 注明数据真实性提示（"以上数据均为公司声称，待第三方测试验证"）
- 算法/产品全栈能力补充段

### V · Competitive Landscape
- **A · 国际竞争格局** comp-table（≥ 5 行）
- **B · 国内竞争格局** comp-table（≥ 4 行）
- 标的公司放在最后一行用 `highlight-row` 高亮
- `highlight-grid` 双栏：差异化优势 + 最大威胁
- 单元格用 `star-high / star-med / star-low` 颜色标签

### VI · Business Model & Financials
- 收入结构（产品 / 算法授权 / 服务 / 第二曲线）
- 落地案例表（客户 · 披露状态 · 推导价值）
- 涉及未披露的财务数据：**留空或写"未披露"，不做"⚠️ 待补"标签**

### VII · Blue Team Risk Assessment
- `blueteam-box` 蓝军视角说明（红色边框 + 浅红底）
- `risk-table` ≥ 6 行风险矩阵：
  - 风险类别 / 蓝军核心论点 / 等级 / 验证路径或缓释条件
  - 等级标签：CRITICAL / HIGH / MEDIUM / LOW-MED / LOW

### VIII · Investment Recommendation
- `verdict-box` 综合评价：3-4 段长文字 + 一个 verdict-rating 标签
- `highlight-grid` 双栏：看多核心催化剂 / 核心下行风险场景

### IX · Key Milestones / Action Items
- `data-table` 跟踪表：跟踪维度 · 具体指标 · 目标时间 · 重要性
- 含技术验证 / 基准测试 / 商业化 / 融资节点 / 团队补全 / 生态建设 / 竞争监控

### 分析师签 + 免责声明
- 左：首席分析师 + 机构 + 研究方向
- 右：日期 + 版本 + 密级
- 免责声明：标的真实性未经独立核实 · 第三方数据存在估计误差 · 蓝军分析为情景演练 · 投资决策请结合专业意见

---

## 硬性规则

1. **专业研报范，不用儿化语**：杜绝"老大""仅供参考"等口语；用"投资人""投资决策"等正式表述。
2. **数据缺失就留空 / 写"未披露"**：不再使用 `⚠️ 待补` 标签；不再使用 `--`；如果整行字段未披露，**直接省略该行不写**。
3. **不打分**：技术壁垒、护城河、产品力等评估**用文字说事实和定量数据**，不用 1-5 星 / 16/25 分。
4. **结论必须明确且可决策**：`verdict-rating` 三选一：积极跟进 · 谨慎观察 · Pass / 不予推进。
5. **风险用 CRITICAL/HIGH/MEDIUM/LOW**：不用"红/黄/绿"或"高/中/低"中文版（除非完全中文化报告）。
6. **数字单位统一**：金额（亿元 / 万元 / $ 亿）· 增速（%）· 倍数（x）· 时间（YYYY Q? / YYYY-YYYY）。
7. **每段事实必须挂数据或来源**；推断必须标注"推断 / 基于 SOP 测算"。
8. **蓝军视角必备**：VII 章不能跳过，是专业研报的标志。
9. **报告独立性**：每份报告**只评本标的**，禁止以"相比 XX""不同于 XX 类"等表述引用其他标的（即使是同一个 skill 跑过的项目）。投资人读一份报告时，只想看到关于这家公司的事实与判断，不需要被其他案例分散注意力。
10. **HTML 标签闭合校验**：`<div class="callout-strip">` 等深色底块必须用 `</div>` 闭合，**严禁用 `</p>` 错配**——否则后续 `<p>` 段落会继承父级深色背景，黑字深底导致内容不可见。生成 HTML 后必须 grep 检查 `<div class= ` 与 `</div>` 数量匹配。

---

## 视觉规则（与 design-tokens.css 联动）

- 主体色：`--opc-brand-primary` #1a1a4e（深海军蓝）
- 强调色：`--opc-bull-green` #0a6e2a（看多）/ `--opc-bull-red` #8b0000（高风险）/ `--opc-warn` #7a4f00（中等）
- 字体：`--opc-font-serif`（Times New Roman + Songti SC）作正文；`--opc-font-sans`（Arial + PingFang SC）作表头/标签/章节标题
- 背景：`--opc-bg-canvas` #f4f1eb（页外）+ `--opc-bg-page` #fff（纸面）+ `--opc-bg-soft` #faf9f6（高光块）
- 表格：表头深蓝底白字 + 偶数行米白斑马 + 标的高亮行 `highlight-row`
- 章节编号：罗马大写 I-IX + `· 中文 · English`

---

## 出厂模板

任何 HTML 报告都从 `assets/templates/investment-memo.md` 出发，套上 `assets/design-tokens.css`，按本骨架填内容即可。
