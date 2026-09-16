# 2026年Codex提示Selected model is at capacity怎么办？GPT-6 Astra上线后容量不足、模型切换和额度排查

GPT-6 Astra上线后，最近不少Codex用户遇到同一个报错：

`Selected model is at capacity. Please try a different model.`

有些用户切换到GPT-5.6 Sol、Terra或Luna以后仍然出现类似提示，甚至Usage页面明明还有额度，任务依然无法继续。

这时候最容易误判成：

**“我的Codex额度是不是用完了？”**

但实际上，`at capacity`和`Usage Limit`并不是完全相同的问题。

**更新时间：2026年9月。**GPT-6 Astra仍在逐步开放，Codex容量、模型权限和额度规则可能继续调整，实际以当前账号页面和OpenAI官方状态为准。

## 一、Selected model is at capacity是什么意思

这句话可以理解为：

**当前选择的模型暂时没有足够可用服务容量，建议稍后重试或切换其他模型。**

它和下面这种提示不同：

`You've reached your usage limit`

后者更明确指向套餐额度或Usage Limit。

因此看到：

`Selected model is at capacity`

不要第一时间认为：

**Plus / Pro额度已经用完。**

最近OpenAI Codex官方GitHub中也出现多起用户报告：Usage仍有剩余，但Codex返回capacity错误，部分日志甚至显示`server_overloaded`。

## 二、为什么GPT-6 Astra上线后更容易看到这个提示

GPT-6 Astra目前正在逐步向ChatGPT和Codex用户开放。

OpenAI当前说明：

- Pro 100和Pro 200正在获得GPT-6相关能力；
- Plus会逐步获得Astra在Work和Codex中的访问权限；
- 不同账号开放时间可能不同；
- Astra的使用量消耗可能比GPT-5.6 Sol更快。

新模型上线初期，如果大量用户集中尝试复杂Codex任务，就可能出现某些时段模型容量紧张。

需要注意：

**目前公开的capacity报错主要来自用户和GitHub Issue反馈，不能简单理解成所有Codex用户都会遇到。**

## 三、先判断是容量不足还是额度用完

遇到报错后，先打开：

**Codex → Settings → Usage**

重点检查：

- 5小时窗口还剩多少；
- 周额度是否已经达到限制；
- Credits余额；
- 当前使用模型；
- Reset时间。

如果Usage仍然有明显剩余，但提示：

`Selected model is at capacity`

更应该优先考虑模型容量或服务侧异常，而不是立即购买Credits。

如果页面明确提示：

`You've reached your usage limit`

那才重点检查套餐额度。

## 四、出现capacity以后先切换模型

如果当前使用GPT-6 Astra，可以尝试切换到其他可用模型。

例如：

- GPT-5.6 Sol；
- GPT-5.6 Terra；
- GPT-5.6 Luna。

对于不需要最高推理能力的任务，可以先使用更轻量的模型继续工作。

但最近也有用户反馈：

**Astra出现capacity时，切换GPT-5.6系列仍可能遇到同类报错。**

如果多个模型连续失败，就不要无限点击Retry。

这种情况更可能不是单个模型问题。

## 五、检查Codex版本

OpenAI目前说明：

**GPT-6 Astra需要Codex CLI 0.153.0或更高版本。**

如果使用Codex CLI，可以先检查版本。

桌面端用户也建议更新到最新ChatGPT Desktop版本。

如果账号已经获得Astra权限，但本地版本过旧，可能出现模型无法正常使用或入口不一致的问题。

因此排查顺序建议是：

1. 检查Codex版本；
2. 检查Usage；
3. 切换模型；
4. 新建一个简单任务测试；
5. 再判断是不是服务容量问题。

## 六、不要因为capacity马上购买Credits

这一点很重要。

如果你的：

**Usage还有额度**

并且报错明确是：

`Selected model is at capacity`

继续购买Credits不一定能解决问题。

OpenAI目前也明确说明：

**购买Credits不会让用户在Astra逐步开放期间提前获得模型访问权限。**

Credits主要解决的是：

**套餐额度已经用完以后继续使用。**

而不是解决服务器容量不足。

Credits购买规则可以查看：

[2026年Codex Credits怎么买？Plus/Pro额度用完后的购买入口和使用规则](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-buy-usage-guide-2026.md)

## 七、为什么切换模型也没用

近期Codex官方GitHub中有用户报告：

- GPT-6 Astra出现capacity；
- GPT-5.6 Sol同样出现capacity；
- Terra和Luna也可能受到影响；
- Pro用户仍有大量Usage剩余。

这种情况下，更像是：

**Codex后端容量、请求路由或账户侧服务异常**

而不是单纯某一个模型没有额度。

这时可以：

- 暂停连续重试；
- 等待一段时间后重新尝试；
- 新建简单任务验证；
- 查看OpenAI状态页面；
- 保留Request ID和错误截图。

如果持续很长时间，再通过OpenAI Help Center反馈。

## 八、长任务中途出现capacity怎么办

这个问题对Codex开发者影响最大。

如果正在：

- 修改大型代码库；
- 执行长时间Agent任务；
- 跑测试；
- 多文件重构；

中途出现capacity，有时任务可能直接停止。

因此在模型容量不稳定期间，建议：

- 大任务拆成多个阶段；
- 重要修改及时提交Git；
- 每一步完成后保留Diff；
- 不要把几个小时工作全部放在一个超长任务中；
- 关键节点保留任务说明，方便重新继续。

这样即使模型临时不可用，也不会完全丢失之前的工作进度。

## 九、Astra为什么额度下降也比较快

除了capacity，GPT-6 Astra上线后另一个需要注意的问题是：

**额度消耗。**

OpenAI目前明确说明，Astra可能比GPT-5.6 Sol更快消耗套餐Allowance。

实际消耗取决于：

- 任务规模；
- 输入输出长度；
- 推理强度；
- Fast Mode；
- 上下文；
- 工具调用。

所以不要把：

**容量不足**

和

**额度消耗快**

混成一个问题。

额度下降太快，可以查看：

[2026年Codex额度为什么消耗这么快？Credits快速下降、Usage Limit和额度异常排查](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-usage-too-fast-guide-2026.md)

## 十、Plus和Pro遇到capacity有区别吗

Pro拥有更高Codex使用额度，但：

**更高额度并不等于服务器容量永远充足。**

近期GitHub公开Issue中，也有Pro 20x用户在Usage剩余充足的情况下遇到`Selected model is at capacity`。

所以升级Pro主要解决：

**使用量不够**

而不是保证：

**任何时间模型都不会capacity。**

如果你真正的问题是每周频繁达到Usage Limit，再考虑Pro更合理。

Plus和Pro额度区别可以查看：

[ChatGPT Pro 100和200怎么选？Pro 5x、20x区别与Codex额度对比](https://github.com/lb05150616/gulang-ai-notes/blob/main/chatgpt-pro-5x-20x-codex-guide-2026.md)
## 十一、确实需要升级Plus或Pro怎么办

如果排查后确认问题不是临时的模型Capacity，而是Codex套餐额度长期不足，可以再根据自己的实际使用强度考虑Plus或Pro。

没有合适海外付款方式、官方升级多次失败，或者希望使用本人ChatGPT账号办理Plus / Pro的用户，可以[查看Plus/Pro订阅充值入口](https://lin.aixufei.net)。

支持国内常用付款方式，使用本人ChatGPT账号办理，不提供共享账号；订单进度可以查询，内含操作教程，并提供售后质保和发票服务。

需要注意，升级套餐主要解决的是使用额度和套餐权限问题，并不能保证模型在任何时间都不会出现Capacity。具体套餐、价格、到账时间和服务规则以下单页面实时显示为准。

## 写在最后

Codex提示：

`Selected model is at capacity. Please try a different model.`

可以按照这个顺序排查：

**第一步：看Usage，确认是不是额度真的用完。**

**第二步：切换Sol、Terra或Luna测试。**

**第三步：确认Codex CLI和桌面App已经更新。**

**第四步：如果多个模型都失败，而且Usage还有大量剩余，不要继续购买Credits。**

**第五步：稍后重试，并查看OpenAI状态；持续异常再提交Request ID给官方支持。**

最重要的是区分：

**Capacity = 当前服务容量或路由可能不足。**

**Usage Limit = 套餐使用额度达到限制。**

两者处理方法并不相同。

## ChatGPT Plus、Pro和Codex完整教程

需要继续查看ChatGPT Plus、Pro、Codex国内开通、Credits、额度、付款失败和套餐选择等问题，可以阅读：

[2026年ChatGPT Plus、Pro、Codex国内充值完整教程：支付宝微信、无海外卡、付款失败与发票](https://github.com/lb05150616/gulang-ai-notes/blob/main/chatgpt-plus-pro-codex-china-recharge-guide-2026.md)

## 相关阅读
- [2026年Codex额度为什么消耗这么快？Credits快速下降、Usage Limit和额度异常排查](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-usage-too-fast-guide-2026.md)
- [2026年Codex Credits怎么买？Plus/Pro额度用完后的购买入口和使用规则](https://github.com/lb05150616/gulang-ai-notes/blob/main/codex-credits-buy-usage-guide-2026.md)
- [ChatGPT Pro 100和200怎么选？Pro 5x、20x区别与Codex额度对比](https://github.com/lb05150616/gulang-ai-notes/blob/main/chatgpt-pro-5x-20x-codex-guide-2026.md)
