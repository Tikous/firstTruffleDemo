# FirstTruffleDemo

我的第一个Truffle智能合约演示项目，包含一个简单的信息存储合约和Web前端交互界面。

## 📋 项目概述

这是一个基于Truffle框架的以太坊智能合约项目，包含：
- **InfoContract**: 一个简单的智能合约，可以存储和获取姓名、年龄信息
- **Web前端**: 使用ethers.js和jQuery构建的交互界面

## 🏗️ 项目结构

```
firstTruffleDemo/
├── contracts/           # 智能合约源码
│   └── InfoContract.sol
├── migrations/          # 部署脚本
├── test/               # 测试文件
├── build/              # 编译后的合约文件
├── web/                # Web前端
│   ├── index.html      # 主页面
│   ├── package.json    # 前端依赖
│   └── node_modules/   # 前端依赖包
├── truffle-config.js   # Truffle配置
└── package.json        # 项目依赖
```

## 🚀 快速开始

### 1. 安装依赖

```bash
# 安装Truffle依赖
npm install

# 安装Web前端依赖
cd web
npm install
```

### 2. 启动本地区块链

```bash
# 使用Ganache CLI
ganache-cli

# 或者使用Ganache GUI
```

### 3. 编译和部署合约

```bash
# 编译合约
truffle compile

# 部署到本地网络
truffle migrate --network development
```

### 4. 启动Web界面

```bash
cd web
npx http-server -p 8000
```

然后在浏览器中访问 `http://localhost:8000`

## 📱 功能特性

### 智能合约功能
- `setInfo(string _name, uint256 _age)`: 设置姓名和年龄
- `getInfo()`: 获取存储的信息
- `sayHi()`: 返回问候语
- `Instructor` 事件: 当信息更新时触发

### Web界面功能
- 🔗 连接MetaMask钱包
- 📋 显示合约信息和账户余额
- 🎯 调用合约方法（sayHi、setInfo、getInfo）
- 📡 实时监听合约事件
- 💫 现代化UI设计

## 🛠️ 技术栈

- **智能合约**: Solidity ^0.4.22
- **开发框架**: Truffle
- **前端**: HTML5 + CSS3 + JavaScript
- **区块链交互**: ethers.js v6
- **UI库**: jQuery
- **钱包**: MetaMask

## 📖 使用说明

1. **连接钱包**: 点击"连接MetaMask"按钮
2. **测试sayHi**: 点击"调用sayHi()"测试纯函数调用
3. **设置信息**: 输入姓名和年龄，点击"设置信息"发送交易
4. **查询信息**: 点击"获取信息"查看存储的数据
5. **监听事件**: 开启事件监听来实时查看合约事件

## ⚙️ 配置说明

### MetaMask网络配置
- 网络名称: Local Testnet
- RPC URL: http://localhost:8545
- 链ID: 1337
- 货币符号: ETH

### 合约地址
部署后的合约地址会显示在迁移输出中，需要更新到 `web/index.html` 的 `contractAddress` 变量中。

## 🔧 开发说明

### 修改合约
1. 编辑 `contracts/InfoContract.sol`
2. 运行 `truffle compile`
3. 运行 `truffle migrate --reset`
4. 更新前端的合约地址和ABI

### 自定义前端
- 修改 `web/index.html` 中的样式和功能
- 合约ABI已内嵌在HTML中
- 支持事件监听和错误处理

## 📝 许可证

MIT License

## 🤝 贡献

欢迎提交Issue和Pull Request！

---

**注意**: 这是一个学习项目，请不要在主网上使用。