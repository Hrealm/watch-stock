# 🚀 摸鱼看盘 VS Code 插件

一个优雅、极简的 VS Code 股票实时查看插件，让您在编码的同时轻松掌握股市动态。

> **项目地址**: [https://github.com/pbstar/watch-stock](https://github.com/pbstar/watch-stock)

## ✨ 核心功能

| 功能            | 描述                           |
| --------------- | ------------------------------ |
| 📈 **实时行情** | 状态栏实时显示股票价格和涨跌幅 |
| 🎯 **智能搜索** | 支持股票代码、中文名称搜索     |
| 🔄 **自动刷新** | 可配置刷新频率，默认 5 秒更新  |

## 🚀 快速开始

### 安装方式

#### 方法一：从 GitHub 安装（推荐）

```bash
# 克隆项目
git clone https://github.com/pbstar/watch-stock.git
cd watch-stock

# 使用VS Code打开
# 按 F5 启动调试模式
```

#### 方法二：直接下载

1. 访问 [https://github.com/pbstar/watch-stock](https://github.com/pbstar/watch-stock)
2. 点击 "Code" → "Download ZIP"
3. 解压后复制到 `.vscode/extensions/` 目录
4. 重启 VS Code

## 📋 支持的输入格式

### 📊 股票代码格式（最准确）

| 格式       | 示例       | 说明               |
| ---------- | ---------- | ------------------ |
| `shXXXXXX` | `sh600519` | 上交所股票         |
| `szXXXXXX` | `sz000001` | 深交所股票         |
| `bjXXXXXX` | `bj430047` | 北交所股票         |
| `XXXXXX`   | `600519`   | 纯数字，默认上交所 |

### 🔍 中文名称搜索

| 输入     | 示例       | 匹配结果         |
| -------- | ---------- | ---------------- |
| 完整名称 | `贵州茅台` | 贵州茅台(600519) |
| 简称     | `茅台`     | 贵州茅台(600519) |

## 🎯 使用教程

### 📥 添加股票

#### 方法一：状态栏点击

1. 点击状态栏的股票信息
2. 选择"添加股票"
3. 输入股票代码或名称

#### 方法二：命令面板

1. 按 `Ctrl+Shift+P` 打开命令面板
2. 输入 "添加股票" 并选择
3. 输入股票信息

### 📤 管理股票

#### 移除股票

1. 点击状态栏股票信息
2. 选择"移除股票"
3. 从列表中选择要移除的股票

#### 清空列表

1. 打开命令面板 (`Ctrl+Shift+P`)
2. 输入 "清空股票"
3. 确认清空操作

## ⚙️ 个性化配置

在 VS Code 设置中搜索 `watch-stock`：

| 配置项            | 类型     | 默认值       | 说明               |
| ----------------- | -------- | ------------ | ------------------ |
| `stocks`          | string[] | `["000001"]` | 股票列表           |
| `maxDisplayCount` | number   | `5`          | 状态栏最大显示数量 |
| `refreshInterval` | number   | `5000`       | 刷新间隔（毫秒）   |

### 配置示例

```json
{
  "watch-stock.stocks": ["sh600519", "sz000001", "bj430047"],
  "watch-stock.maxDisplayCount": 3,
  "watch-stock.refreshInterval": 3000
}
```

## 🛠️ 常见问题

### ❓ 股票搜索失败怎么办？

1. **检查网络连接**：确保能访问新浪股票 API
2. **确认格式**：使用标准股票代码格式
3. **重试搜索**：网络波动可能导致暂时失败

### ❓ 支持哪些股票？

- ✅ A 股：上交所、深交所、**北交所**
- ✅ 支持中文名称搜索
- ❌ 不支持港股、美股、期货

## 🌟 特色亮点

### 🔍 智能搜索

- **新浪 API**：主要数据源，支持中文搜索
- **腾讯 API**：备用数据源，提高成功率
- **多市场支持**：上交所、深交所、北交所全覆盖

### 🎯 用户体验

- **零配置**：安装即用
- **轻量级**：占用资源少
- **状态栏显示**：不干扰编码

## 📞 技术支持

### 问题反馈

- **GitHub Issues**: [提交问题](https://github.com/pbstar/watch-stock/issues)

### 调试信息

查看开发者工具控制台（`帮助 > 切换开发者工具`）获取详细日志。

## 📄 开源协议

本项目采用 [MIT 开源协议](https://github.com/pbstar/watch-stock/blob/main/LICENSE)。

---

<div align="center">
  <p><strong>💡 点击状态栏股票信息开始使用！</strong></p>
  <p><a href="https://github.com/pbstar/watch-stock">⭐ Star on GitHub</a></p>
</div>
