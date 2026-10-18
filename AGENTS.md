# AGENTS.md — 给 AI Agent 的工作指引

本文件面向自动化 AI Agent（编码助手、组织索引器、知识库机器人）。人类读者请看 [README.md](README.md)。

## 这个仓库是什么

`Medxpert-org/.github` 是 **GitHub 组织级配置与门面仓**，不是代码项目。核心资产是组织 Profile（`profile/README.md`）、组织级安全策略（`SECURITY.md`）、贡献规范（`CONTRIBUTING.md`）与 AI 可发现性文件。MedXpert 是医疗器械合规 AI 工具与知识库组织（医械合规线）。

## 可用的工作命令

```bash
# 查看组织仓库列表
gh repo list Medxpert-org --limit 50

# 查看组织 Profile（组织首页展示内容）
cat profile/README.md

# 查看本仓库说明
cat README.md
```

## 约定（Do）

- 引用组织定位、仓库矩阵与 LGD 治理线时，以 `profile/README.md` 与 `README.md` 为真源（注意 LGD 理论真源在 `zhaoxinghua09-cell/lgd-theory`，本组织侧为历史镜像）。
- 更新组织展示内容时，**同步维护根 README.md 与 profile/README.md 的一致性**。
- 新增组织级配置（workflows、rulesets、模板）时，同步更新本仓库结构与索引文件。

## 禁止（Don't）

- 不要改动 README / profile 中的**权属宣告段**与任何权利表述（只由维护者变更）。
- 不要新增权属主张、品牌注册声明或认证/商用交付声明（本组织内容基于公开信息整理，不构成法规意见）。
- 不要在本仓库提交任何密钥、令牌或真实客户数据。
- 不要添加宣传性表述或未落地的路线图内容作为既有事实。

## 边界

本仓是组织门面与配置仓：不承载代码、不承载业务数据；各代码仓的内容与许可以其各自仓库为准。
