## Portable Python for macOS
# Built with portable-python pip package compilation.(python pip)
# Note: I'm just delivering the goods here! Want a different Python version? Go ahead and roll your own!
# 使用python 的 portable-python 库编译,这里只是编译结果,如果需要其他版本的python,你也可以自己去试试!
**- 包含pip的跨架构便携式Python环境(使用`portable-python` pip库编译的成品)**
### 🎯 项目简介
这是一个专为macOS设计的便携式Python运行时环境，**内置pip包管理器**，提供预编译的二进制包，让用户无需复杂配置即可快速使用Python并安装第三方库。(使用`portable-python` pip库编译,这里只是结果,你也可以去试试)
[portable-python库 简介与使用说明](https://pypi.org/project/portable-python/)
### ✨ [`portable-python` ](https://pypi.org/project/portable-python/)编译成品 的 核心特性
- **📦 内置pip支持**：包含完整的pip包管理器，支持第三方库安装
- **🏗️ 跨架构支持**：同时提供ARM64（M1/M2芯片）和x86_64（Intel芯片）版本
- **⚡ 开箱即用**：下载解压即可运行，无需安装Xcode或Homebrew
- **🔧 便携式设计**：使用[`portable-python` pip库](https://pypi.org/project/portable-python/)编译，确保环境独立性.
### 🎯 解决的问题
- 避免了macOS系统Python版本冲突
- 简化了Python环境搭建流程
- 支持快速部署和迁移
- 提供完整的包管理能力
- 适合需要隔离Python环境的场景
### 🚀 使用场景
- **开发者**：快速搭建开发环境，避免本地配置问题
- **运维人员**：部署脚本时需要稳定的Python运行时和包管理
- **教育用途**：教学演示，学生无需复杂安装
- **CI/CD**：构建流程中的Python环境
- **应用分发**：打包Python应用，确保运行环境一致性
### 📦 使用方法
#### 基础使用
```bash
# 1. 下载对应架构的压缩包
# ARM芯片选择 portable-python-arm64(Darwin 3.*).zip
# Intel芯片选择 portable-python-x86_64(Darwin 3.*).zip
# 2. 解压到任意目录
unzip portable-python-*.zip
# 3. 运行Python
cd portable-python-*
./bin/python --version
# 4. 使用pip安装包
./bin/pip install requests
```
#### 包管理示例
```bash
# 先cd到当前portable-python目录
cd portable-python-*
# 然后安装依赖包
./bin/pip install -r requirements.txt
# 查看已安装包,同理
./bin/pip list
# 升级pip
./bin/pip install --upgrade pip
```
#### 🔧 技术细节
- **Python版本**：3.12.11
- **包管理器**：内置pip，支持第三方库安装
- **编译方式**：使用`portable-python` pip库编译，确保环境独立性
- **目标系统**：macOS (Darwin)
- **架构支持**：ARM64 + x86_64
- **发布方式**：GitHub Releases
#### 📋 项目结构
```
portable-python-*/
├── bin/
│   ├── python          # Python解释器
│   ├── pip             # pip包管理器
│   └── …               # 其他工具
├── lib/                # Python库
└── …                   # 其他文件
```
#### 🎯 优势特点
- **完全独立**：不依赖系统Python，避免版本冲突
- **包管理完整**：支持pip安装、升级、卸载第三方库
- **部署简单**：解压即用，无需配置环境变量
- **路径相对**：使用相对路径，适合移动和分发
#### ⚠️ 注意事项
- 使用相对路径`./bin/python`确保环境独立性
- 建议在应用脚本中使用绝对路径或相对路径调用Python
- pip安装的包仅限当前便携式环境使用
#### 📈 版本说明
当前版本v1.0.0包含：
- Python 3.12.11 解释器
- 完整的pip包管理器
- 基础标准库
