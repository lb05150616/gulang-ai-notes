# 2026年Codex Usage页面怎么看？5小时额度、周额度、Credits余额和重置时间说明

最近使用Codex时，很多用户打开Usage页面后会看到好几组数字：

- 5-hour limit；
- Weekly limit；
- Credits余额；
- Reset时间；
- 有些账号还会出现Reset available或Buy an instant reset。

第一次看很容易混淆：

**5小时额度是不是只能用5小时？周额度为什么还有剩余却不能用了？Credits还有钱为什么还提示Usage Limit？Reset以后又从什么时候重新计算？**

这篇把Codex Usage页面里最容易搞混的几个概念一次说明白。

**更新时间：2026年9月。**Codex额度、Credits和Reset功能仍可能调整，具体以当前账号Settings → Usage页面显示为准。

## 一、Codex Usage页面在哪里看

目前可以进入：

**ChatGPT / Codex → Settings → Usage**

Codex App中也可以进入：

**Usage & Billing**

这里主要可以查看：

- 套餐包含的使用额度；
- 5小时使用窗口；
- 周使用限制；
- Credits余额；
- 最近使用记录；
- 当前Reset时间；
- 当前账号可用的Credits或Reset选项。

如果正在使用Codex CLI，也可以输入：

`/status`

查看当前会话相关的额度状态。

## 二、5小时额度是什么意思

首先要明确：

**5小时额度不等于“每天只能使用Codex 5个小时”。**

它更接近一个滚动的短周期使用窗口。

在这个窗口中，你运行Codex任务会持续消耗套餐包含的使用量。

真正能运行多少任务并不是固定的，因为消耗会受到：

- 使用模型；
- 项目大小；
- 上下文长度；
- 推理强度；
- 工具调用；
- 任务运行时间；

等因素影响。

所以同样一个5小时窗口：

一个用户可能完成很多简单代码修改，

另一个用户运行几个大型项目任务就可能接近限制。

## 三、周额度又是什么意思

除了5小时窗口，Codex还可能存在Weekly，也就是周使用限制。

可以简单理解成：

**5小时额度：限制短时间内的使用强度。**

**周额度：限制更长周期内的总体使用量。**

两个限制会同时存在。

所以可能出现：

**5小时窗口已经恢复，但周额度已经用完。**

这种情况下，仍然可能无法继续使用套餐内额度。

反过来也可能是：

**周额度还有很多，但当前5小时窗口已经达到限制。**

因此看到Usage Limit以后，第一件事不是只看一个百分比，而是把：

**5小时 + Weekly**

一起检查。

## 四、为什么周额度还有剩余却提示Usage Limit

这是最近比较容易遇到的问题。

例如Usage页面显示：

**Weekly还有40%**

但任务却提示：

`You've reached your usage limit`

这时有可能是：

**当前5小时窗口已经达到限制。**

所以不能理解成：

“周额度还有40%，我就一定还能继续使用。”

正确做法是打开Usage页面同时确认：

1. 5小时窗口；
2. Weekly额度；
3. Reset时间；
4. Credits余额。

到底是哪一个限制先达到上限，要以当前页面显示为准。

## 五、Credits余额和套餐额度是什么关系

Credits和5小时、周额度不是同一个东西。

正常情况下，扣费顺序是：

**先使用套餐包含的额度 → 达到套餐限制 → 再使用Credits**

也就是说：

购买Credits以后，不会一开始就跳过Plus或Pro自带的额度。

如果当前账号支持Credits，达到套餐限制后，可以继续从Credits余额中扣除相应使用量。

目前可以在：

**Settings → Usage**

或者：

**Codex App → Usage & Billing**

查看Credits余额和购买入口。

详细可以查看：

[2026年Codex Credits怎么买？Plus/Pro额度用完后的购买入口和使用规则](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-buy-usage-guide-2026.md)

## 六、为什么Credits还有余额却不能继续用

出现这种情况时，不要第一时间继续充值Credits。

先检查：

- 当前任务是否支持Credits继续使用；
- Usage页面是否已经更新；
- 当前登录的账号是否正确；
- 是否达到另一个套餐限制；
- 是否出现模型Capacity或服务异常。

尤其如果报错是：

`Selected model is at capacity`

这并不等于Credits已经用完。

Capacity更多指向模型容量或服务端问题。

可以查看：

[2026年Codex提示Selected model is at capacity怎么办？GPT-6 Astra上线后容量不足、模型切换和额度排查](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-selected-model-at-capacity-gpt6-astra-guide-2026.md)

## 七、Codex额度什么时候重置

最准确的方法不是自己计算，而是：

**直接查看Usage页面显示的Reset时间。**

因为5小时和Weekly可能分别有自己的重置时间。

所以不要简单理解成：

**“等5个小时以后，所有额度都会恢复。”**

实际上可能是：

- 5小时窗口恢复了；
- 但Weekly还没有恢复。

也可能当前页面显示的是下一次周额度重置时间。

达到限制时，Codex通常也会显示当前可以选择：

- 等待Reset；
- 使用Credits；
- 购买Credits；
- 使用可用Reset；
- 根据套餐情况升级。

## 八、为什么现在有些账号会显示Reset available

GPT-6 Astra上线后，部分符合条件的Plus、Pro和Business用户获得过一次性：

**Banked Reset**

也就是可以保存到账号中的Codex额度重置机会。

如果你的Usage页面出现：

`1 reset available`

或者：

`Full reset`

可以按照页面提示使用。

使用完整的Banked Reset以后，会刷新：

**5小时额度 + Weekly额度**

同时Weekly的下一次Reset日期也会发生变化。

需要注意：

**Banked Reset不是Credits。**

它不会给账户增加一笔可消费余额，而是直接刷新套餐的使用窗口。

是否有这个选项，以当前账号实际显示为准。

## 九、Buy an instant reset又是什么

现在部分符合条件的Plus和Pro个人账号还可能看到：

**Buy an instant reset**

它和购买Credits也不是一回事。

Instant Reset会立即恢复：

**5小时 + Weekly使用额度。**

新的Weekly周期，会从Reset完成后你第一次继续使用Work或Codex时开始计算。

下一次正常Weekly Reset通常会在这个新周期开始后的7天。

需要注意：

**Instant Reset会直接改变你的周额度周期。**

它不是额外送一份独立额度，也不能保存到以后再使用。

所以购买之前最好先看：

- 当前还剩多少额度；
- 下一次正常Reset还有多久；
- 是买Credits更合适；
- 还是直接Reset更合适。

## 十、Credits和Reset到底怎么选

可以简单判断。

### 适合等待Reset

如果：

- 项目不着急；
- 距离恢复时间很近；
- 平时额度基本够用。

直接等待最省成本。

### 适合买Credits

如果：

- 只是临时项目需要继续；
- 平时Plus或Pro额度基本够；
- 不想改变当前Weekly周期。

可以考虑Credits。

### 适合Instant Reset

如果：

- Weekly额度已经明显不够；
- 当前账号提供Reset购买入口；
- 希望直接重新开始完整额度周期。

再考虑Reset。

如果每周都频繁遇到这些问题，则更应该考虑自己的套餐是否已经长期不够用。

## 十一、Usage下降特别快怎么办

Codex使用量不是按照简单的“消息条数”计算。

以下情况通常会消耗更多：

- 大型代码仓库；
- 长上下文；
- 高推理模型；
- 长时间Agent任务；
- 多个工具调用；
- 多任务并行。

所以看到Usage下降很快，不一定是额度异常。

可以查看：

[2026年Codex额度为什么消耗这么快？Credits快速下降、Usage Limit和额度异常排查](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-usage-too-fast-guide-2026.md)

## 十二、长期额度不够需要升级Plus或Pro怎么办

如果只是偶尔碰到一次5小时或Weekly限制，没有必要马上升级套餐。

但如果已经长期出现：

- 每周频繁达到Usage Limit；
- Credits持续额外购买；
- Reset后很快再次达到限制；
- Codex已经成为日常开发主力工具；

就可以重新比较Plus和Pro。

没有合适海外付款方式、官方升级多次失败，或者希望使用本人ChatGPT账号办理Plus / Pro的用户，可以[查看Plus/Pro订阅充值入口](https://lin.aixufei.com)。

支持国内常用付款方式，使用本人ChatGPT账号办理，不提供共享账号；订单进度可以查询，内含操作教程，并提供售后质保和发票服务。

具体套餐、价格、到账时间和服务规则以下单页面实时显示为准。

## 写在最后

Codex Usage页面最重要的是区分四个概念：

**5小时额度：短周期使用限制。**

**Weekly额度：更长周期的总体使用限制。**

**Credits：套餐额度达到限制后继续使用的额外付费余额。**

**Reset：直接刷新相应的套餐使用窗口。**

所以以后看到Usage Limit，不要只问：

**“我的周额度是不是没了？”**

应该同时检查：

**5小时 → Weekly → Credits → Reset时间**

再决定是等待、买Credits、使用Reset还是升级套餐。

## ChatGPT Plus、Pro和Codex完整教程

需要继续查看ChatGPT Plus、Pro、Codex国内开通、Credits、额度、付款失败和套餐选择等问题，可以阅读：

[2026年ChatGPT Plus、Pro、Codex国内充值完整教程：支付宝微信、无海外卡、付款失败与发票](https://github.com/lb05150616/gulang-ai-notes/blob/main/chatgpt-plus-pro-codex-china-recharge-guide-2026.md)

## 相关阅读

- [2026年Codex额度为什么消耗这么快？Credits快速下降、Usage Limit和额度异常排查](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-usage-too-fast-guide-2026.md)
- [2026年Codex Credits怎么买？Plus/Pro额度用完后的购买入口和使用规则](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-buy-usage-guide-2026.md)
- [2026年Codex提示Selected model is at capacity怎么办？GPT-6 Astra上线后容量不足、模型切换和额度排查](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-selected-model-at-capacity-gpt6-astra-guide-2026.md)
- [ChatGPT Pro 100和200怎么选？Pro 5x、20x区别与Codex额度对比](https://github.com/lb05150616/gulang-ai-notes/blob/main/chatgpt-pro-5x-20x-codex-guide-2026.md)
