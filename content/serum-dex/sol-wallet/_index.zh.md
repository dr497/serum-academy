---
date: 2020-08-27T00:0:00+00:00
title: SOL钱包
weight: 1
---

## 创建您的SOL钱包和入金

Serum是建基于 [Solana公链](https://solana.com), 需要在Serum上交易的话，第一步是创建一个SOL钱包。我们建议使用 [Sollet.io](https://sollet.io)。

如果您是首次进入 [Sollet.io](https://sollet.io) 页面时就能创建新钱包。 创建新钱包时，您会获得seed words。请注意，务必将seed words保存在一个安全不会遗失的地方，它只会出现在首次创建钱包的时候，找回密码亦需要seed words验证。

![creat-wallet](/images/articles/serum-dex/sol-wallet/create-new-wallet.png?classes=shadow&width=25pc)

您将seed words保存在一个安全的地方后，您可以为您的 [Sollet.io](https://sollet.io) 钱包配置一组密码。虽然密码不是必需的，但因为安全理由，我们还是议您使用密码。

![password](/images/articles/serum-dex/sol-wallet/password.png?classes=shadow&width=25pc)

不论您是否设定了密码，您已经成功创建了您的SOL钱包。下一步就是将SOL转入到您创建的钱包中。SOL可以在 [币安](https://binance.com)、 [FTX](https://ftx.com) 或 [OKEx](https://okex.com)等交易所买到。

![balance](/images/articles/serum-dex/sol-wallet/balance.png?classes=shadow&width=50pc)

我们现在转一些SOL通证到刚创建的钱包。点击 **接收（Receive）** 后会出现弹窗，上面有您专属的SOL地址。您可以从交易所转入SOL通证到这地址。**该地址仅能接受SOL通证，请不要将其他SPL制式通证（例如SRM）转入到该地址**

![deposit-sol](/images/articles/serum-dex/sol-wallet/deposit-sol.png?classes=shadow&width=50pc)

您也可以充值ETH然后将它**CONVERT（转换）**成SOL。您仅需点击ETH，然后连接您的**Metamask**钱包即可。

![deposit-sol-eth](/images/articles/serum-dex/sol-wallet/deposit-sol-eth.png?classes=shadow&width=30pc)

成功将SOL通证转入钱包后，您可以在钱包创建其他SPL制式通证地址。点击页面右上角的 **+** 图示后会出现个弹窗，在弹窗内您可以选择添加主要通证（Popular Tokens）例如: **SRM**, **MSRM**, **FTT**, **BTC**, **ETH**, **LINK** **XRP**, **USDT** 。成功添加以后有以下几种方式入金：
- 您可以使用[Sollet.io](https://sollet.io)以及**Metamask**来**直接存入ERC20通证**然后将他们**CONVERT（转换）**为SPL版本通证（以下会做详细介绍）。

- 您也可以将不同链上通证（ERC20、XRP、BTC等）直接存入 [FTX](https://ftx.com)，然后再将它们提取到[Sollet.io](https://sollet.io)钱包。FTX会自动将这些通证转化为SPL制式通证。
当您需要把这些SPL制式通证转化回原生通证仅需将他们提取到FTX地址即可。

![add-token-popular](/images/articles/serum-dex/sol-wallet/add-token-popular.png?classes=shadow&width=25pc)

以下您能看到您的SOL通证地址和SRM通证地址。您可以使用这些地址来存入资金到您的 [Sollet.io](https://sollet.io) 钱包，或提取款项。

![srm-balance](/images/articles/serum-dex/sol-wallet/srm-balance.png?classes=shadow&width=50pc)

如果您想要添加其他通证到钱包，您也可以手动添加，只需要输入该通证的 **铸币地址（Mint Address）** 即可。

![add-token-manual](/images/articles/serum-dex/sol-wallet/add-token-manual.png?classes=shadow&width=25pc).

### 将ERC20转换成SPL制式通证

Sollet.io允许您使用**MetaMask Wallet**进行ERC20与SPL制式的互相转换。

选择您希望存入的通证，然后选择**ERC20**。

![erc20 tab](/images/articles/serum-dex/sol-wallet/deposit-erc20.png?classes=shadow&width=25pc).

现在点击 **CONNECT TO METAMASK（连接Metamask）**，然后在**MetaMask**弹窗中点击**Confirm（确认）**。

当您的钱包连接成功以后请输入您想要转换的**ERC20**通证的数量然后点击**CONVERT（转换）**。然后请确认**MetaMask**的弹窗并选择您想要支付的Gas：

![metamask popup](/images/articles/serum-dex/sol-wallet/metamask-popups.png?classes=shadow&width=25pc).

然后请等待这笔转账在链上确认。

![confirmation](/images/articles/serum-dex/sol-wallet/erc20-confirm.png?classes=shadow&width=25pc).

转账确认以后，这些通证将会在您钱包中出现。
现在您已经成功入金到[Sollet.io](https://sollet.io)钱包。可以开始在Serum上交易了！

{{% notice 小贴士 %}}
您可以使用**convert（转换）**功能来入金ETH和ERC20通证到[Sollet.io](https://sollet.io)。 
{{% /notice %}}

{{% notice 警告 %}}
通证地址（Token Address）或 **铸币地址（Mint Address）** 是通证的 **合约地址** ，可以理解为通证的 **识别码，请不要发送入金到这个地址**
{{% /notice %}}

{{% notice 警告 %}}
**入金地址（Deposit Address）** 用来存入通证的地址。
{{% /notice %}}
