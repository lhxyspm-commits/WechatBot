# WeChatBot by Ephemeris

一个基于 Gemini API 和 `wxauto` 的微信智能聊天机器人，支持多轮对话上下文记忆与 Google 联网搜索。

A WeChat AI chatbot based on the Gemini API and `wxauto`, supporting multi-turn dialogue context memory and Google Search grounding.

---

## 特性 / Features

* **双语与多模型支持 / Dual Language & Multi-model Support**: 原生支持 Gemini 3.5 / 3.6 系列模型。 Native support for Gemini 3.5 / 3.6 series models.
* **上下文记忆 / Context Memory**: 可自由设定 1-5 轮的多轮对话历史记忆。 Flexible multi-turn conversation memory settings (1 to 5 rounds).
* **联网搜索 / Search Grounding**: 集成 Google Search 实时联网检索能力。 Integrated with Google Search for real-time grounding.
* **可视化界面 / Graphical User Interface**: 基于 `tkinter` 构建的易用 GUI，实时日志展示。 Easy-to-use GUI built with `tkinter` and real-time log displaying.

---

## 快速开始 / Quick Start

### 1. 环境要求 / Prerequisites

* Windows 操作系统 / Windows OS
* Python 3.10+
* 登录状态的微信 PC 客户端 / Logged-in WeChat PC Client

### 2. 安装依赖 / Installation

```bash
pip install pythoncom google-genai wxauto4 pillow
3. 运行程序 / Run the Application
Bash
python WeChatBot1.0_Beta.py
构建与打包 / Build & Executable
使用 PyInstaller 将项目打包为单个可执行文件：

Build into a single executable file using PyInstaller:

Bash
# 1. 生成图标文件 / Generate logo icon
python generate_logo.py

# 2. 执行打包命令 / Build exe
pyinstaller --noconfirm --onefile --windowed --add-data "logo.ico;." --icon "logo.ico" --name "WeChatBot1.0_Beta" WeChatBot1.0_Beta.py
打包完成后，二进制文件将存放在 dist/ 目录下。

The output executable will be saved in the dist/ directory upon completion.

配置说明 / Configuration Guide
API Key: 从 Google AI Studio 获取您的 API 密钥。 Obtain your API key from Google AI Studio.

监听好友 / Monitored Contacts: 输入需要自动回复的微信好友或群聊备注名称，多个名称用逗号 , 分隔（例如：Ephemeris_,文件传输助手）。 Enter contact/group display names to monitor, separated by commas.

免责声明 / Disclaimer
本软件仅供编程学习与技术研究使用。作者不对因使用本工具导致的微信账号异常或封禁承担任何责任。

This project is for educational and research purposes only. The developer takes no responsibility for any account restrictions or bans resulting from the use of this tool.
