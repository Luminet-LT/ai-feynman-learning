# AI Feynman Learning

> 一套面向 AI Agent 的费曼学习法技能：先调研，再访谈锁目标；确认资料与报告后生成课程，逐章学习，并用练习、费曼输出和间隔复习验证真实掌握。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 这是什么

本仓库是一个可直接安装到 Codex 等支持 `SKILL.md` 的 AI Agent 中的技能包。它不是独立的 Web 应用，而是一套可执行的课程设计与教学协议，规定 Agent 如何：

- 在提问前完成初步调研，让访谈问题真正针对学习主题；
- 一次只问一个问题，先锁定可验收的学习目标；
- 只使用可读、可追溯的资料生成调研报告；
- 生成连续、无重复的课程大纲与级别结构；
- 按 10 模块标准编写讲义，以练习和费曼输出检验掌握；
- 根据错题、卡点与迁移表现动态调整后续课程。

核心理念：**如果你不能把它简单地解释给一个外行听，就说明你还没有真正理解它。**

## 核心能力

| 模式 | 用途 |
| --- | --- |
| 课程模式 | 从初步调研、目标访谈到逐章学习，构建完整个性化课程 |
| 考官模式 | 递进式主动回忆测验，逐题评分、诊断与追问 |
| 速查表模式 | 生成可快速扫描的一页复习材料 |
| 资源规划模式 | 筛选最高价值的学习资源 |
| 费曼深入模式 | 用讲解、举例和换条件验证真正理解一个概念 |
| 文件库模式 | 导出为 Markdown 或 Obsidian 离线知识库 |

## 课程流程

课程创建遵循固定的七阶段流程，不允许跳步：

1. **初步 AI 调研**：先了解市场上如何教，形成重点、难点假设和访谈问题。
2. **针对性访谈与目标锁定**：确认终点深度、可验收成果、周期和投入。
3. **资料收集与用户确认**：区分自动来源与用户资料，只保留有正文或有效摘要的来源。
4. **可编辑调研报告**：基于已确认资料生成，可反复修改和保存。
5. **课程大纲与结构**：按级别、章、节生成连续且可追溯的完整大纲。
6. **首章讲义**：结构确认后只生成首章，完成后即可开始学习。
7. **逐章学习**：后续章节按顺序解锁，结合测验、练习和费曼输出动态调整。

## 10 模块讲义

每节讲义都必须包含：

1. 学习导航
2. 课前检索
3. 问题情境
4. 概念建构
5. 完整示范
6. 渐隐练习
7. 变式与错误诊断
8. 提取练习
9. 费曼输出
10. 小结、迁移与复习

练习默认采用 3 道四选一单选题 + 1 道开放题；提交后由 AI 评价，并保存答案、反馈、缺口和改进建议。

## 安装

### Codex

将仓库克隆到 Codex 的用户技能目录：

```powershell
# Windows PowerShell
git clone https://github.com/Luminet-LT/ai-feynman-learning.git "$HOME\.codex\skills\feynman-learning"
```

```bash
# macOS / Linux
git clone https://github.com/Luminet-LT/ai-feynman-learning.git ~/.codex/skills/feynman-learning
```

如果技能已安装，可通过以下命令更新：

```powershell
git -C "$HOME\.codex\skills\feynman-learning" pull
```

```bash
git -C ~/.codex/skills/feynman-learning pull
```

安装后，在 Codex 中使用 `$feynman-learning` 调用该技能。若未立即出现，请重新加载或重启 Codex。

### 其他 Agent

将整个目录复制到对应 Agent 的用户技能目录，并确保 `SKILL.md` 位于技能根目录。其他平台并非原生支持 Codex 技能格式时，可将 `SKILL.md` 作为系统提示或工作流规范使用。

## 使用示例

```text
使用 $feynman-learning 帮我系统学习概率论，目标是一个月后能独立完成基础建模题。
```

```text
使用 $feynman-learning 的考官模式测验我对 Transformer 的理解，一次问一题。
```

```text
使用 $feynman-learning 为线性代数生成一页速查表，先核实关键定义。
```

```text
使用 $feynman-learning 把我的课程导出为 Obsidian 知识库。
```

## 目录结构

```text
.
├── SKILL.md                    # 技能入口与核心教学协议
├── agents/
│   └── openai.yaml             # Agent 界面元数据与默认提示词
├── assets/
│   └── course-template.md      # 课程文件模板
├── references/
│   ├── depth-spec.md           # 深度与质量规格
│   ├── levels.md               # 级别、掌握程度与评价标准
│   ├── modes.md                # 非课程模式说明
│   └── obsidian-vault.md       # 离线知识库结构
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## 设计原则

- **先诊断，后教学**：不通过“看完了”判断掌握。
- **来源可追溯**：不编造页码、链接或教材原话；未核内容明确标记。
- **一次只教一小节**：先让学习者回答，再揭晓、评价和补讲。
- **证据驱动升级**：依据作答、练习、费曼输出和迁移表现定档。
- **渐进生成**：不一次性灌完整门课，首章完成即可开始学习。
- **节约上下文但不截断关键信息**：保留学生答案、课程编号和当前章节核心来源。

## 能力边界

- 本仓库提供技能定义与工作流，不包含课程数据库、Web UI 或模型 API。
- 课程、报告、练习与反馈的持久化能力由承载 Agent 或平台提供。
- 技能要求联网调研真实来源；无法访问正文时会明确标记信息限制，而不是补造来源。
- AI 的教学反馈用于学习辅助，不替代正式教育评估、考试结论或专业建议。

## 参与贡献

欢迎提交 Issue 和 Pull Request，尤其是：

- 教学流程与质量标准的改进；
- 新的学科适配与反例；
- Agent 平台兼容性修复；
- 文档、模板和来源核验。

提交前请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。

## License

本项目采用 [MIT License](LICENSE) 开源。
