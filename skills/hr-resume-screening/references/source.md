# 来源与改编说明

- 上游：Anthropic / knowledge-work-plugins。
- 固定版本：`da38ec1ee89d41e5380e652a97382695003396e7`。
- 核验日期：2026-09-27。
- [原始文件](https://github.com/anthropics/knowledge-work-plugins/blob/da38ec1ee89d41e5380e652a97382695003396e7/small-business/skills/hiring-screener/reference/rubric.md)。
- 许可：Apache-2.0，完整原始许可附于本 Skill 的 [LICENSE](../LICENSE)。本地改编不代表上游官方产品或认可。

## 复用与修改

沿用必要条件与评分项分离、0–3 分、缺失不作零、已评估权重归一化。新增中文文件清点、去重、相关年限重叠处理、缺失证据分组、重筛版本和 BOSS 不操作边界。删除国外示例、单项权重强制上限和自动后续流程。

中文入口由本任务于 2026-09-27 改编；不是原文件直译。读取本地 SKILL.md 即可执行，不依赖海外连接器或网络下载。

## 2.0 用人访谈、面试与综合评审

按用户新增流程扩展原技能；保持名称不变。检索与源码核对日期：2026-09-29。先查 skills.sh 榜单与具体条目，再读 GitHub 实际文件。没有安装新的外部 Skill，也没有因搜索而连接招聘账号。

### 现成方法选择

| 来源 | 本次核验 | 采用的部分 | 未直接套用的部分 |
|---|---|---|---|
| [Anthropic job-post-builder](https://github.com/anthropics/knowledge-work-plugins/blob/main/small-business/skills/job-post-builder/SKILL.md) | [skills.sh](https://www.skills.sh/anthropics/knowledge-work-plugins/job-post-builder) 显示约 1.5K 安装；同仓库页面约 25.7K–25.8K Star，缓存存在差异 | 用人需求访谈、岗位职责和约束、面试分工、岗位专属评分锚点 | Offer、DocuSign、国外雇佣条款不属于本次流程 |
| [Anthropic interview-prep](https://github.com/anthropics/knowledge-work-plugins/blob/main/human-resources/skills/interview-prep/SKILL.md) | [skills.sh](https://www.skills.sh/anthropics/knowledge-work-plugins/interview-prep) 显示约 3.5K 安装、仓库约 25.8K Star；已读源码 | 同岗位结构化问题、能力维度、行为与情境题、评分及复盘 | 不直接套用固定题数、通用维度或其 1–4 分制 |
| [OPM 结构化面试方法](https://www.opm.gov/policy-data-oversight/assessment-and-selection/other-assessment-methods/structured-interviews/) | 原始方法资料，非 Skill | 以岗位分析确定能力、具体工作事件、标准化问题、评分人先独立评分再讨论分歧 | 不能由方法有效性推出本地 AI 评分准确率；不套用美国职位规定 |

补充阅读：[role-intake](https://github.com/anthropics/knowledge-work-plugins/blob/main/small-business/skills/job-post-builder/reference/role-intake.md)、[interview-guide-structure](https://github.com/anthropics/knowledge-work-plugins/blob/main/small-business/skills/job-post-builder/reference/interview-guide-structure.md)。本地写成中文指引，运行时不需要抓取这些页面。

Star 是整个仓库热度，不是某项 Skill 的赞数。安装量不是招聘成功率。上述 Anthropic 方法按本包既有 Apache-2.0 许可归属保留来源；新增业务成果追问、录音全程核对、HTML 报告和人机复核规则为本地编写。

本次检索还发现不少面向求职者练习面试、UX 用户访谈和招聘系统操作的 Skill，但不能直接解决 HR 的用人需求访谈。首选复用上述两项已核验方法，没有证据声称找到一款同时覆盖公司需求澄清、整场录音分析、可视化与人工决策且经过验证的高热度完整方案。

### 心理学方法的准确表述

使用组织心理学中的岗位分析、关键事件和行为锚定思路，把抽象品质还原为工作行为。中文题库为本地适配，不是标准化心理量表，未做预测效度或评分人一致性验证。不从声音、面相或聊天风格推断心理健康、人格类型、诚信或‘文化匹配’。

### 与上游的差异

- 按用户要求保留“JD 初筛后问 HR”的顺序，初筛是暂定证据匹配；岗位规则校准后对整批一致复筛，防止先看简历再迎合候选人设标准。
- HR 提问落到公司成果、任务、实际事件、能力取舍和资源约束；每条回答映射到可检验标准。
- 简历维持 0–3 分；面试没有现成量表时也提出 0–3 分草案，确认后使用。上游有 1–4 与 1–5 两套面试示例，不直接混用。
- 面试录音先检查实际处理范围、转写质量和说话人，再用时间戳证据评分。
- 可视化分别展示简历、AI 面试和人工评价；最终综合结论保留评审人和理由，不默认自动加权或代替人做录用决定。

## 上游快照用途

[上游快照](upstream-snapshot.md)仅供维护者核对出处、比较后续改动；它是源材料，不是本地执行入口。内部未打包的上游文件链接、工具名、默认业务参数和外部写入指令不适用于本地 Skill；如要扩展功能应回到固定版本核验，不能照抄执行。
