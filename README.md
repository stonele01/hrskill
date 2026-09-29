# HR 场景技能包

这是一个包含 **4 个独立 Skill** 的仓库。`plugin.json` 是多技能包的安装入口；每个场景的实际执行入口是其目录内的 `SKILL.md`。仓库根目录没有单独的 `SKILL.md`，因为这里不是第五个综合 Skill。

| 场景 | Skill 入口 | 什么时候用 |
| --- | --- | --- |
| 招聘评估 | [hr-resume-screening](skills/hr-resume-screening/SKILL.md) | JD 初筛、澄清用人需求、复筛、面试出题、录音分析及人工复核 |
| 绩效材料 | [hr-performance-evidence](skills/hr-performance-evidence/SKILL.md) | 整理 KPI、周任务和主管反馈的原始证据 |
| 薪酬复核 | [hr-payroll-reconciliation](skills/hr-payroll-reconciliation/SKILL.md) | 按公司已确认的规则核对工资与考勤差异 |
| 行政采购 | [hr-admin-purchase-ledger](skills/hr-admin-purchase-ledger/SKILL.md) | 整理订单、票据、收货和付款依据 |

## 开始使用

在支持 Agent Skills 的工具中，导入需要的 **整个 Skill 文件夹**，保留其中的 `references/` 和 `agents/`。导入后，在支持 `$技能名` 的客户端可以这样说：

> 用 `$hr-resume-screening` 按这份 JD 初筛虚拟简历。先列证据和待核实项，再问我哪些岗位要求需要澄清。

若目标工具不支持自动发现或 `$` 调用，就让它读取上表对应的 `SKILL.md`，并按文件里的链接按需读取 `references/`。只打开 GitHub 页面不会使 Skill 自动生效；`plugin.json` 也不代表已安装或发布到插件目录。

每个 Skill 可独立使用。招聘流程可以从已有阶段继续；录音分析需要宿主具备实际转写或读取逐字稿的能力。简历、工资和员工资料只在获得授权的范围内处理。技能本身不连接 BOSS、钉钉或发薪系统。

更具体的材料清单与用语见[使用说明与选型](使用说明与选型.md)和[另外三个技能怎么用](其他三个技能怎么用.md)。[合成验收案例](验收案例.md)可用于试跑，但不代表真实招聘或薪酬数据已完成验证。

本仓库遵循 [Agent Skills 规范](https://agentskills.io/specification) 的单技能目录结构，并按 [OpenAI 的多技能插件结构](https://developers.openai.com/plugins/build/plugins)提供根目录 `plugin.json` 与 `skills/`。
