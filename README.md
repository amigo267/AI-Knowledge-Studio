# AI Knowledge Studio —— 不用配环境、100% 跑在本地的私有知识库工具

![video_cover_obsidian](https://soure.oss-cn-hangzhou.aliyuncs.com/img/video_cover_obsidian.jpg)

> 做这个小工具的初衷很纯粹：**我实在受够了为了本地搜个笔记，还得装 Docker、配 Python 环境和折腾复杂的向量数据库了。**

- 🚀 **GitHub Releases 下载页**：[前往 Releases 下载最新版本](https://github.com/amigo267/AI-Knowledge-Studio/releases)
- 📖 **飞书完整使用说明与教程**：[查看飞书 Wiki 公开文档](https://ycnkcvfjy3lc.feishu.cn/wiki/ZeLgwN2gViuFm6khrEmc457AnIx?from=from_copylink)

---

### **一、我为什么要做这个工具？**

![界面展示](https://soure.oss-cn-hangzhou.aliyuncs.com/img/微信图片_20261104213742_4663_2.png)

作为一个重度 Markdown / Obsidian 用户，随着笔记积累到两三千篇，日常经常遇到几个让人非常抓狂的事情：

1. **找东西像大海捞针**：明明记得去年记录过一个 MySQL 调优参数或者线上故障排查命令，但搜索关键词时会跳出几十篇笔记，还要挨个点开人工翻找，非常浪费时间。
2. **私密和商业数据不敢碰公有云**：公司项目的架构图、线上接口规范、客户信息、个人的账单与私密笔记，根本不可能上传到公网的云端 AI 知识库，一旦泄密后果不堪设想。
3. **开源工具太重、门槛太高**：市面上那些开源 RAG 项目（比如 Dify、各种向量库方案），动不动就要装 Docker、拉几个 G 的镜像，动不动端口冲突、内存狂吃大几个 G，普通电脑根本跑不顺畅。
4. **自己画的架构图成了盲区**：在 Obsidian 里用 Excalidraw 画了大量的业务流程图和技术架构图，市面上的工具全部抓瞎，根本看不懂图里的拓扑和箭头走向。

   ![preview_drawer_excalidraw](https://soure.oss-cn-hangzhou.aliyuncs.com/img/preview_drawer_excalidraw.png)

为了彻底解决自己的这些刚需，我花时间写了这款独立的 Windows 原生桌面端应用——**没有套路，开箱即用，所有文档和计算全部留在你自己的电脑里。**

---

### **二、日常使用中，它能帮你做什么？**

![setting_knowledge_base](https://soure.oss-cn-hangzhou.aliyuncs.com/img/setting_knowledge_base.png)

#### **1. 像选文件夹一样简单，3 秒就能跑起来**

不用配任何数据库，不用装 Docker，也不需要懂命令行。下载解压后双击打开软件，点击「更换知识库」，直接选中你电脑里的笔记文件夹（支持 Markdown / Obsidian、Word `.docx`、Excel `.xlsx`/`.csv`、PDF、SQL、YAML、代码配置等 **18 种格式**，全面支持中文路径），几秒钟就索引完毕，马上可以开始提问。

#### **2. 回答严格基于你的笔记，句句有出处**

平时用 AI 最怕它“一本正经地胡说八道”。这个工具在底层做了严格的规则约束：**只根据你文档里写过的内容回答**。

- 文档里写的端口、配置、IP、代码，逐字原样提取，绝不擅自脑补；
- 答案后面会明确标注《xxx.md》与引用来源卡片（含相关度评分），点击就能直接预览全文或唤起本地编辑器；
- 没记载的内容会直接告诉你“知识库未记载”，不瞎编。

#### **3. 笔记改动毫秒级自动热更新，不用手动点刷新**

很多工具最烦人的地方是：刚在 Obsidian 或 Typora 里保存了一段新内容，切回 AI 提问却搜不到，还得到处找按钮去刷新索引。

本工具支持**按需自动感知**：平时完全不占 CPU、0 耗电，只要你在输入框敲回车提问，程序会在 **3 毫秒内自动感知文件夹里的最新改动并静默重载**。**随写随问，答案永远基于你的最新笔记，毫无心智负担。**

#### **4. 连 Excalidraw 架构图和流程图都能读懂**

如果你平时喜欢在笔记里画架构图、时序图（`.excalidraw` / `.excalidraw.md` 格式），它能自动提取图里的节点文本、模块名称和箭头连线逻辑。问系统怎么流转时，它不仅能回答，还能直接在界面里把矢量图展开滚轮缩放、切换表格视图，或一键跳转 Obsidian 修改。

#### **5. 免 Key 开箱体验 + 支持纯断网离线**

- **想零门槛体验**：软件默认内置免费 AI 体验通道，新手无需申请 API Key 打开即可直接提问；
- **想接常用云端模型**：一键切换 DeepSeek、阿里通义千问、智谱 GLM、硅基流动、OpenAI、Claude、Gemini 等 **14 款主流服务商**；
- **想极致私密**：原生支持 **本地 Ollama（免 Key）**。你甚至可以直接把电脑网线拔掉、关掉 Wi-Fi，在纯离线状态下检索问答，核心数据 100% 物理隔绝，任何人拿不走。

![setting_llm_api](https://soure.oss-cn-hangzhou.aliyuncs.com/img/setting_llm_api.png)

#### **6. 内置 12 套专业场景角色预设**

针对不同岗位高频需求，直接预置了对应的提示词规范与检索加权（也支持高级自定义）：

- **团队通用**：通用知识库检索、企业流程与新人带教、技术支持与交付实施；
- **研发架构**：后端与接口架构、前端与客户端工程、技术方案评审与 ADR；
- **运维数据**：SRE 运维与应急排障、数据工程与 DBA、安全合规与攻防审计；
- **设计质量**：产品设计与 PRD 规范、产品规划与竞品分析、测试工程与质量验收。

---

### **三、横向对比**

| 对比项       | 云端知识库（Notion AI / 钉钉等） | 开源自建（Dify / 向量库方案）           | **AI Knowledge Studio（本工具）**     |
| ------------ | -------------------------------- | --------------------------------------- | ------------------------------------- |
| 安装方式     | 网页登录                         | 装 Docker、配环境、拉镜像（折腾大半天） | 单文件/解压即用，无任何外部环境依赖   |
| 内容改动同步 | 需重新上传文件或手动同步         | 需重启容器或发指令重扫                  | 改完直接提问，后台毫秒级自动热更新    |
| 数据安全性   | 数据上传第三方服务器，有泄密风险 | 取决于服务器安全，维护繁琐              | 100% 物理留存在本地电脑，支持纯脱网   |
| 图文解析     | 仅支持纯文本                     | 绝大多数只支持文本                      | 独家支持 Excalidraw 画布拓扑解析      |
| 文档格式     | 偏纯笔记格式                     | 需配置重型解析插件                      | 原生支持 18 种办公、代码与画布格式    |
| 系统资源占用 | 依赖浏览器                       | 内存常驻 4G~8G+，风扇狂转               | 轻量桌面客户端，体积约 40MB，随开随关 |

---

### **四、怎么开始体验？**

#### 方式 A：通过 GitHub Releases 下载（推荐）
- 👉 前往 **[GitHub Releases 页面](https://github.com/amigo267/AI-Knowledge-Studio/releases)** 下载最新版 `Setup.exe` 安装包或 `Portable.zip` 便携版（附 SHA-256 校验文件）。

#### 方式 B：国内高速直链下载
- **Windows 标准安装版**：https://osstest.yoximi.com/soft/knowledge/AI_Knowledge_Studio_Setup_v1.0.exe
- **Windows 绿色便携版**：https://osstest.yoximi.com/soft/knowledge/LocalKnowledgeAI_v1.0_Portable.zip

软件不需要复杂的安装流程，拿到后只需两步：
1. 运行安装程序，或解压压缩包后双击里面的 `LocalKnowledgeAI.exe`（绿色运行，不写系统注册表垃圾）；
2. 界面上选择你平时的笔记或工作文件夹，输入问题，立刻开始体验（内置演示库与免费体验通道）。

![产品展示](https://soure.oss-cn-hangzhou.aliyuncs.com/img/xianyu_cover_banner.jpg)

---

### **❓ 常见问题（FAQ）**

- **Q：我的电脑配置不高，能流畅运行吗？**  
  A：完全可以！本桌面端经过深度优化，体积仅约 40MB，采用纯内存轻量检索；普通办公轻薄本甚至几年前的旧电脑都能流畅秒开。
- **Q：我的数据会上传到外部服务器吗？**  
  A：文档解析、切分与检索全部在本地电脑完成；搭配本地 Ollama 运行时更是 100% 物理脱网运行，无任何外泄风险。
- **Q：哪里可以看更详细的图文教程与 FAQ？**  
  A：请参阅公开的 **[飞书完整说明文档](https://ycnkcvfjy3lc.feishu.cn/wiki/ZeLgwN2gViuFm6khrEmc457AnIx?from=from_copylink)**。

---

*项目由个人独立持续维护，欢迎提交 Issue 交流需求或点亮 Star 支持。*
