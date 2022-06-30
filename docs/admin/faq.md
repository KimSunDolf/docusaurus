---
title: 常见问题 - CODING 帮助中心
pageTitle: 常见问题
pagePrevTitle: 访问审计
pagePrev: admin/access-audit.html
pageNextTitle: 水印设置
pageNext: admin/watermark.html
---

### [如何锁定 / 解锁成员？](#how-to-lock)

此操作会禁止成员访问团队资源与登录团队。

点击团队首页右上角的齿轮图标 <img src ="https://help-assets.codehub.cn/enterprise/20210928153255.png" style ="margin:0"> 进入团队设置中心，前往「全局设置」->「组织与成员」->「成员管理」中的团队成员列表，选择需要锁定的用户，点击右侧的 `···` 按钮并选择「锁定成员」。被锁定的用户会有锁定标记，如需解锁，执行「解除成员」操作即可。

![](https://help-assets.codehub.cn/enterprise/20210719170609.png)

### [账号被锁的原因及解决办法是什么？](#why-blocked)

如果被锁定的是**团队负责人**，那么需前往[工单中心](https://e.coding.net/signin?redirect=/workorder)提交解锁申请。

如果被锁定的是**团队成员**，以下是可能的原因以及解锁办法。

1.  登录团队时连续 5 次输入密码错误。

    请联系团队负责人 / 管理员，在“设置中心” > “成员管理”中进行解锁。

2.  被锁成员的账号类型为腾讯云子账号，缺乏 `QcloudCODINGFullAccess` 角色权限。

    请联系主账号所有者，前往[访问管理](https://console.cloud.tencent.com/cam)进行角色策略授权。

![](https://help-assets.codehub.cn/enterprise/20220318110207.png)

3.  由企业微信导入至 CODING 的成员，因退出企业微信组织或被移除而导致锁定。

    团队负责人 / 管理员可以参考[此文档](https://help.coding.net/docs/admin/member/wecom.html#sync)调整成员自动同步机制。

### [如何退出团队？](#exit-team)

> 团队负责人不能退出团队。

团队成员点击右上角头像下拉框的「个人账户设置」→「个人账户」即可看到退出团队选项。

![](https://help-assets.codehub.cn/enterprise/20211203152557.png)

若团队成员由企业微信导入，点击[了解](/docs/admin/member/wecom.html#sync)如何实现在成员离职时自动解除与 CODING 团队关联。

### [如何注销团队？](#logout)

团队负责人点击首页右上角的齿轮图标 <img src ="https://help-assets.codehub.cn/enterprise/20210928153255.png" style ="margin:0"> 进入团队设置中心，点击「基本信息」→「注销团队」进入操作页面。

![](https://help-assets.codehub.cn/enterprise/20211203153456.png)

### [如何转让团队负责人？](#transfer-team-owner)

> 若账号已关联腾讯云账号，则不支持此功能。参考[此文档](/docs/admin/service-integration/cloud.html#unbind)进行解绑。

团队负责人可以点击首页右上角的齿轮图标 <img src ="https://help-assets.codehub.cn/enterprise/20210928153255.png" style ="margin:0"> 进入「设置中心」->「全局设置」->「基本信息」中将团队转让给相应成员。

![](https://help-assets.codehub.cn/enterprise/20210929151710.png)

### [团队成员减少后没有自动降档](#auto-downshift)

团队成员减少后，系统并不会自动调低目前高级版团队的所属档位。若确认不再需要更多档位，请[提交工单](https://e.coding.net/signin?redirect=/workorder)由客服为您调低档位。

工单信息需包括：

（1）团队名称
（2）团队域名
（3）更新后的档位数量
（4）申请原因

### [如何购买 CODING 服务？](#q1)

仅团队负责人/管理员具备团队付费权限。点击右上角头像下拉处的「服务订购」→「订购服务」，选择所需的服务类型及人数后，核实订单金额后可以直接提交订单完成支付，若账户有优惠券可在提交订单前进行选用，系统会自动减免订单金额，点击[此处](/docs/admin/pay/price.html#scenes-1)了解更多。

### [如何使用优惠券？](#q2)

在订购服务页中点击「兑换优惠券」，输入优惠券代码后即可抵扣金额。

![](https://help-assets.codehub.cn/enterprise/20211119172450.png)

### [是否能通过腾讯云账号扣款？](#q3)

团队账号关联腾讯云账号后，才能使用腾讯云账号进行扣款。团队负责人/管理员点击团队首页右上角的齿轮图标进入团队设置中心，在「第三方应用」中绑定腾讯云账号。

![](https://help-assets.codehub.cn/enterprise/20211119173901.png)

绑定完成后，点击前往[此处](https://buy.cloud.tencent.com/coding)进行服务购买。

> 需绑定腾讯云主账号。

### [如何增加/减少高级版用户人数](#q4)

请阅读[场景四：高级版增加人数](/docs/admin/pay/price.html#scenes-4)与[场景五：高级版减少人数](/docs/admin/pay/price.html#scenes-5)。

### [如何退款？](#q5)

付款后，暂不支持退款，请在确认购买所需的服务后再进行支付。若遇到下单错误等特殊情况请及时联系[官方人员](https://e.coding.net/signin?redirect=/workorder)。

### [如何查看服务到期时间？](#q6)

团队负责人/管理员点击右上角头像下拉处的「服务订购」→「订购服务」，在服务概览右侧中可以查看预估到期时间。

![](https://help-assets.codehub.cn/enterprise/20211119155804.png)

### [是否支持对公转账？](#q7)

支持。详情请阅读[此处](/docs/admin/pay/price.html#pay)。

### [如何获取发票？](#q8)

CODING 支持开具增值税普通发票与增值税专用发票两种类型发票，请阅读[此处](/docs/admin/pay/invoice.html#manage)了解如何开具不同的发票类型。

### [如何下载合同？](#q9)

请阅读[此处](/docs/admin/pay/invoice.md#contract)了解详情。

### [绑定腾讯云账号时失败怎么办？](#q10)

**问题描述：**在第三方应用中绑定腾讯云账号时提示“当前凭据无可用账号”。

![](https://help-assets.codehub.cn/enterprise/20220616162453.png)

**解决办法：**您可能之前使用过腾讯云 Serverless 或某项容器服务，而这些服务调用了 CODING 能力，从而系统自动生成了 CODING 团队并完成两者间绑定。您需要前往腾讯云[控制台](https://console.cloud.tencent.com/coding)，登录该自动创建的团队。

![](https://help-assets.codehub.cn/enterprise/20220616164309.png)

补全信息后前往“全局设置”→“第三方应用”解绑腾讯云。然后再登录自己的 CODING 团队，重新前往团队设置中心绑定腾讯云账号。
