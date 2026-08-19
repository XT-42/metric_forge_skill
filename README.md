# Metric_forge_skill

**指标规范化梳理与指标平台搭建方法论 skill** — 一份可以直接被 Claude（claude.ai / Claude Code / Claude Cowork）加载使用的技能包，把企业指标治理从"一堆散乱报表"锻造成"一套有编号、有规范、可复用的指标体系"。

内容融合了阿里巴巴 OneData、字节跳动 DataLeap、快手 OneMetric+OneService、美团指标平台、滴滴数易、盒马 DataWorks、腾讯欧拉 t-Metric、58同城/赶集集团指标白皮书等公开分享的实践方法论，抽象成一套通用的工作流程、命名规范和文档模板。

## 这个 skill 能帮你做什么

- 梳理一套企业指标体系：数据域划分、原子/派生/复合指标建模、命名与词根规范
- 制定指标分级（资产等级/维度等级/安全等级）与治理流程（谁能新增、谁审批、谁维护口径）
- 设计指标平台/中台的技术架构（元数据层、模型层、引擎层、服务层）
- 撰写规范的指标定义文档：编号体系、八字段模板、业务口径边界规则怎么写
- 落地一份指标字典 / 指标 CRUD 工具的字段设计
- 查阅八家公司的指标治理实践案例，直接复用其中可迁移的设计思路

## 目录结构

```
metric-forge/
├── SKILL.md                                    # 主文档：workflow、速查表、常见误区
├── references/
│   ├── 01-industry-case-studies.md             # 阿里/字节/快手/美团/滴滴/盒马/腾讯/58同城 八家案例
│   ├── 02-metric-classification-and-naming.md  # 指标分类、分级、命名与词根规范
│   ├── 03-governance-process-and-roles.md      # 指标治理流程与角色设计
│   ├── 04-metric-platform-architecture.md      # 指标平台技术架构参考
│   ├── 05-tool-design-checklist.md             # 指标字典/CRUD工具设计清单
│   └── 06-metric-spec-writing-guide.md         # 指标定义文档撰写指南（编号体系+八字段模板+边界规则）
└── templates/
    └── metric-dictionary-template.csv          # 可直接用的指标字典模板
```

## 怎么用

**在 Claude 中作为 skill 加载**：将本仓库打包为 `.skill` 文件（或直接使用仓库根目录），添加到 Claude 的 skills 目录。当对话中出现"帮我理一下指标体系""指标口径有点乱""怎么搭建指标平台"这类诉求时，Claude 会自动读取 `SKILL.md` 并按需查阅对应的 `references/` 文档。

**不使用 Claude，直接当参考资料读**：`references/` 下每篇文档都可以独立阅读，`01-industry-case-studies.md` 适合先读，建立整体认知；`06-metric-spec-writing-guide.md` 最适合直接照抄去写你自己的指标文档。

## 说明

`references/` 中的大厂案例整理自各公司公开的技术分享，用于启发方案设计，细节可能随时间演进，正式引用前建议核实最新情况。欢迎提 issue / PR 补充更多公司的实践或修正过时信息。

