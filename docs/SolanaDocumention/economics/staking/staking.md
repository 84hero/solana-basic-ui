# 在 Solana 上质押

*阅读前须知：所有关于 SOL 价值增加的表述均以绝对值为准。本文档未对 SOL 在任何时间点的货币价值提出建议。*

通过质押您的 SOL，你可以为网络安全作出贡献，并在此过程中[获得奖励](https://docs.solanalabs.com/implemented-proposals/staking-rewards)。

你可以通过将你的代币委托给处理交易和运行网络的验证者来进行质押。

委托质押是一种共担风险、共享收益的金融模型，它可能会为长期委托代币的持有者提供回报。这是通过将代币持有者（委托人）和他们委托的验证者之间的财务激励对齐来实现的。

委托质押是一种共同风险共同回报的财务模型，可能会为长期委托的代币持有者提供回报。这是通过使代币持有者（委托人）和他们委托的验证者之间的财务激励保持一致来实现的。

委托给验证者的质押越多，这个验证者被选中将新交易写入账本的频率就越高。验证者写入的交易越多，验证者及其委托人获得的奖励就越多。配置系统以能够处理更多交易的验证者会按比例获得更多的奖励，并且因为他们保持网络运行尽可能快速和顺畅。

验证者在运行和维护其系统时会产生成本，这部分成本以收取奖励的百分比形式转嫁给委托人，这种费用被称为*佣金*。由于验证者获得的奖励越多，委托给他们的质押就越多，他们可能会相互竞争，提供更低的佣金费率来吸引委托人。

在通过称为削减( *slashing* )的过程进行质押时，你可能会面临失去代币的风险。削减涉及因故意的恶意行为（例如创建无效交易或审查某些类型的交易或网络参与者）而移除并销毁验证者委托质押的一部分。

当一个验证者被削减时，所有委托质押给该验证者的代币持有者都会失去他们委托的一部分。虽然这意味着代币持有者会立即遭受损失，同时这也意味着验证者由于总委托量减少而损失未来的奖励。有关惩罚路线图的更多详细信息可以在[此处](https://docs.solanalabs.com/proposals/optimistic-confirmation-and-slashing#slashing-roadmap)找到。

奖励和削减机制使得验证者和代币持有者的利益一致，这有助于保持网络的安全性、稳定性和高性能。

## 我怎么质押我的SOL代币?

你可以通过将你的代币转移到支持质押的钱包来进行 SOL 质押。该钱包提供了创建质押账户和进行委托的步骤。

### 支持的钱包

许多网页和移动钱包支持 Solana 质押操作。请向你最喜欢的钱包的维护者咨询状态。

### Solana 命令行工具

- Solana 命令行工具可以与CLI生成的密钥对文件钱包、纸质钱包或连接的 Ledger Nano 一起执行所有质押操作。
[使用 Solana 命令行工具的质押命令](https://docs.solanalabs.com/cli/examples/delegate-stake).

### 创建一个质押账户

根据钱包的指示创建一个质押账户。这个账户将与用于简单发送和接收代币的账户类型不同。

### 选择一个验证者

遵循钱包的指示来选择一个验证者。您可以从下面的链接中获取有关潜在性能良好的验证者的信息。Solana 基金会不推荐任何特定的验证者。

solanabeach.io 网站由我们的验证者之一 Staking Facilities 建立和维护，它提供了一些关于整个网络的高级图形信息，以及每个验证者列表和一些最近的每个验证者的性能统计信息。

- https://solanabeach.io

要查看区块生产统计信息，请使用 Solana 命令行工具：

- `solana validators`
- `solana block-production`

Solana 团队不会就如何解释这些信息提供建议。请自行做好尽职调查。

### 委托你的质押

遵循钱包的说明，将你的质押委托给你选择的验证者。

## 质押账户详情

有关与质押账户相关的操作和权限的更多信息，请参阅
[质押账号](https://solana.com/zh/docs/economics/staking/stake-accounts)
