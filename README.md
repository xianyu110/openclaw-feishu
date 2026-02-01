# Clawdbot安装教程：从零开始到接入飞书

这几天，Clawdbot把整个科技圈都刷屏了。

就是这个胖逼小龙虾🦞。

![图片](https://upload.maynor1024.live/file/1769832788875_image_1.jpg)

不过现在改名叫Moltbot了。

原因很简单：被Anthropic告了。

![图片](https://upload.maynor1024.live/file/1769832795345_image_2.jpg)

Anthropic觉得Clawdbot这名字太像Claude Code的延伸产品，要求改名。

真的，Anthropic你这家伙...

更离谱的是，因为Clawdbot太火，Mac Mini都被抢断货了。

![图片](https://upload.maynor1024.live/file/1769832796939_image_3.jpg)

无数人为了用它，疯狂买Mac Mini。

![图片](https://upload.maynor1024.live/file/1769832802216_image_4.jpg)

我刚打开美团外卖，发现居然没货了？？？

![图片](https://upload.maynor1024.live/file/1769832807014_image_5.jpg)

---

## 为什么这么多人买Mac Mini？

Clawdbot是个本地AI助手，权限极高，主动性极强。

它能：
- 直接改你本地文件
- 帮你炒股
- 处理邮件
- 干一切你让它干的事

官方定义：一个"在你自己设备上运行的个人AI助理"。

![图片](https://upload.maynor1024.live/file/1769832812619_image_6.jpg)

看着跟Claude Code有点像，但Claude Code因为名字，大家更把它当编程工具。

Clawdbot就没这个顾虑，定位更通用。

**但是！**

因为它是本地运行，权限极高，主动性又强，所以风险很大。

你随口一句话，它可能：
- 发个社死的朋友圈
- 把你文件删了
- 把你钱花完了

比如我今天在朋友圈看到的案例：

![图片](https://upload.maynor1024.live/file/1769832823143_image_7.jpg)

这风险，绝大多数人承受不起。

所以大家选择两种做法：
1. 买台新电脑专门跑Clawdbot
2. 上云服务或虚拟机部署

后一种对大多数人来说太复杂了。

腾讯云倒是反应快，直接提供了一键服务：

![图片](https://upload.maynor1024.live/file/1769832824537_image_8.jpg)

这时候，买台Mac Mini反而成了最简单的做法。

省心省力，还省电。

就是，得爆几千块钱...

不是一般人玩得起的。

**我的建议**：

如果你真的不在乎风险，或者就想在自己电脑上试试，完全没必要买Mac Mini。

一台很多年前的二手老电脑都能跑。

完全没必要给苹果交税。

我真觉得，Mac Mini这波热度有点不正常...

---

## Clawdbot vs Claude Code

Clawdbot大部分能力跟Claude Code一样，但有几个区别：

**1. 能接入聊天软件**

可以接入WhatsApp、Telegram、Discord。

国内有人把飞书接进去了，QQ方案我们也在试。

也就是说，你出门在外，给聊天软件发条消息，它就能在你本地电脑上操作。

用普通聊天软件当入口，太丝滑了。

**2. 有长期记忆**

记忆存在本地文件里，跟ChatGPT体验类似。

日常对话中，能用记忆搜索把相关内容捞回上下文。

跨会话积累更可控，也更容易理解和改造。

**3. 开源，能折腾**

能自己部署，背后能随便接自己喜欢的模型。

跟OpenCode有点像，也支持Skills。

再结合天时地利人和，还有大家对AI的焦虑。

于是，Clawdbot爆了。

Github上已经6万3的Star了，增长曲线极其离谱。

![图片](https://upload.maynor1024.live/file/1769832832765_image_9.jpg)

---

## 开始安装

部署这玩意，说简单也简单，说麻烦也麻烦。

Mac部署和Windows部署完全不是一个难度级别。

我这里教大家怎么装，以及如何接入飞书，让我们在国内也能玩起来。

**⚠️ 严重声明**：

这是我在公司放的测试笔记本。

**一定注意安全问题！**

**如无必要，不要在主力机安装！**

**一定要用备用机！**

这玩意权限很高，一定要悠着点。

如果你直接在主力机上跑，万一AI抽风执行个 `rm -rf /`，你电脑里的那点隐私和学习资料可全完了。

千万别到时候重要文件被删了然后来骂我...

---

## 第一步：安装Clawdbot

一行命令就行，很简单。

下面的命令适用于Mac、Windows和Linux。

我这里选择Windows进行部署测试。

```bash
# Windows安装
iwr -useb https://molt.bot/install.ps1 | iex

# macOS / Linux / Ubuntu / Debian安装
curl -fsSL https://molt.bot/install.sh | bash -s -- --install-method git
```

**注意**：运行前要先装Node.js，得22版本以上，否则会报错。

然后你就能看到它开始安装了。

![图片](https://upload.maynor1024.live/file/1769832836143_image_10.jpg)

安装好后，会出现这个：

![图片](https://upload.maynor1024.live/file/1769832834511_image_11.jpg)

问你选yes还是no。

意思就是：我懂这大龙虾能力很强但风险极大，你确认继续吗？

只有选yes，才让你进行下一步。

选No，直接把进程关了。

也是非常的霸王条款...

![图片](https://upload.maynor1024.live/file/1769832838252_image_12.jpg)

选yes后，会看到一个选项：

![图片](https://upload.maynor1024.live/file/1769832843331_image_13.jpg)

第一个是快速启动，后续通过 `clawdbot configure` 配置信息。

第二个是先手动配置。

我们选第一个。

---

## 第二步：配置模型

然后它会让你配置模型。

![图片](https://upload.maynor1024.live/file/1769832846889_image_14.jpg)

我是ChatGPT Pro会员，可以直接用Codex OAuth。

也就是把Codex的额度挂过来，跟OpenCode玩法一样。

OpenAI自己很支持这种做法，所以几乎没风险。

**⚠️ 注意**：千万别用Claude Max的额度！

Anthropic现在只准那个额度在Claude Code上用。

用Clawdbot授权可能直接被封号，X上已经有好多案例了。

你也可以选国产模型，比如MiniMax、Qwen、智谱。

**💡 推荐：使用第三方API中转服务**

如果你不想用官方API（需要魔法、价格贵、支付麻烦），可以用第三方API中转。

推荐：**https://apipro.maynor1024.live/**
