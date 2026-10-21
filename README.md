# 链迹智寻-融合大语言模型与图推理的虚拟货币案件协同分析系统

虚拟币案件协同调查、资金追踪与证据分析系统。支持开源情报、规则资金追踪、关联主体发现、复杂交易语义分析及案件报告，各子系统保留独立入口。

## 下载

- [下载软件](https://github.com/TOBYCheN123/chainlens/releases/download/v2026.10.21.6/chainlens.zip)：Windows 10/11 x64，完整解压后运行 `01_可执行程序/chainlens链迹智寻.exe`，无需安装 Python 或 Node.js。
- [下载完整源码](https://github.com/TOBYCheN123/chainlens/releases/download/source-v2026.10.21.6/chainlens-source.zip)：包含前后端、桌面启动与构建代码、依赖说明及三个完整 SP 推理模型。完整工程位于 Release 附件；GitHub 自动生成的 Source code 归档不是完整复现包。
- [SP 模型](https://github.com/TOBYCheN123/chainlens/releases/tag/sp-model-v1)：可在软件“能力与数据源”中按需下载。软件验证固定 SHA-256 后启用；未安装时 SP 分类不可用。

## 以协同案件为核心

案件管理与案件总览统一管理协同案件；进入案件直接打开协同工作台。支持只填写名称先建案，导入情报或历史材料，后补地址及来源，启动链上分析时才要求地址。独立子系统保留工具入口。

## 情报与协同调查

独立情报文章自动汇入协同调查的情报案件库。含地址或交易引用的文章可提供链上线索；旧文章无链上线索时标为背景情报，仍可保存入案。选择“先导入情报，稍后选择地址”建案后，可在“案件线索”从已关联文章选择地址并确认网络。启动调查可多选本案文章地址，手动地址支持逐行批量导入；报告证据索引和导出附公开来源链接。正文与公开来源保留。重复关联去重，新证据会提示更新报告，保存文章不会自动发起链上或模型请求。

## 示例与使用准备

内置 Penpie、Euler Finance 两篇公开案例整理摘要，含公开来源与链上线索，可离线查看并建案；不包含预生成路径。首次启动显示使用说明。在线调查前，使用自己的 RPC、Etherscan 和 LLM 服务；RPC 需具备所用链的历史执行 trace 能力。情报采集使用本机 Edge/Chrome。桌面界面需要 Microsoft Edge WebView2 Runtime，软件包附有官方安装引导。

软件不包含个人密钥、历史案件或浏览器资料。原始转移、规则候选和语义支持关系分别展示，不将模型审核通过等同于资金归属证明。复杂流动性及市场创建的语义解释仍有已知边界。

## 源码运行

Windows x64 与 Python 3.11：解压完整源码，阅读 README，执行 `powershell -ExecutionPolicy Bypass -File scripts/setup_source.ps1`，随后运行 `.venv\Scripts\python.exe run.py --open`。已提供前端构建产物；修改前端后需 Node.js 20.19+ 重新构建。模型用于推理复现，不包含模型训练数据。
