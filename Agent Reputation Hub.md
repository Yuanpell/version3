# Agent Reputation Hub

基于 BSC 链上数据的 Agent 身份、钱包交易与 DeFi 行为分析工具。

## 功能

### Agent

- Agent ID 持有状态检查
- Agent 激活
- Agent 角色标签
- 链上打卡
- Agent 打赏
- Agent 声誉与活跃度
- Agent 榜单

### 钱包分析

输入 BSC 钱包地址后，可以查看：

- 钱包交易历史
- 交易笔数
- BNB 流入
- BNB 流出
- 钱包活跃度
- 合约交互
- 交易 Hash
- BscScan 交易入口

### Swap / 买入 / 卖出

自动识别常见交易行为：

- Swap
- 买入
- 卖出
- Token 兑换
- DEX Router 交互

### DeFi 识别

支持识别常见 DeFi 行为：

- DEX
- 流动性 / LP
- 借贷
- 存款
- 借款
- 还款
- 质押
- Vault / 收益金库
- Deposit
- Withdraw
- Claim
- Harvest
- Mint / Redeem

### DeFi 声誉与风险

根据钱包实际链上交易行为进行规则分析：

- DeFi 声誉评分
- DeFi 活跃度
- DEX 交互统计
- 流动性行为统计
- 借贷行为统计
- 质押行为统计
- Vault 行为统计
- 交互类型分析
- 风险等级
- 风险行为提示

评分和风险分析由浏览器端规则计算。

## 使用方法

### 1. 打开项目

直接打开项目页面。

### 2. 连接 BSC 钱包

点击钱包连接按钮，并切换到：

```text
BNB Smart Chain (BSC)
```

### 3. 查询 Agent

输入 Agent Wallet 地址，系统会读取对应的链上 Agent 数据。

### 4. 分析钱包

在钱包分析区域输入 BSC 钱包地址。

点击：

```text
开始分析
```

系统会读取钱包交易并进行：

```text
交易统计
    ↓
Swap 识别
    ↓
买入 / 卖出识别
    ↓
DeFi 交互识别
    ↓
活跃度分析
    ↓
声誉评分
    ↓
风险分析
```

## 交易识别

系统通过链上交易的：

- 交易目标地址
- 函数选择器
- 交易数据
- BNB 转账
- 合约交互特征

进行规则识别。

无法确定类型的交易会保留为普通合约交互或未知交互，不会虚构交易类型。

## DeFi 评分

DeFi 评分用于描述钱包的链上 DeFi 活跃程度和行为特征。

主要参考：

- DeFi 交易数量
- DEX 活跃度
- 流动性行为
- 借贷行为
- 质押行为
- Vault 行为
- 交互类型数量
- 钱包活跃情况
- 未知合约交互

评分范围：

```text
0 - 100
```

## 数据来源

项目主要读取：

- BNB Smart Chain
- BSC RPC
- Agent ID 合约
- Agent Reputation Hub 合约
- 钱包公开链上交易
- 智能合约事件
- 交易函数选择器

## 运行方式

项目采用浏览器端运行方式。

```text
浏览器
  ↓
BSC 链上数据
  ↓
前端规则分析
  ↓
交易 / DeFi / 声誉结果
```

不需要部署项目自己的本地或云端服务器。

不运行本地 AI 模型。

## 安全说明

项目不会要求用户输入：

- 私钥
- 助记词
- 钱包密码

钱包签名和交易确认由用户自己的 Web3 钱包完成。

## 项目结构

```text
.
├── contracts/
├── tests/
├── scripts/
├── artifacts/
├── 优化代码.txt
├── README.md
└── remix.config.json
```

## 技术栈

- Solidity
- JavaScript
- HTML
- CSS
- ethers.js
- BNB Smart Chain
- Web3 Wallet

## License

以项目仓库中的 LICENSE 文件为准。
