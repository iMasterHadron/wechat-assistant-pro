[![ 由Wechaty提供 ](https://img.shields.io/badge/Powered%20By-Wechaty-blue.svg)](https://github.com/wechaty/wechaty)
[![node version](https://img.shields.io/badge/node-%3E%3D16-blue.svg)](http://nodejs.cn/download/)
![](https://img.shields.io/badge/Window-green.svg)
![](https://img.shields.io/badge/Mac-yellow.svg)
![](https://img.shields.io/badge/Centos-blue.svg)
[![](https://img.shields.io/badge/Docker-red.svg)]()

## 智能微秘书

智能机器人配置管理平台，一键接入ChatGPT对话，无缝适配Dify,FastGPT,Coze知识库！

支持群组，个人定义不同的角色，灵活配置各种对话模式，绘图，识图，联网查询，GPTs，语音分析，技能丰富多样！拥有各种定时任务，RSS订阅，倒计时提醒，新闻咨询发送，批量群发，转发，跨群聊天，提醒功能，API发送消息

配合智能微秘书客户端可以一键接入公众号，企业微信，Gitter，Lark，WhatsApp，5G消息等Wechaty所支持的协议

[微秘书官网](https://wechat.aibotk.com)

本项目是搭配智能微秘书平台使用的微秘书客户端，想要使用自己的机器人，必须自己部署微秘书客户端方可。

## 依赖

node 版本 >18

## 项目说明

本项目是基于[wechaty](https://github.com/wechaty/wechaty) 的开源智能机器人项目，更多关于`Wechaty`项目说明及 api 
文档可以移步：[wechaty 介绍](https://wechaty.js.org/docs/howto/)

微秘书部署详细教程链接地址：[微秘书文档](https://help.aibotk.com/?plugin=czw_emDoc&post=5)

## 更多功能说明

![](./doc/img/aibot.png)

- [x] 每日说,定时给女朋友发送每日天气提醒，以及每日一句

* 定时提醒

- [x] 当天定时提醒 例："提醒 我 18:00 下班了，记得带好随身物品"
- [x] 每天定时提醒 例："提醒 我 每天 18:00 下班了，记得带好随身物品"
- [x] 指定日期提醒 例："提醒 我 2019-05-10 8:00 还有 7 天是女朋友生日了，准备一下"

* 智能机器人

- [x] 天行机器人
- [x] 图灵机器人
- [x] 微信开放对话平台
- [x] Coze
- [x] 扣子
- [x] Dify
- [x] FastGPT
- [x] Qanything
- [x] 火出圈的ChatGPT
  - [x] 支持多种模型在线切换，代理在线配置
  - [x] 自定义对话配置， 不同群，不同好友，不同的对话配置
  - [x] Prompts 市场，设定不同角色
  - [x] GPT-4V识图功能
  - [x] DALL-E3绘图功能
  - [x] 多模态，Dify插件，联网模式，爬取网站内容
- [ ] 更多

* 定时任务

- [x] 新闻资讯定时发送
- [x] 个性化内容定时发送
- [x] 固定素材内容定时发送
- [x] 倒计时提醒
- [x] rss订阅推送
- [ ] 更多功能等你来 pr

* 关键词

- [x] 关键词加好友，加好友欢迎词设置
- [x] 关键词加群，群欢迎词设置
- [x] 关键词回复
- [x] 技能中心
    - [x] 天气查询 例："上海天气"
    - [x] 垃圾分类 例："?香蕉皮"
    - [x] 名人名言 例： "名人名言"
    - [x] 老黄历查询 例： "黄历 2019-6-13"
    - [x] 姓氏起源 例： "姓陈"
    - [x] 星座运势 例： "\*双子座"
    - [x] 神回复 例： "神回复"
    - [x] 获取表情包 例： "表情包你好坏"
    - [x] 获取美女图 例： "美女图"
    - [x] 群合影 例： "群合影"
    - [x] 牛年头像 例： "牛气冲天"
    - [ ] 更多待你发现
- [x] 进群自动欢迎
- [x] 加好友自动回复

* 自动更新配置文件，无需重启

- [x] 默认给机器人发送 ‘更新’ 触发拉取新配置文件操作，可在面板`小助手配置->关键词回复->关键词事件`进行修改关键词

* 特色功能

- [x] api发送消息
- [x] 主动更新配置
- [x] 主动同步好友和群列表
- [x] 跨群聊天，自动转发消息
- [x] 不同好友或者群组设置不同的ChatGPT角色，实现千人千面
- [x] 语音识别，语音发送

更多详情介绍：[功能概览](https://help.aibotk.com/?plugin=czw_emDoc&post=31)

## 提前准备

### 注册智能微秘书管理账号

1. 注册：[智能微秘书](https://wechat.aibotk.com/#/signup?r=dBL0Bn)

2. 初始化配置文件`小助手配置->基础配置`，修改后保存

3. 个人中心获取`APIKEY`和`APISECRET`，后续配置用到

![](./doc/img/user-center.png)

### 注册天行数据账号

由于本项目大部分定时资讯和一些天气接口来自于天行数据，所以需要提前准备好天行数据的账号，同时申请好相关接口的权限

1、注册: [天行数据](https://www.tianapi.com/source/865c0f3bfa)

2、申请接口权限

必选接口

* [天行机器人](https://www.tianapi.com/apiview/47): https://www.tianapi.com/apiview/47
* [天气](https://www.tianapi.com/apiview/72):https://www.tianapi.com/apiview/72
* [新闻](https://www.tianapi.com/apiview/51) : https://www.tianapi.com/apiview/51 ** (新闻资讯只需要申请这个接口即可，不需要申请具体的分类接口，务必记着)**
* [垃圾分类](https://www.tianapi.com/apiview/97): https://www.tianapi.com/apiview/97

可选接口（如果想使用相应的功能还是必须申请的），但是如果默认使用了天行机器人，以下功能接口无需申请也可以，机器人会直接返回对应信息

* [土味情话](https://www.tianapi.com/apiview/80):https://www.tianapi.com/apiview/80
* [名人名言](https://www.tianapi.com/apiview/92):https://www.tianapi.com/apiview/92
* [星座运势](https://www.tianapi.com/apiview/78):https://www.tianapi.com/apiview/78
* [姓氏起源](https://www.tianapi.com/apiview/94):https://www.tianapi.com/apiview/94
* [顺口溜](https://www.tianapi.com/apiview/54):https://www.tianapi.com/apiview/54
* [老黄历](https://www.tianapi.com/apiview/45):https://www.tianapi.com/apiview/45
* [神回复](https://www.tianapi.com/apiview/39):https://www.tianapi.com/apiview/39
* [歇后语](https://www.tianapi.com/apiview/38):https://www.tianapi.com/apiview/38
* [绕口令](https://www.tianapi.com/apiview/37):https://www.tianapi.com/apiview/37
* [疫情](https://www.tianapi.com/apiview/169):https://www.tianapi.com/apiview/169
* [网络取名](https://www.tianapi.com/apiview/36):https://www.tianapi.com/apiview/36

目前平台只适配了以上天行数据的接口，其他接口暂未适配，如有需要，可以联系定制


## 开始

### 源码运行

需要node版本>16，如果是windows 系统，请使用win10及以上版本

#### Step 1: 安装

克隆本项目，并进入项目根目录执行 `npm install`安装项目依赖

#### Step 2: 配置

`src/index.js`代码中配置`APIKEY`和`APISECRET`

#### Step 3: 运行

执行命令`npm run start`，终端会显示二维码，可以直接扫码，也可以到[智能微秘书](https://wechat.aibotk.com)（小助手配置->登录状态中进行扫码登录）

#### Step 4: 配置相应功能

在[智能微秘书](https://wechat.aibotk.com?r=dBL0Bn)中配置你需要的功能后，给启动的微信发送`更新`关键词即可拉取最新配置（或者你自己设置的更新关键词，初始关键词是`更新`，**
每次修改配置后，请记得一定发送关键词更新配置**


### Docker部署

由于自己构建部分依赖安装比较慢，或者经常会卡住，所以本项目已经提前构建好发布到dockerhub了，直接pull就行了

> 注：使用第三方镜像源加速的。拉取的可能不是最新版本，所以会运行不起来，建议使用官方镜像源，自行切换，不会的可以百度一下

![](https://img.aibotk.com/picgo/202304141139150.png)

可以在[https://hub.docker.com/r/aibotk/wechat-assistant/tags](https://hub.docker.com/r/aibotk/wechat-assistant/tags) 这里查看到最新的 tag版本

[![](https://img.aibotk.com/aibotk/help/7NOgdA20240112114359.png)](https://img.aibotk.com/aibotk/help/7NOgdA20240112114359.png)

拉取完毕的大小大概不到 500M ,如果你拉取的大小超过 1G，大概率是拉取错版本了，请切换成官方源拉取

> 国内用户可以用这个镜像地址进行拉取 registry.cn-hangzhou.aliyuncs.com/aibotk/wechat-assistant:latest

#### step1： 拉取镜像

```shell
# docker pull registry.cn-hangzhou.aliyuncs.com/aibotk/wechat-assistant:latest

docker pull aibotk/wechat-assistant

```

#### step2： 启动docker


```shell
# docker run -d -e AIBOTK_KEY="微秘书apikey" -e AIBOTK_SECRET="微秘书apiSecret" --name=wechatbot registry.cn-hangzhou.aliyuncs.com/aibotk/wechat-assistant:latest

docker run -d -e AIBOTK_KEY="微秘书apikey" -e AIBOTK_SECRET="微秘书apiSecret" --name=wechatbot aibotk/wechat-assistant
```

查看docker日志

```
docker logs  wechatbot
```

### 自行构建docker镜像

需要提前安装 docker 环境，项目根目录执行一下命令

```shell script
docker build -t wechat-assistant .
#web协议
docker run -e AIBOTK_KEY="微秘书apikey" -e AIBOTK_SECRET="微秘书apiSecret" wechat-assistant
```

其他步骤同上

### 使用Gitpod 在线运行测试

现智能微秘书已经适配Gitpod，如果你想测试自己的账号是否能够正常登录，可以在线运行一下测试，此环境仅做测试，不建议作为生产环境使用。

Gitpod 是一个在线和开源平台，用于自动化和现成代码的开发环境。您可以点击下面的按钮在gitpod 上访问wechat-assistant-pro的完整设置。如果您以前从未使用过 gitpod，则需要使用您的 gitHub 帐户登录。

[![GitPod Ready-to-Code][gitpod_img]][gitpod_link]

更多关于Gitpod的信息可以参考: https://wechaty.js.org/2021/02/06/wechaty-getting-started-without-leave-your-browser/

### Railway部署

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/w6W1s-?referralCode=2rS9In)

环境变量：AIBOTK_KEY和AIBOTK_SECRET必填

### ipad协议运行

查看：[如何使用padlocal协议](https://github.com/leochen-g/wechat-assistant-pro/issues/61)

### 企微协议运行

查看：[如何使用企微部署](https://github.com/leochen-g/wechat-assistant-pro/issues/60)

### 公众号部署

公众号部署目前仅只支持源码部署配置

修改文件`src/office.js`文件变量

```javascript
import {WechatyBuilder} from 'wechaty'
import {WechatyWebPanelPlugin} from 'wechaty-web-panel'
import {PuppetOA} from 'wechaty-puppet-official-account'
const name = 'office-assistant-pro';
let bot = '';
const oa = new PuppetOA({
    appId           : '公众号appid',
    appSecret       : '公众号appSecret',
    token           : '公众号加密token',
    // personalMode: true, // 如果你是个人订阅号或者未认证 请开启此项
    // port 和 webhookProxyUrl 自己选择一个
    // port: 8077, // 有自己域名或者服务器 可以启用这个 服务启动的端口 自己映射好配到公众号后台机就行
    webhookProxyUrl: 'https://****.loca.lt'  // 如果没有自己的域名可以直接用默认自带穿透代理服务localtunnel ***替换成随机字符串即可  这个域名记得配置到公众号后台
})


bot = WechatyBuilder.build({
    name, // generate xxxx.memory-card.json and save login data for the next login
    puppet: oa,
});


bot
    .use(
        WechatyWebPanelPlugin({
            apiKey: '****',
            apiSecret: '****'
        }
    ))
bot.start()
    .catch((e) => console.error(e));
```

执行命令：`npm run office`

## 体验与交流

扫描下方二维码，添加智能微秘书，体验以上所有功能，发送加群关键词即可进入交流群，如果微信无法添加可以先进QQ群：1045575073

![](http://image.xkboke.com/picgo/202301141927005.png)

## 更新日志

[更新日志](./CHANGELOG.md)

## 常见问题处理

参见[https://help.aibotk.com](https://help.aibotk.com/?plugin=czw_emDoc&post=5)

## 面板预览

![](./doc/img/index.png)
![](./doc/img/roomasync.png)
![](./doc/img/everyday.png)
![](./doc/img/event.png)
![](./doc/img/material.png)

## 功能预览

![](./doc/img/news.jpeg)

个人定时与群定时任务

![](./doc/img/func.jpeg)



## 免责声明

本软件依据github上开源项目 Wechaty

通过简单的设置UI和交互，运行IM机器人。

请遵守国家法律政策，请勿用于非法犯罪行为！

请合理使用，一切不良行为和后果均与作者无关！

本项目不参与解析任何底层代码，只是适配层，所有底层协议均为第三方提供，与本人无关！

[gitpod_img]: https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod
[gitpod_link]: https://gitpod.io/#https://github.com/leochen-g/wechat-assistant-pro
