# 量潮工作日志

## 仓库定位

量潮工作日志（quanttide-journal）是量潮知识管理体系中的**日志聚合容器**——按主体与领域聚合各业务的工作日志子仓库（git submodule）。每个子仓库独立维护，本仓库只追踪引用。

在量潮"正交分解"中，本仓库位于**能力轴（How it runs）**：`default/` 聚合法人主体日志，`domains/` 聚合各领域日志，回答"量潮如何运行、各领域发生了什么"。

## 仓库结构

```
quanttide-journal/
├── default/company      → 法人主体日志（quanttide-journal-of-business-entity）
├── domains/             → 领域日志子仓库（git submodule）
│   ├── agent            → 智能体工程日志（quanttide-journal-of-agent-engineering）
│   ├── alliance         → 联盟管理日志（quanttide-journal-of-alliance-management）
│   ├── auth             → 身份认证日志（quanttide-journal-of-authorization）
│   ├── business         → 商务拓展日志（quanttide-journal-of-business-development）
│   ├── code             → 软件工程日志（quanttide-journal-of-software-engineering）
│   ├── crowd            → 众包管理日志（quanttide-journal-of-crowd-sourcing）
│   ├── data             → 数据工程日志（quanttide-journal-of-data-engineering）
│   ├── design           → 交互设计日志（quanttide-journal-of-interaction-design）
│   ├── docs             → 文档工程日志（quanttide-journal-of-document-engineering）
│   ├── econ             → 经济建模日志（quanttide-journal-of-economic-modeling）
│   ├── entrep           → 创业管理日志（quanttide-journal-of-entrepreneurship-management）
│   ├── execute          → 执行管理日志（quanttide-journal-of-execution-management）
│   ├── health           → 健康管理日志（quanttide-journal-of-health-management）
│   ├── knowl            → 知识工程日志（quanttide-journal-of-knowledge-engineering）
│   ├── media            → 新媒体运营日志（quanttide-journal-of-social-media）
│   ├── product          → 产品研发日志（quanttide-journal-of-product-development）
│   ├── security         → 安全工程日志（quanttide-journal-of-security-engineering）
│   ├── strategy         → 战略管理日志（quanttide-journal-of-strategy-management）
│   └── think            → 认知工程日志（quanttide-journal-of-cognitive-engineering）
├── README.md            → 本文件
├── AGENTS.md            → Agent 工作指南
├── CHANGELOG.md         → 版本变更记录
└── LICENSE              → 许可证
```

## 子模块管理

- 子模块独立提交推送，本仓库只更新引用指针
- 新增日志仓库：`git submodule add <url> domains/<path>`
- 同步全部子模块：`git submodule update --init --recursive`

## 关联

- 日志与意图、档案同源：`assets/quanttide-profile`（工作档案聚合）、`assets/quanttide-intention`（工作意图聚合）
- 分层关系：journal（事实）→ intention（意图）→ profile（档案/叙事），更新方向单向
