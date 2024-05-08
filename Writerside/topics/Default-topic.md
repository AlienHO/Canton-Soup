# 使用指南

以下是如何在 Windows 和 macOS 上运行此 Vue 项目以查看图表的详细指南。指南包括环境设置、依赖项安装和运行程序的步骤。

### 一、前置准备

确保您的电脑已安装以下软件：

- [Node.js](https://nodejs.org/)：请下载并安装稳定版本。安装后，确保 `node` 和 `npm` 命令可用。

### 二、项目文件结构

项目结构已经提供，确保所有文件都保持在初始位置。

### 三、环境设置

#### 1. Windows 用户

1. **克隆或解压项目文件**：将项目文件放在一个文件夹中。
2. **打开命令提示符**：按 `Windows + R`，输入 `cmd`，然后点击 `OK`。
3. **进入项目目录**：使用 `cd` 命令进入项目文件夹。例如：

   ```bash
   cd C:\path\to\project\folder
   ```

4. **安装 Yarn（可选）**：如果您打算使用 Yarn 进行依赖管理，请执行：

   ```bash
   npm install -g yarn
   ```

5. **安装项目依赖项**：执行以下命令以安装项目依赖：

   ```bash
   yarn install  # 如果您选择使用 yarn
   ```
   或者：

   ```bash
   npm install  # 如果使用 npm
   ```

#### 2. macOS 用户

1. **打开终端**：在 `应用程序 -> 实用工具` 中找到 `终端` 并启动它。
2. **进入项目目录**：使用 `cd` 命令进入项目文件夹。例如：

   ```bash
   cd /path/to/project/folder
   ```

3. **安装 Yarn（可选）**：如果您打算使用 Yarn 进行依赖管理，请执行：

   ```bash
   npm install -g yarn
   ```

4. **安装项目依赖项**：执行以下命令以安装项目依赖：

   ```bash
   yarn install  # 如果您选择使用 yarn
   ```
   或者：

   ```bash
   npm install  # 如果使用 npm
   ```

### 四、转换数据

1. **准备数据文件**：确保 `convert_to_json.py` 中的 `path_to_your_data.csv` 路径指向正确的 CSV 文件。
2. **运行 Python 数据转换程序**：在终端或命令提示符中，进入数据目录并运行脚本：

   ```bash
   python date/convert_to_json.py
   ```

   这会生成 `public/chart_data.json` 文件。

### 五、运行项目

1. **启动开发服务器**：在终端或命令提示符中运行：

   ```bash
   yarn dev  # 使用 Yarn
   ```
   或者：

   ```bash
   npm run dev  # 使用 npm
   ```

2. **查看图表**：开发服务器会打印出一个本地地址（通常是 `http://localhost:3000` 或 `http://127.0.0.1:3000`），用浏览器打开该地址以查看图表。

### 六、项目文件说明

- **`src/App.vue`**：主要图表配置文件，负责数据的读取和图表的展示。
- **`date/convert_to_json.py`**：负责从 CSV 文件中转换数据为 JSON 格式。
- **`public/chart_data.json`**：存储由 Python 程序生成的 JSON 数据文件。

