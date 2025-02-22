---
name: Breez 销售点

description: 指南开始使用 Breez POS 接受比特币支付
---

![封面](assets/cover.webp)

_此文本来自 Breez 文档网站：https://doc.breez.technology/How-to-Get-Started-with-Breez-POS.html_

## 什么是 Breez POS？

**Breez** 是一个全功能的，非托管的 Lightning 应用。让我们来详细解释一下：

- **Lightning** 是一个比特币支付网络，它将交易时间从几分钟减少到几毫秒，将交易费用从几美元降低到几美分或更少。Lightning 将比特币从数字黄金转变为数字货币，同时保留了使比特币变得伟大的所有优点。
- **非托管** 意味着 Breez 不会占有用户的资金。许多 Lightning 应用确实会占有用户的资金。它们基本上是比特币银行。使用像 Breez 这样的非托管应用，所有用户都是自己的银行。
- **全功能** 意味着 Breez 几乎自动并在后台处理所有技术操作。像通道创建、入站流动性和路由这样的事情都保持在幕后。（但 Breez 也是开源的，所以对技术进行审计感兴趣的人欢迎这样做！）

**Breez POS** 是我们销售点模式的简称。换句话说，Breez 像是为希望接受 Lightning 支付的企业和商家提供的数字收银机（除了它的“标准”模式，这更像是比特币的数字版皮夹克，以及下一代播客播放器）。现在让我们看看如何将 Breez 设置为您业务的 Lightning 收银机。

## 如何开始使用 Breez？

1. 第一步是下载应用程序。它适用于 Android 和 iOS（安装 TestFlight 并从您的设备点击链接）。
2. Breez 可以自动备份到 Google Drive、iCloud 或任何 WebDav 服务器。
   > 请注意，每个设备都运行自己的 Lightning 节点。您可以在尽可能多的设备上运行 POS 模式，但余额将保持独立。
3. 打开应用后，点击左上角的图标找到销售点模式。

## 设置 POS

1. 点击左上角的图标，然后点击销售点 > POS 设置。

### 管理员密码

在 POS 设置中，您可以选择创建一个管理员密码。管理员密码使得未经授权无法从 Breez 应用发送出站支付。销售人员只能从设备接收支付。请注意，如果您使用此选项，您可能还想防止访问 Breez 的备份，因此在这种用例中推荐使用外部 WebDav 账户（例如，Nextcloud）。

### 商品列表

商品列表是待售商品及其价格的目录。有两种方式可以将商品添加到列表中：

- 要一次输入一个商品，请点击主 POS 视图顶部附近的商品，然后点击右下角的“+”号。在这里，您可以输入单一类型商品的名称、价格（以您选择的货币等值显示）和 SKU（该类型商品的唯一内部标识符；可选）。
- 要一次性输入多个项目，请点击左上角的计算器图标，然后选择销售点 > 偏好设置 > POS 设置，接着点击项目列表右侧的三个点，然后点击从 CSV 导入。这将允许您导入一个事先准备好的包含项目名称、价格和 SKU 的 CSV 文件。
### 法定货币显示

Breez 仅发送和接收比特币，对于大多数在 Lightning 上进行的交易，这些交易往往金额较小，金额通常以 Satoshi 显示，也就是 sats（1 BTC = 100,000,000 sats）。然而，许多商家发现能够看到（并告知顾客）以当地法定货币显示的购买价值是很实用的。

在主 POS 视图中，当前显示的货币可在右侧看到（默认为 SAT）。还有一个下拉列表，可显示其他可用的货币。要在此下拉列表中添加或移除货币，请点击销售点 > 偏好设置 > 法定货币。然后只需勾选您希望在下拉菜单中显示的货币，并取消勾选您希望省略的货币。

显示的值来自于 yadio，一个受尊敬的汇率数据提供商，这些数据几乎是实时更新的。但请记住：无论当前显示的是哪种货币价值，支付本身都是以比特币进行的。

### 收取订单

要组成订单，可以从项目列表中添加项目，或者直接在键盘上输入金额。然后点击主 POS 视图顶部的收费。接下来您将看到一个 QR 码，顾客可以用他们的 Lightning 应用扫描，您可以直接从设备上的另一个应用分享，或者在必要时复制和粘贴。

扫描该码或点击分享/粘贴的发票后，顾客将在他们的 Lightning 应用中看到发票，并有选项立即支付并结算交易。

一旦您在商家设备上的 Breez 应用中看到支付已批准的动画，您可以点击打印机图标为顾客生成收据。要在 Android 中使用收据打印机，请尝试使用此驱动程序。注意，您还可以通过交易屏幕打印过去的交易。

### 销售报告

要查看您的销售日报/周报/月报（出于会计目的或其他目的），请点击左上角的图标，然后点击交易。点击报告图标显示报告，点击日历图标更改所选日期范围。

### 导出交易

要查看在 Breez 中收到的支付列表，请点击左上角的图标，然后点击交易。点击右上角的三个点，然后点击导出以 CSV 格式导出收到的支付列表。要将列表限制在特定时间段内，请点击日历图标设置日期范围。

### 打印收据

要打印销售收据，请在支付确认对话框的右上角点击打印图标。或者，点击左上角的图标，然后点击交易。找到要打印的销售，打开它，然后点击右上角的打印图标。

> 注意：使用此驱动程序在便携式 58mm/80mm 蓝牙/USB 热敏打印机上打印。

## 我想了解更多

- 想了解更多关于 Lightning 和 Breez 的信息，请查看我们的[博客](https://breez.technology/blog)。
- 如需获取更多技术提示，了解如何充分利用该应用程序并执行常见操作，请查看我们的[文档](https://breez.technology/documentation)。
- 如果您遇到困难，无法在我们的帮助文献中找到答案，您可以在[Telegram](https://t.me/breez_labs)上找到我们，或给我们发送一封[电子邮件](mailto:support@breez.technology)。
- 如果您想看看我们的粉丝和用户制作的一些展示Breez POS模式的演示视频，[这里](https://www.youtube.com/watch?v=xxxx)有一个很棒的短片，而[这里](https://www.youtube.com/watch?v=xxxx)则是一个更长、更详细的视频。