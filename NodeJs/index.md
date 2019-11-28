# NodeJS介绍

## 目录
<!-- TOC -->

- [NodeJS介绍](#nodejs介绍)
  - [目录](#目录)
  - [大纲](#大纲)
  - [谁在用NodeJS](#谁在用nodejs)
    - [阿里巴巴](#阿里巴巴)
    - [迅雷](#迅雷)
    - [雅虎](#雅虎)
    - [腾讯](#腾讯)
    - [LinkedIn(领英)](#linkedin领英)
    - [网易](#网易)
    - [NETFLIX](#netflix)
    - [微软](#微软)
    - [IBM](#ibm)
    - [Twitter](#twitter)
  - [NodeJs的特性](#nodejs的特性)
    - [特点](#特点)
    - [NodeJS解决其他语言的瓶颈](#nodejs解决其他语言的瓶颈)
    - [优点](#优点)
    - [缺点](#缺点)
    - [适合场景](#适合场景)
  - [浅谈NodeJs的个人使用的相关实践](#浅谈nodejs的个人使用的相关实践)
    - [作为API后台](#作为api后台)
    - [处理图片](#处理图片)
    - [处理数据](#处理数据)
    - [抓取数据](#抓取数据)
    - [构建前台框架](#构建前台框架)
  - [NodeJs在我们当前项目中的应用](#nodejs在我们当前项目中的应用)
    - [主要工程构建](#主要工程构建)
    - [集成 SWTC-LIB](#集成-swtc-lib)
    - [迁移通用业务](#迁移通用业务)
    - [开发定制业务](#开发定制业务)
  - [如何如学习NodeJS](#如何如学习nodejs)
    - [入门](#入门)
    - [进阶](#进阶)
  - [NodeJs最佳实践](#nodejs最佳实践)
    - [搭建运行环境](#搭建运行环境)
    - [选择一个框架进行学习，入门推荐Express](#选择一个框架进行学习入门推荐express)
      - [Express](#express)
      - [Egg](#egg)
    - [相关资源介绍](#相关资源介绍)

<!-- /TOC -->

## 大纲

- 谁在用NodeJS
- NodeJs的特性
- 浅谈NodeJs的个人使用的相关实践
- NodeJs在我们当前项目中的应用
- 如何如学习NodeJS
- NodeJs最佳实践

## 谁在用NodeJS

### 阿里巴巴

1. 全栈 web 应用
2. 前后端分离方案
3. 统一的前端本地开发工具及服务
4. 用来替代 php 的模版渲染环境
5. 淘宝数据魔方
6. 淘宝指数
7. 淘宝-全景洞察
8. 用nodejs替代老的mvc层
9. 其他方向
   
阿里是业界最早的一批使用 Node.js 来做线上大流量应用的公司，早在 2011 年的就已经开始在生产环境中使用。

众所周知，在阿里的技术栈中， Java 是最最核心的，那 Node.js 扮演怎么样的一个角色呢？

基础设施大部分采用 Java/C++ 实现，变化较少，有事务要求的 Business Services 通常使用 Java 实现。
而 Node.js 则替代过去 PHP/Java Web 的场景，用在需要快速迭代，需求变化非常快的用户侧。
据不完全统计，目前阿里 Node.js 的开发者几百号人，线上的应用也非常之多，仅次于 Java 应用，光对外服务的进程数就超过 1w+

### 迅雷

1. PC迅雷WEB应用，后端直出、灰度控制等，1000W左右PV，使用2台服务器
2. 前端接入层， 峰值QPS有1.8W左右，使用3台服务器。
3. 迅雷升级服务
4. 很多运营类系统，内部使用的公共服务都采用Node编写。
  
迅雷的前端团队在向Node转，不少写PHP的同学都开始用Node写新服务。项目基本上基于express架构，开发效率较高。复杂度随着业务的需求在慢慢增加，node天生对模块化做的很好，加上迅雷内部的XNPM仓库的使用，项目扩展比较平滑。

### 雅虎

雅虎开放了Cooktail框架，将YUI3这个前端框架的能力借助Node延伸到了服务器端。

### 腾讯

将Node应用到长连接，以提供实时功能。

### LinkedIn(领英)

移动网站也是使用的Node。

### 网易

游戏领域对并发和实时要求很高，网易开源了Node的实时框架pomelo。

### NETFLIX

NETFLIX 是一家国外比较出名的视频公司

他们后端以前一直都是 Java，整体架构也比较复杂，业务发展很快，很多老的代码都很难维护，后来为了跟上业务发展的步伐，他们要做整体架构大调整，遵循简洁高效的面向服务的架构目标，过程中他们把服务端相对比较靠前的部分全部采用 Node.js 来实现，后面还是 Java，于此同时前端部分也采用 ReactJS 重写掉了。

之所以采用 Node.js 其中一个很重要的原因就是他们希望前后端能够使用同一种语言，这样他们的工程师就没有跨语言的障碍和成本（knowledge shifting），而且 Node.js 整个社区活跃，生态系统中有大量成熟的工具。

### 微软

Azure 云平台已经支持了 Node.js，意味着你可以在 Azure 部署 Node.js 的应用。

### IBM

IBM 这种老牌软件公司也拥抱了 Node.js，而且抱得还不是一般的紧。他们最早用 Node.js 做了一个很成功的冒烟测试工具——CITGM，这个是内部的工具，而且据说还用在 node core 本身。

除此之外，现在很多人在用的 ExpressJS，IBM 也是接管在开发和维护的。

### Twitter

想像一下像Twitter这样的公司，它必须接收tweets并将其写入数据库。实际上，每秒几乎有数千条tweet达到，数据库不可能及时处理高峰时段所需的写入数量。Node成为这个问题的解决方案的重要一环。如您所见，Node能处理数万条入站tweet。它能快速而又轻松地将它们写入一个内存排队机制（例如memcached），另一个单独进程可以从那里将它们写入数据库。Node在这里的角色是迅速收集tweet，并将这个信息传递给另一个负责写入的进程。想象一下另一种设计（常规PHP服务器会自己尝试处理对数据库本身的写入）：每个tweet都会在写入数据库时导致一个短暂的延迟，因为数据库调用正在阻塞通道。由于数据库延迟，一台这样设计的机器每秒可能只能处理2000条入站tweet。每秒处理100万条tweet则需要500个服务器。相反，Node能处理每个连接而不会阻塞通道，从而能够捕获尽可能多的tweets。一个能处理50000条tweet的Node机器仅需20台服务器即可。

## NodeJs的特性

### 特点

1. 它是一个Javascript运行环境
2. 依赖于Chrome V8引擎进行代码解释
   > V8 JavaScript引擎是Google用于其Chrome浏览器的底层JavaScript引擎。Google使用V8创建了一个用C++编写的超快解释器，该解释器拥有另一个独特特征：您可以下载该引擎并将其嵌入任何应用程序。V8 JavaScript引擎并不仅限于在一个浏览器中运行。因此，Node.js实际上会使用Google编写的V8 JavaScript引擎，并将其重建为可在服务器上使用。
3. 事件驱动
4. 非阻塞I/O
5. 轻量、可伸缩，适于实时数据交互应用
6. 单进程，单线程

### NodeJS解决其他语言的瓶颈

* 并发连接
* I/O阻塞
  > NodeJS遇到I/O事件会创建一个线程去执行，然后主线程会继续往下执行的，因此，拿profile的动作触发一个I/O事件，马上就会执行拿timeline的动作，两个动作并行执行，假如各需要1S，那么总的时间也就是1S。它们的I/O操作执行完成后，发射一个事件，profile和timeline，事件代理接收后继续往下执行后面的逻辑，这就是NodeJS非阻塞I/O的特点。

### 优点

1. 高并发（最重要的优点）
  > Node.js非阻塞模式的IO处理给Node.js带来在相对低系统资源耗用下的高性能与出众的负载能力，非常适合用作依赖其它IO资源的中间层服务。
2. 适合I/O密集型应用
   >Node.js轻量高效，可以认为是数据密集型分布式部署环境下的实时应用系统的完美解决方案。Node非常适合如下情况：在响应客户端之前，您预计可能有很高的流量，但所需的服务器端逻辑和处理不一定很多。
3. 采用事件驱动、异步编程，为网络服务而设计。其实Javascript的匿名函数和闭包特性非常适合事件驱动、异步编程。而且JavaScript也简单易学，很多前端设计人员可以很快上手做后端设计。

### 缺点

* 不适合CPU密集型应用；CPU密集型应用给Node带来的挑战主要是：由于JavaScript单线程的原因，如果有长时间运行的计算（比如大循环），将会导致CPU时间片不能释放，使得后续I/O无法发起；
> 解决方案：分解大型运算任务为多个小任务，使得运算能够适时释放，不阻塞I/O调用的发起；

* 只支持单核CPU，不能充分利用CPU, 可靠性低，一旦代码某个环节崩溃，整个系统都崩溃。原因：单进程，单线程

> 解决方案：1. Nnigx反向代理，负载均衡，开多个进程，绑定多个端口；

> 解决方案：2.开多个进程监听同一个端口，使用cluster模块；

### 适合场景

* RESTful API
  > 这是NodeJS最理想的应用场景，可以处理数万条连接，本身没有太多的逻辑，只需要请求API，组织数据进行返回即可。它本质上只是从某个数据库中查找一些值并将它们组成一个响应。由于响应是少量文本，入站请求也是少量的文本，因此流量不高，一台机器甚至也可以处理最繁忙的公司的API需求。
* 统一Web应用的UI层,即现在流行的前端框架，Vue-React-Angular
    > 目前MVC的架构，在某种意义上来说，Web开发有两个UI层，一个是在浏览器里面我们最终看到的，另一个在server端，负责生成和拼接页面。不讨论这种架构是好是坏，但是有另外一种实践，面向服务的架构，更好的做前后端的依赖分离。如果所有的关键业务逻辑都封装成REST调用，就意味着在上层只需要考虑如何用这些REST接口构建具体的应用。那些后端程序员们根本不操心具体数据是如何从一个页面传递到另一个页面的，他们也不用管用户数据更新是通过Ajax异步获取的还是通过刷新页面。
* 大量Ajax请求的应用
  > 例如个性化应用，每个用户看到的页面都不一样，缓存失效，需要在页面加载的时候发起Ajax请求，NodeJS能响应大量的并发请求。总而言之，NodeJS适合运用在高并发、I/O密集、少量业务逻辑的场景。
* 等其他方面
  
## 浅谈NodeJs的个人使用的相关实践

### 作为API后台
  比较常用，为api提供服务
  * 资源模板库后台
  * 新会员系统后台
  * 知书APP后台
  * 谢谢有礼小程序公众号后台

### 处理图片
  NodeJs可以在Linux调用资源处理图片相关，不建议这样去做。
  * 联合出版集团 GIF 贺卡系统

### 处理数据
  可以处理不同格式的数据，进行数据格式的转换，可以成为工作中的一个实用工具
  * 批量生产SQL语句
  * 数据库的数据迁移转换
  * 拼装需要的数据结构
  * 在页面上进行快速计算等其他处理

### 抓取数据
  提到抓取数据大家想到的是Python，但是NodeJs也可以抓取网络数据。
  * 抓包工具Charles 或者 Fiddler 进行数据抓取
  * 用nodejs进行数据分析
  * 用nodejs进行批量下载图片和资源处理功能
  
### 构建前台框架
  做的比较多的就是构建前台的框架，CLI
  * React 的脚手架
  * Taro 的脚手架
  * 等其他

## NodeJs在我们当前项目中的应用

### 主要工程构建

- [Eggjs](https://eggjs.org/zh-cn/) 阿里云NodeJS服务架构体系
- [工程架构](../太极链/index.md)

### 集成 SWTC-LIB

做为Service去集成 [SWTC-LIB](https://github.com/swtcca/swtclib/tree/master/docs/swtclib) ,进行封装和维护,传参进行调用。做好参数说明

### 迁移通用业务

通用型业务测试和实际运行一段时间之后，可以逐步拆分成插件，后续项目进行插件化集成。如以下相关业务。

- 认证
- 个人中心
- 钱包
- 交易
- 挂买/挂卖
- 后台管理
- 其他通用业务
  
### 开发定制业务

定制业务的开发按照需求进行开发

## 如何如学习NodeJS

> 自己对NodeJs的了解和使用还是比较浅薄，下面的提议只是个人的一些相关的建议

* 语言都是互通的

### 入门

- 学习NodeJs需要有一定的JS基础，建议先看 [菜鸟教程-JS](https://www.runoob.com/js/js-tutorial.html) 这个模块。
- 之后，可以做NodeJs相关的实践，推荐使用 [Expressjs](http://www.expressjs.com.cn/) 这个框架，简单，适用性强，可以作为小公司的企业级框架。
- 之后，可以学习 [Eggjs](https://eggjs.org/zh-cn/) 学习写法和使用的标准。

### 进阶
- 学习 ES6 （6、7、8、9在行业内统称6，如果是特定的说的是ES2015。） 推进 阮一峰大神的 [ECMAScript 6 入门](http://es6.ruanyifeng.com/) ，或者网上去搜一些相关的文章
- 学习 TypeScript ,推荐菜鸟教程的 [TypeScript教程](https://www.runoob.com/typescript/ts-tutorial.html) 这个模块，看完一遍就有个大概了

## NodeJs最佳实践

### 搭建运行环境

1. 下载NodeJs [NodeJs中文网](http://nodejs.cn/) 这里我们统一使用最新稳定版本 v-12.13.0
2. 全局安装Yarn (可选) [Yarn官网](https://www.yarnpkg.com/zh-Hans/) 模块安装，速度比npm要快
3. 安装Mysql (可选)
4. 安装Redis (可选)
5. 安装Vscode (可选), 编辑器，调试NodeJS推荐使用

### 选择一个框架进行学习，入门推荐Express

#### Express

1. 去[Expressjs](http://www.expressjs.com.cn/) 官网
2. 安装入门里面的提示，去安装 Express
3. 安装指南把路由敲一下
4. 安装pm2 使用pm2进行服务器端启动

#### Egg

1. 去[Egg](https://eggjs.org/zh-cn/) 官网
2. 打开快速入门，进行安装
3. 启动egg，项目结构参考代码，或者[太极链结构](../太极链/index.md)

### 相关资源介绍

1. [NPM](https://www.npmjs.com/),类似于 Java 的 maven,一个JS模块库
2. Vscode 断点调试 (可选), 需要配置Vscode