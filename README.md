# 🗂️ AI 文件与照片助手

这个 Streamlit 应用程序是一个智能助手，旨在帮助用户方便地管理本地文件和照片。它利用 DeepSeek AI 的工具调用能力，实现文件读写和图像批量重命名等功能。

## ✨ 主要功能

* **读取本地文本文件内容**：让 AI 帮助你快速查看指定文本文件的内容。
* **创建或修改本地文本文件**：通过 AI 指令创建新文件或更新现有文本文件。如果目标路径的父目录不存在，应用会自动创建。
* **批量按顺序重命名文件夹中的图片**：例如，将 `IMG_1234.jpg`, `DSC_0001.png` 等图片文件，统一重命名为 `我的照片-001.jpg`, `我的照片-002.jpg` 等序列化名称。目前支持 `sequential` 顺序编号规则。

## 🛠️ 技术栈

* **Python 3**
* **Streamlit**：用于构建交互式 Web 界面。
* **DeepSeek API (openai 库)**：作为 AI 驱动的核心，提供自然语言理解和工具调用能力。

## 🚀 快速开始

pip install -r requirements.txt

运行前设置你的密钥
$env:DEEPSEEK_API_KEY="sk-你的API密钥"

Bash 
streamlit run streamlit_app.py

💡 使用指南
在左侧的文本输入框中输入你的指令。例如：

“请帮我读取 /Users/YourName/Documents/notes.txt 这个文件的内容。”

“在 C:\Reports 目录下创建一个名为 daily_summary.txt 的文件，内容是 '今天的总结：项目进展顺利。'”

“请帮我批量重命名 /Users/YourName/Pictures/旅行照片 文件夹里的所有图片，以 '旅行-照片' 为基础名称，从 1 开始按顺序编号。”

AI 将会分析你的指令，并决定是否需要调用本地工具来完成任务。

如果 AI 调用工具，你将在界面上看到工具执行的实时状态和结果。

AI 会根据工具的执行结果给出最终的回复。

点击“开始新对话”按钮可以清空当前对话历史，开始一个新的任务。

欢迎通过 Pull Requests 或 Issues 贡献代码或提出建议！
