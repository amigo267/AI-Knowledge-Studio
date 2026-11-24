## ⚡ AI Knowledge Studio v1.0.0

面向个人知识工作者、研发与运维工程师、备考学子与小微团队打造的**零配置、纯本地、轻量级 Windows AI 知识库桌面工作台**。

无需安装 Docker、无需配置 Python 环境、无需部署重型向量数据库，解压或安装即可直接绑定任意本地文件夹并开始精准问答。

---

### 📦 下载与安装说明

请从下方 **Assets** 中任选一种交付形态下载（校验值见 `SHA256SUMS.txt`）：

| 文件名 | 交付形态 | 适用人群与说明 |
| :--- | :--- | :--- |
| **`AI_Knowledge_Studio_Setup_v1.0.exe`** | Windows 标准安装包 | **推荐大众用户**：标准安装向导，自动创建桌面快捷方式与卸载入口 |
| **`LocalKnowledgeAI_v1.0_Portable.zip`** | Windows 绿色便携版 | **推荐极客 / 便携党**：解压后双击 `LocalKnowledgeAI.exe` 直接运行，免安装无残留 |

> 🚀 **国内高速镜像下载**（如 GitHub 下载较慢）：
> - 安装版：https://osstest.yoximi.com/soft/knowledge/AI_Knowledge_Studio_Setup_v1.0.exe
> - 绿色版：https://osstest.yoximi.com/soft/knowledge/LocalKnowledgeAI_v1.0_Portable.zip

---

### ✨ 核心亮点

- **零依赖极轻桌面端**：仅约 40MB，无 Docker、无外部向量数据库，采用纯内存 BM25 + 多词共现倍增与 3 行滑动窗口近邻加权检索，低配轻薄本流畅运行。
- **内置免费体验通道（免 Key 开箱即用）**：新用户打开即可直接基于内置演示库或自有文件夹提问；同时支持一键切换 DeepSeek、通义千问、智谱 GLM、OpenAI、Claude、Gemini 等 **14 款主流模型**。
- **100% 本地隐私与物理断网支持**：原生集成 **本地 Ollama（免 Key）**，拔掉网线照样秒查本地资料，数据零上传公网。
- **18 种本地格式原生解析**：支持 `.md`、`.excalidraw`、`.docx`、`.xlsx`、`.csv`、`.pdf`、`.sql`、`.yaml`、`.json`、`.py`、`.conf`、`.ini`、`.sh`、`.toml` 等格式，原样保留 Word/Excel 表格结构并支持暗黑预览。
- **独家 Excalidraw 架构图拓扑反解**：自动解析 `.excalidraw` / `.excalidraw.md` 节点与箭头流转链路，支持窗口内滚轮无极缩放、表格视图及一键联动 Obsidian 编辑。
- **3ms 笔记改动自动热更新**：闲置 0 后台轮询，外部编辑保存后提问瞬间自动感知更新。
- **12 套行业专家角色模板**：覆盖通用知识库、后端接口架构、前端工程、SRE 运维排障、数据工程 DBA、安全合规审计、产品 PRD、测试验收、企业新人带教等场景。

---

### 🚀 3 步快速上手

1. 下载上方安装包安装，或解压绿色便携版双击 `LocalKnowledgeAI.exe`；
2. 点击界面左上角「更换」，选中你的本地文档文件夹或 Obsidian 仓库（支持中文目录无乱码）；
3. 直接开始提问！回答自动标注原文出处与相关度评分，点击来源卡片即可预览全文或本地打开。
