# FDE Entry Coach

> 一个面向普通人的 Forward Deployed Engineer（FDE）入门与实战 Skill：从职业匹配判断开始，找到第一个真实业务问题，完成最小可用部署（MVD），并把结果沉淀为作品集。

## 这是什么

`fde-entry-coach` 不是一份“FDE 课程目录”，也不是单纯解释岗位概念的问答提示词。

它的目标是把用户从：

> “我对 FDE 感兴趣，但不知道自己能不能做。”

带到：

> “我已经完成一个真实业务部署，有真实用户、真实数据、可量化结果，并能把它讲成一份 FDE 作品集。”

整个 Skill 使用一条固定交付闭环：

`Problem → PSF → Five Maps → MVD → Activation → Metrics → Asset Extraction → Portfolio`

核心原则：**不要先学一堆工具，再寻找使用场景；先找到值得解决的真实问题，再决定 AI 怎么进去。**

---

## 适合谁

这个 Skill 主要服务四类人：

1. **Domain FDE｜行业型**  
   有银行、保险、电商、制造、医疗、人力等行业经验，但工程能力一般。重点是把行业知识转成 AI 部署能力。

2. **Engineering FDE｜工程型**  
   会写代码、做数据或 AI 系统，但缺客户发现、业务判断、落地推动和价值衡量能力。

3. **Product / Solutions FDE｜产品解决方案型**  
   产品经理、售前、咨询、Solutions Architect 等，懂需求和客户，但需要补足“亲手做出端到端系统”的能力。

4. **Internal FDE｜内部型**  
   暂时不准备转岗，或没有外部客户资源。把当前公司/团队当成第一个部署现场，先做一个真实项目。

---

## Skill 会做什么

### 1. 判断你的 FDE 入局类型

Skill 会根据：

- 当前行业与岗位
- 工作年限与业务经验
- 技术基础
- 可接触的真实场景

判断用户最适合从哪条路线进入，而不是默认所有人都走“程序员转 FDE”。

### 2. 从工作经历里挖第一个项目

Skill 不接受“做一个 AI 客服”“做一个企业 Agent”这种过大、过虚的目标。

它会把问题压缩到：

- 一个真实用户
- 一条真实流程
- 一组真实数据
- 一个可量化指标

例如：

> 不做“金融 AI Agent”，先做“把信贷客户经理每周 6 小时的企业资料整理工作压到 2 小时以内”。

### 3. 用 PSF 判断值不值得做

候选项目按三个维度各 0–5 分：

- **Pain**：痛不痛
- **Economics**：值不值钱
- **Feasibility**：做不做得出来

总分：

- `12–15`：适合做第一个 FDE 项目
- `9–11`：可以做，但需要缩小范围或解除一个关键约束
- `≤8`：先不要写代码，换问题

### 4. 建立 Five Maps

部署前至少梳理五张地图：

- Data Map：数据在哪里、谁拥有、谁信任
- Workflow Map：真实工作怎么发生
- Organization Map：谁使用、谁买单、谁支持、谁能否决
- System Map：系统、接口、权限、安全、发布约束
- Politics Map：谁受益、谁可能抵触、组织利益如何变化

个人作品集项目可以使用最小版本：一个真实用户 + 一组真实数据 + 一条真实流程 + 一个真实指标。

### 5. 设计 MVD

这里不是传统的 MVP，而是：

**MVD = Minimum Viable Deployment｜最小可用部署**

必须明确：

- User：谁会真正使用
- Workflow：替代哪条真实工作流程
- Data：用什么真实数据
- Metric：改善什么数字
- Quality：达到什么质量才可用
- Deadline：多久上线
- Graduation：什么结果继续，什么结果停止

### 6. 做 30 天实战计划

四周分别完成：

- Week 1：找对问题
- Week 2：做出 MVD
- Week 3：让真人使用
- Week 4：把项目变成职业资产

完整模板见 [`templates/30-day-plan.md`](templates/30-day-plan.md)。

### 7. 把项目变成作品集

最终不是只留一个代码仓库，而是形成：

- 一页 FDE Case Study
- GitHub README
- 3 分钟面试故事
- 可复用 Prompt / Workflow / Connector / Eval / Checklist
- 一组前后对比指标

模板见 [`templates/portfolio-case-study.md`](templates/portfolio-case-study.md)。

---

## 使用方法

把整个 `fde-entry-coach/` 文件夹放进你的 Skills 目录，并让支持 Skill 的 Agent / Coding Agent 读取 `SKILL.md`。

推荐触发方式：

- “我适合做 FDE 吗？”
- “我是银行客户经理，怎么转 FDE？”
- “帮我找一个能做成 FDE 作品集的项目。”
- “我会 Python 和 RAG，但没有客户经验，怎么补？”
- “给我做一个 30 天 FDE 入门计划。”
- “把我这个 AI 项目改造成一个 FDE Case Study。”

Skill 会一次只问一个高价值问题，不会第一轮丢出长问卷。

---

## 典型输出

完成初步诊断后，输出固定包含：

1. **你的 FDE 入局类型**
2. **最适合你的第一个 FDE 项目**
3. **PSF 评分**
4. **MVD 定义**
5. **30 天行动计划**
6. **真正需要补的 3–5 个能力**
7. **作品集应该收集的证据**
8. **一个推动项目继续前进的问题**

它不会给用户堆几十门课程，也不会把“学习 AI 工具”当成项目结果。

---

## 示例

仓库提供一个“银行信贷客户经理 → Internal / Domain FDE”的示例：

[`examples/bank-credit-example.md`](examples/bank-credit-example.md)

示例展示如何从：

> “我想做金融 AI”

缩小成：

> “企业客户资料预审与信息整理工作流”

再经过 PSF、MVD、指标、30 天计划，变成一个能进入作品集的项目。

---

## 目录结构

```text
fde-entry-coach/
├── SKILL.md
├── README.md
├── CHANGELOG.md
├── references/
│   └── fde-framework.md
├── templates/
│   ├── 30-day-plan.md
│   └── portfolio-case-study.md
└── examples/
    └── bank-credit-example.md
```

---

## 方法来源与版权说明

这个 Skill 是一套**原创的操作化职业与项目教练框架**，其中部分 FDE 方法论受到范冰（XDash）公开作品 *FDE: The Guidance Book of Forward Deployed Engineer /《前线部署工程师》* 的启发。

原始公开仓库：

https://github.com/xdash/FDE-the-Guidance-Book-of-Forward-Deployed-Engineer

本 Skill **不复制或重新发布原书正文**，而是把 FDE 的问题发现、部署、激活、指标与资产沉淀思想重构为互动式诊断和项目执行流程。

原书的版权和商业使用条件以原作者仓库中的最新说明为准。若使用原书 PDF、原文、案例或其他受版权保护内容进行商业分发、培训或付费改编，请先确认并遵守原作者的授权要求。

更多方法映射与来源说明见 [`references/fde-framework.md`](references/fde-framework.md)。

---

## 维护者

**Ryan｜硅基补全计划**

方向：AI 工作流、AI 新职业、个人与企业 AI 落地。

---

## 当前版本

`v0.1.0`

这是首个可用版本，重点完成：

- FDE 入局类型诊断
- PSF 项目筛选
- Five Maps
- MVD 设计
- 激活与指标
- 30 天行动计划
- 作品集模板
