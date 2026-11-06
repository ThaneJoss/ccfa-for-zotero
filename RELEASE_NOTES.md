CCFA 1.0.2（准备发布）：修正 PACMMOD 会议轨道误标，并包含 Workshop 缩写修复。

- 修复 `Proceedings of the ACM on Management of Data`（PACMMOD）被自动归入 SIGMOD 的问题。该系列同时包含 SIGMOD 与 PODS；仅有系列名或另填 PODS 时留空，另一来源字段明确填写 SIGMOD 时才显示 SIGMOD。
- 纳入此前已合并的 Workshop 缩写修复：`CVPRW`、`ICCVW` 及其年份、大小写、全角变体不再继承其他字段中的主会议标签。
- 保持 CCF 2026 第七版目录（37 种期刊、58 个会议）、Zotero 7.0–10.0.* 兼容范围和本地只读计算方式。

安装：版本发布后，下载 `ccfa-1.0.2.xpi` → Zotero 工具 → 插件 → 齿轮 → 从文件安装插件 → 在列表表头右键勾选 CCFA。

口径：所有年份统一使用 2026 名单；名称匹配不验证论文类型。PACMMOD 系列信息不能代替论文所属会议轨道。

验证范围：新增回归用例覆盖 PACMMOD 全称、简称、年份与全角输入，PODS/SIGMOD 区分、既有 SIGMOD 标题及元数据修改。构建回归继续检查 XPI、更新清单、校验和与版本一致性。本版本尚未进行真实 Zotero 或 Windows/macOS 实机验证；自动 CI 不生成 `zotero-smoke.json`。
