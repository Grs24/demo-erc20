# 区块链培训作业

请大家 fork 本仓库后答题，做完后提交自己的软件仓库链接。

## 第 1 题：Solidity 语言有哪些数据类型？

例如：

- bool
- int8

评分标准：每个数据类型计 1 分  
参考资料： <https://docs.soliditylang.org/en/latest/types.html>

## 答

Solidity支持以下类型:

- address
- string
- fixed
- ufixed
- address payable
- function
- contract
- mapping
- enum
- struct
- bytes
- bytes1
- bytes2
- bytes3
- bytes4
- bytes5
- bytes6
- bytes7
- bytes8
- bytes9
- bytes10
- bytes11
- bytes12
- bytes13
- bytes14
- bytes15
- bytes16
- bytes17
- bytes18
- bytes19
- bytes20
- bytes21
- bytes23
- bytes24
- bytes25
- bytes26
- bytes27
- bytes28
- bytes29
- bytes30
- bytes31
- bytes32

## 第 2 题：列举并测试以太坊的 JSONRPC API

评分标准：每条有效的（提供文本命令和测试截图） API 计 2 分，例如：

---

第 1 个 API： net_version

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com \
-d '{"id":1,"jsonrpc":"2.0","method":"net_version","params":[]}' | jq
```

![1673317288973](https://user-images.githubusercontent.com/7695325/211447294-e9e142c1-0fec-4588-9c8a-7ebfbd38a907.png)

---

## 答

### 1.web3_clientVersion: 返回连接到以太坊网络的客户端的版本号

- 文本命令：

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com -d '{"id":1,"jsonrpc":"2.0","method":"web3_clientVersion","params":[]}'
```

- 测试截图: [![pSlBPzT.png](https://s1.ax1x.com/2023/01/16/pSlBPzT.png)](https://imgse.com/i/pSlBPzT)

### 2.eth_blockNumber: 返回当前区块链的高度

- 文本命令：

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com -d '{"id":1,"jsonrpc":"2.0","method":"eth_blockNumber","params":[]}'

```

- 测试截图: [![pSlBywj.png](https://s1.ax1x.com/2023/01/16/pSlBywj.png)](https://imgse.com/i/pSlBywj)

### 3.eth_getBalance: 返回给定地址的余额

- 文本命令：

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com -d '{"id":1,"jsonrpc":"2.0","method":"eth_getBalance","params":["0x742d35Cc6634C0532925a3b844Bc454e4438f44e", "latest"]}'
```

- 测试截图: [![pSlg04H.png](https://s1.ax1x.com/2023/01/16/pSlg04H.png)](https://imgse.com/i/pSlg04H)

### 4.eth_getTransactionByHash: 查询指定交易的详细信息

- 文本命令：

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com -d '{"id":1,"jsonrpc":"2.0","method":"eth_getTransactionByHash","params":["0x3FD761B0106BbE39eD0A627042Bc5B0E95622bdD", "latest"]}'
```

- 测试截图: [![pSlg04H.png](https://s1.ax1x.com/2023/01/16/pSlg04H.png)](https://imgse.com/i/pSlg04H)

### 4.eth_getTransactionCount: 返回给定地址的交易数量

- 文本命令：

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com -d '{"id":1,"jsonrpc":"2.0","method":"eth_getTransactionCount","params":["0x3FD761B0106BbE39eD0A627042Bc5B0E95622bdD", "latest"]}'
```

- 测试截图: [![pSl2eGd.png](https://s1.ax1x.com/2023/01/16/pSl2eGd.png)](https://imgse.com/i/pSl2eGd)

### 5.eth_gasPrice: 返回当前的gas价格，单位：wei

- 文本命令：

```shell
curl -s -X POST -H "Content-Type: application/json" https://matic-mumbai.chainstacklabs.com -d '{"id":1,"jsonrpc":"2.0","method":"eth_gasPrice","params":[]}'
```

- 测试截图: [![pSl2RQ1.png](https://s1.ax1x.com/2023/01/16/pSl2RQ1.png)](https://imgse.com/i/pSl2RQ1)

## 第 3 题：同一个合约里代码相同的函数，为什么 GAS 费不同？

请用 Remix 验证在同一个合约里，名称不同、代码相同的函数的 GAS 费不相等，并解释原因。

评分标准：

- 验证成功： 10 分，对过程要截图
- 解释正确： 10 分

## 答

- 验证截图：[![pSl4Jvd.png](https://s1.ax1x.com/2023/01/16/pSl4Jvd.png)](https://imgse.com/i/pSl4Jvd)
- 解释：在智能合约中，函数的 GAS 费由函数的 bytecode 大小决定。在同一个合约里，名称不同、代码相同的函数，他们的 bytecode 大小也不相等。所以他们的 GAS 费也不相等。

## 第 4 题：用 Remix 部署校验合约

用 Remix 写一个合约，部署到 mumbai 链上，计算 mumbai 链的最近平均出块时间，并校验合约代码代码。

评分标准：

- 代码正确：截图 10 分
- 部署成功：截图 10 分
- 代码校验：截图 5 分
- 获取结果：截图 5 分

- 代码截图：[![pS1XUij.png](https://s1.ax1x.com/2023/01/17/pS1XUij.png)](https://imgse.com/i/pS1XUij)

### 部署成功：截图

[![pSlO7tA.png](https://s1.ax1x.com/2023/01/16/pSlO7tA.png)](https://imgse.com/i/pSlO7tA)

## 第 5 题：黑名单 ERC20 合约

### 5.1 修复 BlacklistTokenFactory 合约里的 bug

命令 `yarn deploy:mumbai` 会在 mumbai 链上部署 BlacklistTokenFactory 和一个 BlacklistToken 合约（简称 BT1 ），地址保存在 deploy/deployed/mumbai.json 文件里（提示：删除该文件可以重新部署）。请在区块链浏览器上调用 BlacklistTokenFactory 合约里的 createBlacklistToken 函数，动态创建一个 BlacklistToken 合约（简称 BT2 ）， BT2 的地址保存在 BlacklistTokenFactory 的 blacklistTokens 数组里，也可以在交易里的 CreateBlacklistToken 事件里查看 BT2 的地址。因为目前 BlacklistTokenFactory 合约里有 bug，导致 `yarn test` 报告某些测试用例失败。请在区块链浏览器上比较 BT1 和 BT2 的功能，找出 BT2 功能异常的问题现象。并尝试修复合约 contracts/BlacklistTokenFactory.sol 的代码，能通过文件 test/BlacklistTokenFactory.test.js 里全部的自动化测试。

评分标准：

- 找到问题现象： 截图 10 分
- 解释问题原因： 10 分
- 修改合约代码： 20 分
- 自动化测试全部通过： 10 分

### 5.2 优化 BlacklistTokenFactory.test.js

参考： <https://hardhat.org/tutorial/testing-contracts> , 使用 loadFixture 重构 test/BlacklistTokenFactory.test.js 文件。

评分标准： 30 分

### 5.3 增强 BlacklistToken 合约的功能

修改本代码仓库里的 BlacklistToken 合约代码，在转账的时候抽取 10% 的手续费，并把被扣除的手续费转给合约的创建者。

评分标准：

- 代码正确： 30 分
- 部署成功： 10 分
- 代码校验： 10 分
- 手工测试： 10 分
-

### 5.4 对 BlacklistToken 合约进行自动化测试

目前 BlacklistToken 还没有写测试用例，请在 test/BlacklistToken.test.js 文件里尽量补齐。可参考 <https://hardhat.org/tutorial/testing-contracts> 和网上其它开源项目的测试用例。

评分标准：每个有效的（能执行通过）测试用例 10 分，性质相同的用例不重复计分
