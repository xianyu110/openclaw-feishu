## Clawdbot安装教程



这几天，相信大家肯定都被一个产品名给刷屏了。

Clawdbot。

就是这个胖逼小龙虾🦞。

![图片](https://upload.maynor1024.live/file/1769832788875_image_1.jpg)

只不过现在改名叫Moltbot了，原因很简单，被Anthropic告了。。。

![图片](https://upload.maynor1024.live/file/1769832795345_image_2.jpg)

因为Anthropic认为Clawdbot这个名字太容易被市场误解为Claude Code的延展产品，所以要求创始人改名。

真的，Anthropic你这家伙坏事做尽。。。

而因为Clawdbot的爆火，甚至导致，MacMini都被卖断货了。

![图片](https://upload.maynor1024.live/file/1769832796939_image_3.jpg)

无数人为了用上它，疯狂的买Mac Mini。

![图片](https://upload.maynor1024.live/file/1769832802216_image_4.jpg)

我甚至刚刚打开了一下美团外卖，发现，居然没货了？？？

![图片](https://upload.maynor1024.live/file/1769832807014_image_5.jpg)

买Mac Mini的原因也特别简单，你可以把Clawdbot理解为，一个主动性极高、有你系统极高的权限的本地Agent。

他可以帮你把你本地文件夹里的东西直接改了，帮你炒股，帮你处理邮件，帮你干一切。

官方的定义是，一个“你在自己设备上运行的个人AI助理。”

![图片](https://upload.maynor1024.live/file/1769832812619_image_6.jpg)

其实从任务上，这玩意看着跟Claude Code有点像，不过Claude Code本身因为名字，所以大家更把它当作是编程Agent，但其实Claude Code本身已经偏通用Agent了。

因为我们整个现代互联网社会，几乎都是建立在代码之上。

所以Claude Code其实有点吃了名字的亏，而Clawdbot，就没有这样的名字的顾虑了。

因为这玩意是本地的运行的，权限极高，同时主动性强到离谱，所以会带来非常强的安全隐患，你也不想你随口一句话，他就给你发个社死的朋友圈，或者把你文件删了，又或者，把你把钱花完了，对吧。

比如我今天在朋友圈里看到的很能代表他主动性的案例。

![图片](https://upload.maynor1024.live/file/1769832823143_image_7.jpg)

这个风险，是绝大多数人承受不起的，所以大多数的玩家们，选择的做法就两种，一种是在一台新电脑上玩Clawdbot，一种选择是上云服务或者虚拟机上部署。

后一种，说实话，对于大多数人来说，门槛太高了，上云还是比较复杂的。

不过也有反应快的，比如腾讯云，直接提供了一键服务。

![图片](https://upload.maynor1024.live/file/1769832824537_image_8.jpg)

而这时候，买一台全新的Mac Mini，反而成了最简单的做法，不仅省心省力，还省电。

除了，需要爆个几千块钱的金币。。。

也不是一般人能玩得起的。

而如果你真的没有那么在乎风险，或者就是想在自己的电脑上用，那几乎没有要求，一个很多年前的二手老电脑，都能跑的起来，完全没必要去给苹果去交税。

其实我真的觉得，Mac Mini这波背后的热度有点不正常。。。

而Clawdbot本身其实大部分的能力，跟Claude Code是一样的，但是还是会有一些区别，大概是几点。

\1. 它能接入你的WhatsApp、Telegram、Discord这些国外的聊天入口，国内也有人把飞书接了进去，QQ的方案我们自己正在试，也能搞，也就是说，你可以出门在外，给你的聊天软件发一句消息，他就能开始在你的本地电脑上进行操作，用普通的聊天软件作为入口，这个就太丝滑了。

\2. 拥有长期记忆，会把记忆作为文件存在你的本地，所以类似于ChatGPT这种体验类似，在日常对话中，能用记忆搜索把相关内容捞回上下文，所以跨会话积累更可控也更容易被理解和改造。

\3. 开源，能自己折腾，能部署，背后能随便接自己喜欢的模型，跟OpenCode有点像，也支持Skills。

再结合天时地利人和，还有在Coding之下人们的焦虑。

于是，Clawdbot，爆了。

Github上已经6万3的Star了，增长曲线极其离谱。

![图片](https://upload.maynor1024.live/file/1769832832765_image_9.jpg)

部署这个玩意，说简单也简单，说麻烦也麻烦，Mac部署和Windows部署简直不是一个难度级别的。

不过我这里，还是想教大家一下，怎么部署下来玩，以及如何，接入到飞书里面，让我们在国内也能玩的起来。

首先教大家先安装一下Clawdbot。

一行命令就可以，其实不难，很简单。



下面的命令适用于Mac、Windows和Linux，我这里选择的是windows进行部署测试。

PS：这里我要严重声明一下，这是我在公司放的测试笔记本，这里提醒大家一定注意注意安全问题，如无必要，不要在自己的主力机安装，一定一定要用备用机，这个预防针我一定要提前打，这玩意权限很高，一定要悠着点。

如果你直接在你的主力机上跑，万一AI抽风执行个rm -rf /，你电脑里的那点隐私和学习资料可全完了。



千万别到时候重要文件被删了然后来骂我= =



这个命令特别简单：

- 

```
# Windows安装使用下面这个命令iwr -useb https://molt.bot/install.ps1 | iex
# macOS / Linux / Ubuntu / Debian安装使用下面这个命令curl -fsSL https://molt.bot/install.sh | bash -s -- --install-method git 
```

记得运行这个命令前，一定要先装个node.js，得22版本以上，要不然会报错。

然后你就能看到他开始安装了。

![图片](https://upload.maynor1024.live/file/1769832836143_image_10.jpg)

安装好之后，会出现这么个东西。

问你选yes还是no。

![图片](https://upload.maynor1024.live/file/1769832834511_image_11.jpg)

这句话的大概意思就是，我懂这个大龙虾能力很强但是风险极大，你确认吗继续吗。

只有选yes，他才让你进行下一步。。。

你要选个No，直接给把进程关了，也是非常的霸王条款。。。

![图片](https://upload.maynor1024.live/file/1769832838252_image_12.jpg)

当你yes之后，就能看到一个选项。

![图片](https://upload.maynor1024.live/file/1769832843331_image_13.jpg)

第一个就是快速启动，后续通过clawdbot configure配置信息，第二个就是先手动配置。

我们选第一个。

然后他就会跟你说，让你配置一个模型。

![图片](https://upload.maynor1024.live/file/1769832846889_image_14.jpg)

因为我是ChatGPT Pro会员，并且我自己很喜欢用Codex且额度极高，所以我就可以直接用Codex OAuth，也就是把你Codex的额度挂过来，跟OpenCode玩法是一样，而且OpenAI自己非常支持这种做法，所以几乎没有风险。

这里要注意，千万别用Claude Max的那个额度来去挂Clawdbot，Anthropic这个狗东西现在只准那个的额度在Claude Code上用，你用Clawdbot授权可能直接就会被封号，X上已经有好多案例了。

当然，你也可以选择国产，比如MiniMax、Qwen、智谱，都可以。

**💡 推荐：使用第三方API中转服务**

如果你不想用官方API（需要魔法、价格贵、支付麻烦），可以使用第三方API中转服务。

推荐：**https://apipro.maynor1024.live/**

**优势：**
- ✅ 国内直连，无需魔法
- ✅ 价格便宜，比官方便宜50%-70%
- ✅ 支持支付宝、微信支付
- ✅ 支持Claude、GPT、Gemini等多种模型
- ✅ 24小时稳定运行

**如何配置第三方API中转？**

1. **注册并获取API Key**
   - 访问：https://apipro.maynor1024.live/
   - 注册账号并充值（建议先充10-20元测试）
   - 在"API管理"页面创建API Key
   - 复制保存你的API Key（格式：sk-xxxxx）

2. **配置Clawdbot使用第三方API**

   安装完成后，编辑配置文件：
   
   ```bash
   # 打开配置文件
   nano ~/.clawdbot/clawdbot.json
   ```
   
   在配置文件中添加以下内容：
   
   ```json
   {
     "models": {
       "mode": "merge",
       "providers": {
         "maynor": {
           "baseUrl": "https://apipro.maynor1024.live",
           "apiKey": "sk-你的API密钥",
           "auth": "api-key",
           "api": "anthropic-messages",
           "models": [
             {
               "id": "claude-haiku-4-5-20251001",
               "name": "Claude Haiku 4.5",
               "reasoning": false,
               "input": ["text"],
               "cost": {
                 "input": 0,
                 "output": 0,
                 "cacheRead": 0,
                 "cacheWrite": 0
               },
               "contextWindow": 200000,
               "maxTokens": 8192
             }
           ]
         }
       }
     },
     "agents": {
       "defaults": {
         "model": {
           "primary": "maynor/claude-haiku-4-5-20251001"
         }
       }
     }
   }
   ```

3. **重启Gateway服务**
   
   ```bash
   clawdbot gateway restart
   ```

4. **验证配置**
   
   打开Web UI，发送测试消息，查看右上角是否显示正确的模型名称。

**配置要点：**
- ⚠️ `baseUrl` 不要包含 `/v1` 后缀（SDK会自动添加）
- ⚠️ 模型ID格式必须是 `provider名称/模型ID`
- ⚠️ 使用 `mode: "merge"` 可以保留内置模型
- ⚠️ 配置后必须重启Gateway才能生效

**费用参考：**
- 简单对话：约 ¥5-10/月
- 文件处理：约 ¥15-30/月
- 代码生成：约 ¥30-60/月
- 重度使用：约 ¥150-300/月

不过这里我提一嘴，这个玩意，上下文工程做的奇差无比，所以，他烧Token的速度是你难以想象的离谱。

比如我们有个小伙伴，测试的时候，随随便便用GLM-4.7跑了两天，它直接跑掉了将近3000万Token。。。

![图片](https://upload.maynor1024.live/file/1769832855382_image_15.jpg)

不敢想象，要是换成Claude的API，估计得卖房了才供得起这玩意24小时烧Token了。。。



一个X的十几篇文章的爬虫任务，直接干没了100万Token，真的，太离谱了。

配置好以后，还有一个选择频道，也就是选择用什么聊天软件来跟他对话。

![图片](https://upload.maynor1024.live/file/1769832860094_image_16.jpg)

这块全部都是海外的，我们正常人也不用这玩意，所以这块可以选择最后一个，直接跳过，我们后续可以教大家，怎么用飞书来启动这个东西。

再然后，他会问你，要不要配置他给的那些个技能，直接无脑Yes就行。

![图片](https://upload.maynor1024.live/file/1769832863935_image_17.jpg)

然后会让你选择用什么管理器安装，我自己一般最常用的就是npm，这个你装了node.js，就自动有npm命令了。

![图片](https://upload.maynor1024.live/file/1769832872118_image_18.jpg)

再然后，就会给你一堆Skills。。。

![图片](https://upload.maynor1024.live/file/1769832874840_image_19.jpg)

每一个后面都有描述，你可以挑你喜欢的装上，你要是懒得挑，直接跳过就行，反正后续跟他对话也能装。

继续下一步，会问你要不要配置hooks。

![图片](https://upload.maynor1024.live/file/1769832874830_image_20.jpg)

你可以理解为三个插件。

boot-md是启动时自动加载一段markdown文本当作默认引导内容，常用于把你的规则、偏好、项目背景这些在每次启动时塞进去。

command-logger是把你在Clawdbot里执行过的命令和关键操作记一份日志，方便排查问题和复盘。你如果比较在意隐私或不想留痕，就别开它。

session-memory是保存会话相关的状态或记忆，让它下次能延续上下文，体验会更连贯。

这三个我建议都开，都非常的实用。

最后的最后，终于，一切就绪！成功！

看到安装好的界面，然后，就可以用这个命令，来启动Clawdbot。

- 

```
clawdbot gateway --verbose
```

然后，你就能看到一串代码。

一般端口都默认是18789了，所以你可以直接复制。

- 

```
http://127.0.0.1:18789/chat
```

然后就能看到亲切的，小龙虾界面了。

![图片](https://upload.maynor1024.live/file/1769832882469_image_21.jpg)



不过，我相信所有人，肯定都是想在手机端或者别的聊天软件里面用的对吧。

这个才是他，最大的魅力。

所以，在国内，现在最容易接进去的，就是飞书了。

因为飞书的机器人，刚好跟这玩意非常的吻合。

并且有个大佬，也做了飞书连接Clawdbot的项目，github网址在此：

https://github.com/m1heng/Clawdbot-feishu



![图片](https://upload.maynor1024.live/file/1769832889336_image_22.jpg)

说实话。

我对着GitHub上那个飞书插件项目的说明，一步步手动配置。

结果，我对着屏幕修了整整一两个小时的Bug，给人都整麻了，一直报错、一直安装失败。。。

![图片](https://upload.maynor1024.live/file/1769832889244_image_23.jpg)



我当时都快疯了。

但是突然一想，不对啊，我个呆逼。

我不是装了Clawdbot吗，不是很屌吗，让它自己装啊，我在这修个屁。

于是我大手一挥就直接在刚刚打开的WebUI输入下面的这条信息。

- 

```
给我安装Clawdbot plugins install @m1heng-clawd/feishu 这个命令
```

然后。。。

它居然真的给自己...安装好了，那我刚才那一两个小时的折腾，到底算什么=_=？

![图片](https://upload.maynor1024.live/file/1769832890376_image_24.jpg)



他说装好了之后，还需要去飞书开放平台（open.feishu.cn）建个应用，把App ID和App Secret记下来，接下来要用到，也是关键的一步。







![图片](https://upload.maynor1024.live/file/1769832898559_image_25.jpg)



然后最骚的操作来了。。。

你直接在对话框中发送自己的App ID App Secret 给他。

没错，它会自己看着办，把剩下的配置全给你搞定。



![图片](https://upload.maynor1024.live/file/1769832907324_image_26.jpg)



真的，爽到爆炸。

然后就是飞书开放平台自己的一些设置了，这个就不太好上AI了，而且也不复杂，大家先把机器人加入进去。



![图片](https://upload.maynor1024.live/file/1769832911773_image_27.jpg)



接下来是开启一些必要的权限，GitHub中作者也有讲到。



![图片](https://upload.maynor1024.live/file/1769832918082_image_28.jpg)



![图片](https://upload.maynor1024.live/file/1769832924864_image_29.jpg)

然后，你需要把下面的这些，也都配置上。

![图片](https://upload.maynor1024.live/file/1769832932841_image_30.jpg)

最后，一切大功告成！

然后你就进行发布。



![图片](https://upload.maynor1024.live/file/1769832934727_image_31.jpg)



就可以在飞书里面，跟他畅聊了。

![图片](https://upload.maynor1024.live/file/1769832935284_image_32.jpg)



配置完之后，因为是测试机，所以其实没啥文件，我就随手试了一个非常现实的场景。

就是我们公司报销发票，需要把发票内容填进一个Excel表格模板里。

以前很多人对着屏幕一张张填，其实挺呆逼的。

现在，只需在飞书给它下个令。

它便会在后台一顿操作，打开本地文件、读取内容、自动填充 Excel……一眨眼的功夫，活儿干完了。

虽说干的有点糙，但有那味了。



![图片](https://upload.maynor1024.live/file/1769832946272_image_33.jpg)



![图片](https://upload.maynor1024.live/file/1769832945929_image_34.jpg)



非常的有意思，这台电脑我就一直放在那，也没打算关机。

晚上回了家，我还是可以用手机上飞书，来对它进行遥控，还是相当好玩的。

以上，基本就是Clawdbot的绝大多数信息了。

说实话，Clawdbot的火爆，其实是大家对AI进场干活的一种极度渴望。



所以我现在对Clawdbot的态度，其实很矛盾。

因为，安全是一笔账。

它可以帮你干活，也可能在你走神的时候，顺手把什么东西改了或者删了，你甚至可能，根本发现不了，当某一天你突然发现的时候。

那一刻，你一定会血涌上头，然后大喊一句：

我草XX，你个XX！！？？

但是我其实既想劝你悠着点。

但也想说一句，这种对未知世界的好奇，真的很有意思。

如果你是那种对新东西很有好奇心、愿意拿一台闲置电脑当实验田的人，这种究极主动性的本地Agent体验一次，绝对会刷新你对 AI 的想象边界。

他可能现在在你看来，会有点冒犯，但，未来我们理想中的Agent，不就是这样吗。

只是准确性和容错率的不同罢了。

特别是当你躺在床上，突然想起了一个事，打开手机，再打开飞书或者QQ，甚至未来有可能是微信，然后发一句消息。

对面那个Clawdbot，就开始矜矜业业的干活了。

这种感觉，真的很上头，也很魔幻。

我真正想劝的其实是。

你在把钥匙交出去之前，一定要先想好，这把钥匙，究竟希望它开的是哪扇门。

就像你家里的管家或者阿姨一样，厨房、客厅、衣帽间啥的，可能会给他开放，但是最私密的卧室，甚至是你真正的私人空间，你会放心的把钥匙交给他们吗。

难说。

所以用AI也是一样，Clawdbot确实蛮有意思，也很上头。

但，一定要想清楚，想清楚，到底要把什么交出去。

这其实看的，也是你真正的管理、还有用人的能力。

在想清楚之后。

也愿我们，对世界永远保持好奇。

***\**\*以上，既然看到这里了，如果觉得不错，随手点个赞、在看、转发三连吧，如果想第一时间收到推送，也可以给我个星标⭐～谢谢你看我的文章，我们，下次再见。\*\**\***
