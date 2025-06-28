🤖 LangChain 协作型智能 Agent 项目报告
1. 🧠 Agent 功能说明
本项目构建了一个基于 LangChain 框架的多功能对话式智能 Agent，支持自然语言交互、调用知识库、本地函数处理和外部 API 查询。通过集成记忆模块，该 Agent 能够进行上下文连续的多轮对话。

背景与目标
在当前大语言模型应用中，单一问答已无法满足用户复杂任务需求。我们希望构建一个多工具协同的智能体，可辅助用户完成实际任务，如：

文档问答与知识检索

获取外部实时信息（如天气）

数据分析与处理任务

该系统适用于教育、科研、助手型产品的原型构建等场景。

2. 🛠 系统实现细节
🧱 技术栈
技术	用途
Python	编程语言
LangChain	Agent 构建框架
FAISS + OpenAI Embeddings	知识库检索系统
Gradio	Web 界面部署
OpenAI API	LLM 接入
requests	外部 API 请求
GitHub	协作开发与版本控制

🧩 Agent 使用的 Tools 简介
工具名称	类型	功能说明
文档知识库工具	知识库工具	支持对上传文档进行嵌入式问答
天气查询工具	外部 API 工具	使用 wttr.in 查询城市天气
数据分析工具	本地函数工具	简单情感分析与关键词统计处理

3. ▶️ 运行测试方法说明
环境准备
克隆仓库：

bash
复制
编辑
git clone https://github.com/yourname/langchain-agent-project.git
cd langchain-agent-project
安装依赖：

bash
复制
编辑
pip install -r requirements.txt
配置 .env 文件或设置环境变量，包含你的 OpenAI API Key：

ini
复制
编辑
OPENAI_API_KEY=your_key_here
启动 Gradio 界面
运行主程序：

bash
复制
编辑
python app.py
浏览器将自动打开一个交互页面，可开始测试 Agent。

4. 💬 聊天记录示例
📷 示例 1：天气查询
mathematica
复制
编辑
用户：请告诉我东京今天的天气
Agent：东京：🌤 +27°C
📚 示例 2：文档问答
复制
编辑
用户：根据上传的教材，解释“Transformer”的原理
Agent：Transformer 是一种基于自注意力机制的神经网络架构，主要由 Encoder 和 Decoder 组成……
📊 示例 3：数据分析
mathematica
复制
编辑
用户：请分析以下文字的情绪：“这家餐厅的服务态度非常差”
Agent：情绪分析结果：Negative
🤖 Agent 帮助用户的方式分析
知识库工具：让用户可与非结构化文档交互，如教学资料、项目文档等。

API工具：提升 Agent 对外部世界感知能力，如天气、百科等。

本地函数：强化 Agent 的逻辑推理与数据处理能力，增强可控性。

多轮记忆：实现持续、上下文相关的对话体验。

5. 👥 合作与反思
👨‍💻 成员 A：@studentA
负责内容：

LangChain Agent 主体搭建

本地函数工具开发

项目结构与 Gradio 部署

学到的内容：

如何基于 LangChain 创建 Agent

Tool 结构的定义方式

LLM 工具链系统化集成

遇到的困难：

Agent 多工具调用调度逻辑较复杂

多轮记忆与函数调用之间的协调需要调试

👩‍💻 成员 B：@studentB
负责内容：

文档知识库构建（FAISS + Embedding）

天气查询 API 接入

记忆模块实现与测试

学到的内容：

向量检索问答的流程

如何封装外部 API 供 Agent 使用

多轮对话与内存保持的机制

遇到的困难：

文档切分与检索效果优化

OpenAI Token 限制处理与请求效率问题
