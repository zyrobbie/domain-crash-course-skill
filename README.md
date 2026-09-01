# domain-crash-course · 陌生领域入门（陌懂懂）

**当前版本：V1.0（2026-09-01）**

一个 Agent Skill：帮助办公人群在会议、客户拜访、面试前快速入门陌生领域——从「完全不懂」到「听得懂、能参与、问得出问题」。

结合知乎开放平台的专业内容、高赞回答与热榜趋势，提供普通百科给不了的三样东西：**行业内部人士的人话解释、业内正在争论的议题、行业的黑话语境**。

## 能力一览

- **领域地图**：一句话解释 + 核心三问（解决什么问题 / 谁在用 / 怎么运转）+ 极简产业角色图
- **核心概念**：8–12 个开会必听概念，配人话解释、重要性、实例、易混淆辨析
- **行业议题**：3–5 个业内正在争论的核心议题（观点 A/B + 主流共识 + 知乎专业观点附链接）
- **行业黑话**：5–10 个高频行话，说明使用语境而不只是翻译
- **会议参谋**：必知 5 件事、可主动问的 3–5 个问题、对方可能提的问题、外行易犯错误
- **三级输出**：1 分钟最后一分钟复习 / 5 分钟会前一页纸 / 20–30 分钟完整速成包
- **交付物**：默认 MD + HTML 呈现；按需追加会前一页纸（A4 竖版 PDF）与核心概念提示卡（A4 横版 PNG，大字极简、手机横屏可读）

## 使用示例

- 明天要跟客户聊 AI Agent，但我完全不了解，帮我快速补课。
- 下午要参加新能源汽车出海讨论，我只有 30 分钟准备。
- 我要面试一家机器人公司，帮我快速建立行业认知。

## 安装

### WorkBuddy

把本仓库拖进 WorkBuddy 对话框，说「安装这个 skill」；或手动将 `SKILL.md` 所在目录放入 `~/.workbuddy/skills/domain-crash-course/`。

### 其他 Agent 宿主

按宿主的 skill 安装规范放置 `SKILL.md` 即可（标准 skill frontmatter 格式）。

## 知乎能力（可选但强烈建议）

本 skill 的「行业议题探测」和「趋势雷达」依赖知乎官方 zhihu skill：

1. 下载官方 skill 包：<https://developer-cdn.zhihu.com/zhihu-cli/releases/stable/skill/zhihu-cli-skill.zip>
2. 按包内 `SKILL.md` 指引完成 CLI 安装（自动下载，无需 sudo）
3. 到 <https://developer.zhihu.com/profile> 登录并申请 Access Secret，按提示配置一次即可（存本机钥匙串）

**未配置时 skill 仍可运行**：自动降级为通用网络检索，仅缺失知乎专业观点与热榜趋势。

## 双形态同步维护（维护者须知）

本仓库与 WorkBuddy 专家「陌懂懂」（`domain-crash-course`，位于 `~/.workbuddy/plugins/marketplaces/my-experts/plugins/domain-crash-course/`）是同一能力的两种形态：

- **SKILL.md 正文** ↔ 专家包 `agents/domain-crash-course.md` 正文：内容保持逐段一致
- 差异仅在 frontmatter（skill 用标准 `name`/`description`；专家用 WorkBuddy 展示字段）和宿主相关表述
- 升级流程：改 SKILL.md → 同步专家 MD → 专家包 `plugin.json` 版本号升号 → validate → register → package → 本仓库 commit & push
- 红线：专家包 `name`/`agentName`/目录名/MD 文件名不可改

## License

MIT
