# 投资人.skill · investor-skill

> 把 AI Agent 变成一名冷静、结构化、可落地的一级市场机构投资人。

![version](https://img.shields.io/badge/version-1.0.2-blue)
![license](https://img.shields.io/badge/license-MIT-green)
![platforms](https://img.shields.io/badge/platforms-Claude%20%7C%20WorkBuddy%20%7C%20OpenClaw%20%7C%20Hermes%20%7C%20SkillHub-orange)
![made by](https://img.shields.io/badge/made%20by-OPC--Studio-black)
![style](https://img.shields.io/badge/style-Equity%20Research-1a1a4e)

---

## 这是什么

`investor-skill` 是一个符合 [agentskills.io](https://agentskills.io) 开放规范的 AI Agent 技能包。
安装后，你的 Agent 将具备一名**一级市场职业机构投资人**的完整工作能力——
从行业研究到投资备忘录，全流程一体化输出**专业券商研报范**的 HTML 报告。

## 它能做什么

| # | 能力 | 产出 |
|---|---|---|
| 1 | **行业研究** | 结构化行研报告（含 TAM/SAM/SOM 测算 + Why Now 驱动力） |
| 2 | **项目尽职调查** | 业务 / 财务 / 法务 / 团队 四维尽调清单 + 尽调纪要 |
| 3 | **商业计划书快速分析** | BP 速析报告（亮点 / 疑点 / 必问清单 + 九要素打分） |
| 4 | **竞争格局分析与市场定位** | 竞争矩阵 + 定位图 + 护城河定性论证（**不打分**） |
| 5 | **核心技术与产品特点呈现** | 技术卖点提炼 + 差异化拆解 + 五维壁垒定性论证 |
| 6 | **投资备忘录撰写** | 投委会可用的 Investment Memo（HTML 专业研报范） |

## 何时触发

> 投资人、VC、PE、FA、看项目、过会、投决、投资备忘录、尽调、DD、行研、BP 分析、商业计划书、赛道研究、市场分析、竞争格局……

## 核心输出风格

输出使用**专业券商深度研报**视觉语言：
- 🎨 深蓝主调 `#1a1a4e` + 米白纸面 `#f4f1eb`
- 📜 Times New Roman + Arial 表头 + 罗马大写章节 I-IX
- 📋 信笺顶 Letterhead + 机密带 Confidential Band
- 📊 Snap-Bar 5 KPI 横条 + 竞争对标矩阵 + 蓝军反驳视角
- ⚖️ Verdict Box 投资建议盒 + Analyst Signature

## 快速上手

### 在 Claude / WorkBuddy 中使用
1. 下载 `investor-skill/` 文件夹，放入 `~/.claude/skills/` 或 `~/.workbuddy/skills/`。
2. 重启客户端，向 Agent 说：**"帮我看下这个项目"** 或 **"把这份 BP 整理成投资备忘录"**，技能自动触发。

### 在 OpenClaw / Hermes 中使用
1. 将 `investor-skill/` 放入 `skills/` 目录。
2. 通过 `skill_view` 查看 SKILL.md 加载。

### 在 SkillHub 中使用
1. 打包：`zip -r investor-skill.zip investor-skill/`
2. 登录 SkillHub，点击"上传 Skill"，选择 zip 文件。

## 目录结构（17 件文件 · 三层架构）

```
investor-skill/
├── SKILL.md                          # 主路由（必读）
├── CHANGELOG.md                      # 版本日志
├── GLOSSARY.md                       # 术语字典（LP/GP/TS/DD/MOIC/IRR…）
├── README.md                         # GitHub 门面
├── LICENSE                           # MIT
├── assets/
│   ├── design-tokens.css             # 专业研报视觉令牌
│   ├── page-shells/
│   │   └── memo-shell.md             # 备忘录 9 Sections 骨架
│   └── templates/
│       ├── industry-research.md      # 行研报告模板
│       ├── dd-checklist.md           # 尽调清单模板
│       └── investment-memo.md        # 投资备忘录模板
└── references/
    ├── 01-industry-research.md       # 行业研究 SOP
    ├── 02-due-diligence.md           # 四维尽调 SOP
    ├── 03-bp-analysis.md             # BP 速析 SOP
    ├── 04-competitive-landscape.md   # 竞争格局 SOP
    ├── 05-tech-product.md            # 技术产品 SOP
    ├── 06-investment-memo.md         # 投资备忘录撰写 SOP
    └── case-studies/
        └── case-template.md          # 案例库模板
```

## 六条设计哲学

1. **沉稳、理性、重证据**：先求真，再求好。
2. **结构化输出**：每个结论都有三段式支撑——事实 / 推理 / 判断。
3. **风险前置**：Red Flag 写在正文前面，不粉饰。
4. **可决策**：输出的是"投 / 跟投 / 继续跟进 / Pass"，不是描述。
5. **不打分**：技术壁垒 / 护城河用事实定量论证，拒绝主观评分。
6. **报告独立性**：每份报告只评本标的，不跨标的引用。

## 兼容性

| 平台 | 状态 | 备注 |
|---|---|---|
| Claude Skills | ✅ | 遵循 agentskills.io 规范，frontmatter 覆盖触发词 |
| WorkBuddy | ✅ | 原生支持 |
| OpenClaw | ✅ | 通过 clawhub 兼容 |
| Hermes Agent | ✅ | 通过 agentskills.io 标准 |
| SkillHub | ✅ | zip 上传 |

## 与 OPC-Studio 其他 skill 协同

本 skill 可与 [`presenter-skill`](../presenter-skill/)（路演者.skill）配合使用：
- **investor-skill** 扮演审判者（看项目 / 找雷 / 判断投否）
- **presenter-skill** 扮演被审判者（讲项目 / 争取 TS）
- 创始人可用 presenter-skill 写 BP，再用 investor-skill 自检打分，识别可能被投资人挑刺的点。

## 许可证

MIT License · © 2026 OPC-Studio

## 反馈与贡献

- Issue / PR：欢迎在本仓库提交
- 兼容问题：请附上平台名与 Agent 版本号
- skill 建议：期待跨赛道的 case-study 贡献

---

*OPC-Studio 出品 · 让每个 AI Agent 都能成为行业专家。*
