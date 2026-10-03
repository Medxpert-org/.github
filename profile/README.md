# MedXpert · 医疗器械合规线

> 医疗器械合规 AI 工具与知识库。权属：赵兴华 / Steven Zhao·China（ORCID [0009-0001-0512-1237](https://orcid.org/0009-0001-0512-1237)）· 官网：[medxpert.cn](https://medxpert.cn)

## 本组织放什么

| 类别 | 仓库 | 说明 |
|---|---|---|
| 技能库 | [medxpert-skills](https://github.com/Medxpert-org/medxpert-skills) | 医械合规 AI 技能集（NMPA / FDA 510(k) / EU MDR / PMDA），一技能一文件夹 |
| 技能索引 | [medxpert-skill-index](https://github.com/Medxpert-org/medxpert-skill-index) | 技能目录与安装指引 |
| 理论 | [lgd-theory](https://github.com/Medxpert-org/lgd-theory) | LGD 全程治理论（与 SynomosAI 线共有的理论基座） |

## 全景脉络

MedXpert（本组织，医械合规线）× SynomosAI·LGD（AI 治理线，见 [zhaoxinghua09-cell](https://github.com/zhaoxinghua09-cell)）构成两条主线的完整矩阵；按主题检索请用 [topic:medxpert](https://github.com/topics/medxpert)。

## 权属说明

- 可执行代码按各仓 LICENSE 授权；**理论文本 / 方法论 / 规范性表述一律保留所有权利**。
- **品牌说明**：MedXpert、SynomosAI、LGD **均未申请实体注册、未申请商标注册**。
- 内容基于公开官方信息整理，不构成法规意见；关键数据以监管机构最新发布为准。
- 权属宣告真源：《LGD 对外表述规范》v1.2 §3.2（每件必带 · 整体复制 · 名称状态与分层许可以此为准）。

---

## LGD 治理线 · Core 5 入口（真源更正）

> **真源更正**：本页上表「理论」行所列 `Medxpert-org/lgd-theory` 为**组织侧历史镜像**（内容真源不在此）；LGD 理论的内容真源与权威版本在 **[`zhaoxinghua09-cell/lgd-theory`](https://github.com/zhaoxinghua09-cell/lgd-theory)**。引用与贡献请以真源为准。

LGD 治理线的理论仓、协议仓、验证仓与入口仓（Core 5）统一维护于个人号 [`zhaoxinghua09-cell`](https://github.com/zhaoxinghua09-cell)：

| 层 | 仓（`owner/repo` 全形） | 说明 |
|---|---|---|
| 理论 Theory | [`zhaoxinghua09-cell/lgd-theory`](https://github.com/zhaoxinghua09-cell/lgd-theory) | LGD 全程治理理论（与 MedXpert 线共有的理论基座）· concept DOI 10.5281/zenodo.22456647 |
| 协议 Protocol | [`zhaoxinghua09-cell/uibc-core`](https://github.com/zhaoxinghua09-cell/uibc-core) | 参考实现 + 一致性测试（代码 Apache-2.0） |
| 验证 Verification | [`zhaoxinghua09-cell/silent-failure-catalog`](https://github.com/zhaoxinghua09-cell/silent-failure-catalog) · [`zhaoxinghua09-cell/assayance`](https://github.com/zhaoxinghua09-cell/assayance) | silent-failure 目录 · 判定「一个检查是不是检查」的元方法 |
| 入口 Entry | [`zhaoxinghua09-cell/LGD`](https://github.com/zhaoxinghua09-cell/LGD) | 公开入口与贡献体系：RUN IT / BREAK IT / BUILD IT |

> 说明：MedXpert（本组织，医械合规线）× SynomosAI·LGD（AI 治理线）构成两条主线；**LGD 治理线核心仓在个人号 `zhaoxinghua09-cell`**，本组织侧 `lgd-theory` 保留为历史镜像。

### 权属宣告（照抄《LGD 对外表述规范》v1.4 §3.2）

```
© 2026 赵兴华 / Steven Zhao·China (ORCID 0009-0001-0512-1237). All rights reserved.
理论署名 (attribution) : LGD（Lifecycle Governance Doctrine / 全程治理论）— SynomosAI initiative
名称状态 (name status)  : "SynomosAI" / "MedXpert" — 未申请实体注册、未申请商标注册
                        (not a registered legal entity; no trademark registered)
生产参考部署 (production reference, self-reported) : MedXpert
                    ← 非认证、非背书、非监管认可（not a certification or endorsement）

代码许可 (code license) : 本页不涉代码；LGD 治理线代码仓（如 uibc-core）为 Apache-2.0（see repo LICENSE）
                    本页与 LGD 理论表述文本不在任何代码许可覆盖范围内
引用格式 (cite as)      : 本页无独立 DOI —— 理论真源 zhaoxinghua09-cell/lgd-theory · concept DOI 10.5281/zenodo.22456647
```
