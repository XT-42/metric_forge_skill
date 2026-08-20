# Metric_forge_skill

**指标规范化梳理与指标平台搭建的实战工具箱** — 一份可以直接被 Claude（claude.ai / Claude Code / Claude Cowork）加载使用的技能包。不只是方法论手册，而是能直接产出交付物：HTML 交互台账、Excel、流程/框架图、可直接使用的申请向导工具。

内容融合了阿里巴巴 OneData、字节跳动 DataLeap、快手 OneMetric+OneService、美团指标平台、滴滴数易、盒马 DataWorks、腾讯欧拉 t-Metric、58同城/赶集集团指标白皮书等公开分享的实践方法论，抽象成一套通用的工作流程、命名规范、文档模板，以及三套可直接复用的自包含 HTML 工具。

## 这个 skill 能帮你做什么

**三个实战模式（核心能力）**：
1. **存量指标盘点与规范化**——把企业散落在各处的历史指标提取、去重、分类、编号，产出可搜索筛选的 HTML 交互台账（或 Excel）
2. **新增指标方法论与工具**——为企业业务域产出"以后怎么规范新增指标/维度"的方法论文档、流程框架图，以及一个带查重功能的 HTML 申请向导工具
3. **分析指标体系框架搭建**——基于历史指标为不同业务域搭建面向分析师的分析框架（北极星指标树 / AARRR漏斗 / OSM+UJM / 杜邦分解），产出自包含 HTML/SVG 框架图，自动标注"业务逻辑需要但还没有对应指标"的缺口

**方法论与规范（地基）**：
- 数据域划分、原子/派生/复合指标建模、命名与词根规范、指标分级（资产/维度/安全等级）
- 治理流程与角色设计（谁能新增、谁审批、谁维护口径）
- 指标平台/中台技术架构（元数据层、模型层、引擎层、服务层）
- 指标定义文档撰写规范：编号体系、八字段模板、业务口径边界规则怎么写
- 八家公司（阿里/字节/快手/美团/滴滴/盒马/腾讯/58同城）的指标治理实践案例拆解

## 目录结构

```
metric-forge/
├── SKILL.md                                    # 主文档：三个实战模式路由、workflow、速查表、常见误区
├── references/
│   ├── 01-industry-case-studies.md             # 阿里/字节/快手/美团/滴滴/盒马/腾讯/58同城 八家案例
│   ├── 02-metric-classification-and-naming.md  # 指标分类、分级、命名与词根规范
│   ├── 03-governance-process-and-roles.md      # 指标治理流程与角色设计
│   ├── 04-metric-platform-architecture.md      # 指标平台技术架构参考
│   ├── 05-tool-design-checklist.md             # 指标字典/CRUD工具设计清单
│   ├── 06-metric-spec-writing-guide.md         # 指标定义文档撰写指南（编号体系+八字段模板+边界规则）
│   ├── 07-audit-and-standardize-workflow.md    # 模式一：存量指标盘点与规范化工作流
│   ├── 08-metric-extension-method.md           # 模式二：新增指标方法论与工具使用指南
│   └── 09-analytical-framework-library.md      # 模式三：分析指标体系框架库（四种经典范式）
├── assets/
│   └── html-templates/
│       ├── metric-audit-table.html             # 模式一交付物：指标盘点交互台账
│       ├── metric-intake-wizard.html           # 模式二交付物：新增指标申请向导（带查重）
│       └── framework-diagram.html              # 模式三交付物：分析指标体系框架图
└── templates/
    └── metric-dictionary-template.csv          # 可直接用的指标字典模板
```

## 怎么用

**在 Claude 中作为 skill 加载**：将本仓库打包为 `.skill` 文件（或直接使用仓库根目录），添加到 Claude 的 skills 目录。当对话中出现"帮我理一下指标体系""指标口径有点乱""帮我们业务域搭个指标体系框架"这类诉求时，Claude 会自动读取 `SKILL.md`，判断落在哪个实战模式，按需查阅对应的 `references/` 文档，复制 `assets/html-templates/` 里对应的模板、填入真实数据后交付。

**直接打开 `assets/html-templates/` 里的文件体验**：三个 HTML 工具都内置了演示数据，双击用浏览器打开即可直接看到效果（无需联网、无需安装任何依赖），感受一下产出物长什么样再决定要不要用 Claude 生成你自己企业的版本。

**不使用 Claude，直接当参考资料读**：`references/` 下每篇文档都可以独立阅读，`01-industry-case-studies.md` 适合先读，建立整体认知；`06-metric-spec-writing-guide.md` 最适合直接照抄去写你自己的指标文档；07-09 是三个实战模式的操作手册。

## 说明

`references/` 中的大厂案例整理自各公司公开的技术分享，用于启发方案设计，细节可能随时间演进，正式引用前建议核实最新情况。欢迎提 issue / PR 补充更多公司的实践或修正过时信息。

## License

MIT
