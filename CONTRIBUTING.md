# 量潮工作日志 — 贡献指南

## 目录结构

```
quanttide-journal/
├── default/company    → 法人主体日志（quanttide-journal-of-business-entity）
├── domains/           → 领域日志子仓库（git submodule）
├── README.md          → 项目定位与结构
├── AGENTS.md          → Agent 工作指南
├── CHANGELOG.md       → 版本变更记录
└── CONTRIBUTING.md    → 本文件
```

## 内容规范

- 文档用中文
- 日志记录事实：什么时间、发生了什么、结果如何；不写动机与叙事（动机归 intention，叙事归 profile）
- 领域日志内容在对应子仓库（`quanttide-journal-of-*`）内独立维护，本仓库不直接存放内容

## 提交流程

1. 在子模块内提交推送（Conventional Commits）
2. 回到父仓库更新子模块指针，提交推送
3. 新增/移除领域时同步更新 README.md 结构树
4. 变更记录写入 CHANGELOG.md
