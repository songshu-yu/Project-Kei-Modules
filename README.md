# Project Kei Modules

Project Kei 官方可安装模块的分发仓库。模块源码和构建器仍在主仓库维护；本仓库只保存可审阅的目录、分类说明和批次 Release，不把 ZIP 二进制写入 Git 历史。

## 下载方式

1. 普通用户优先在 Project Kei 控制台的“可安装模块”中选择模块。
2. 手动下载时，进入最新的 `modules-YYYY.MM.DD` Release，在同一个发布页选择所需 ZIP。
3. 安装前由 Core 校验 Catalog 中的版本、大小和 SHA-256；不要修改 ZIP 内容或文件名。

当前目录：[`catalog/official-catalog.json`](catalog/official-catalog.json)

## 分类

- [`modules/business/`](modules/business/)：日常业务、对话和个人状态模块。
- [`modules/intelligence/`](modules/intelligence/)：每日情报及各来源采集模块。
- [`modules/voice/`](modules/voice/)：语音编排、引擎 Provider 与 Voice Pack 管理模块。
- [`modules/integrations/`](modules/integrations/)：QQ 等外部 sidecar 集成。

## 安全边界

- Release 不包含 `.env`、Token、Cookie、个人状态、缓存、模型权重、参考音频、`node_modules` 或 `vendor`。
- GPT-SoVITS 引擎和 Voice Pack 大型资产不混入普通模块批次。
- 旧的逐模块 Release 暂时保留作兼容入口；新目录只指向集中批次 Release。
