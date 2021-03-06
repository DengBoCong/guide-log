﻿## 总清单

+ PC端
   - 脱机操作，大的区域图直接定点完成锁定
   - 推荐系统，各种业务布局这个考虑安排好
   - 病情监测，各种热力图
> 主要包含大数据分析展示，以及各个控制管理后台的前端界面。整个PC的UI框架使用ElementUI，如何安装和使用自己网上找找看，我这里一般推荐的是[ElementUI 官方文档](https://element.eleme.cn/2.0/#/zh-CN/component/installation)，直接当手册查。整个PC的数据业务逻辑方面使用Vue三件套（Vue+VueRoute+Vuex），具体咋用还是老样子自己学，这里依旧推荐[Vue三件官方文档](https://cn.vuejs.org/v2/guide/)。然后前端中间件使用的是Node，前端的数据接口需要多做一层封装，这和你们之前的基础开发有点子区别，以前你们都是直接使用后端提供的接口，Node怎么用？来官方文档走起来，点这里[Node 官方文档](http://nodejs.cn/api/)。完成了PC总体的技术框架和业务逻辑，接下来就是怎么完成数据展示部分，这里我们可以使用EChart，[官方文档点这](https://www.echartsjs.com/zh/api.html#echarts)，不过对比EChart，我还是更喜欢蚂蚁金服团队做的视图七件套，阿里团队的技术保障我就不多说了，这个的话，就统一使用者六件套吧，[组件源码和文档点这](https://antv.vision/zh)


+ 移动端
> 使用Flutter完成，所承接的任务就是对接PC的脱机操作，以及在采集数据和个人应用使用，包括各种提醒之类的，偏向于用于应用化，具体含有什么功能得仔细想一想，也就是说，这道赛题其实没有要求我们做出APP，不过我们需要在赛题基础上考虑一点的是，我们在没有官方提供数据的前提下，我们怎么获得各种数据，除此之外，我们还还要想想，PC那边的数据呈现肯定不是给用户看的，是给比如公司这种看的，但我们怎么将系统分析的数据结果真正的回馈给用户呢？这是一个值得思考的问题，所以需要有用户能够使用的应用。Flutter怎么用？[官网文档](https://flutter.cn/docs)在这，整套系统的语音控制部分也都是通过手机完成的（注意，是使用管理员账号登录，才能控制PC，普通用户只能使用APP），语音系统使用[讯飞平台，点这里](https://www.xfyun.cn/)，当然要注意一点的是，由于讯飞使用的话，需要分为Android和IOSSDK，所以这里我们只实现Android的语音就可以了（虽然Flutter开发可以安装在Android和IOS平台，但是如果涉及到调用手机底层组件，比如语音控制的时候，就需要混合开发，所以需要Android和IOS的相关知识）。[Android文档](https://developer.android.google.cn/)和[IOS文档](https://www.apple.com.cn/cn/swift/)。怎么开发，我把我原先车载2.0的Flutter前端部分public出来了，你们可以直接去我的GitHub上看，直接[点这这里](https://github.com/DengBoCong/aided_driving_app)给你们导航过去。

+ 后台核心
> 后台部分工作的东西就是对接PC，移动端，已经控制后台的业务逻辑，准备工作就是需要先完成数据库部分的设计以及接口部分的设计，数据库这一块需要所有人一起研究探讨，这个系统需要哪些表，然后接口部分的话，就需要问问前端需要哪些接口，然后访问Node，由Node层向后台接口获取数据，获取的数据格式前后端要对接好。技术这一块，按照你们以前的开发肯定是PC、移动端、控制后台都是一个后台，这样做没有错，不过组织架构不好，这里我打算使用后台核心，也就是说一个后台项目集成了三套独立的后台组织逻辑，在外看起来是一个后台，其实项目里有三个结构。所以这里会使用到Netty框架，这里直接给你们导航到[Netty API文档](http://docs.52im.net/extend/docs/api/netty4_1/)，用到Netty就肯定需要RPC框架，之前和你们说过了，这个系统需要解决高并发的问题，所以这里使用的RPC框架Dubbo框架，还是阿里的开源框架，可能是我自己喜欢阿里的技术的原因吧，哈哈哈喜欢用阿里的东西,前面做并发的时候，我自己用的就是这个框架，挺好用的，[Dubbo文档](https://dubbo.gitbooks.io/dubbo-user-book/content/)在这，缓存这一块我就不要求你们用Redis了，不然感觉你们压力很大，这里我就直接使用比较简单的EHCache，这里还是给你们导航[官网文档](http://www.ehcache.org/documentation/2.8/apis/transactions.html)，我只有英文的，不过你们用Google页面翻译一下，勉强用吧，其实用这个缓存可以直接百度怎么配置，比直接看文档好。然后后台核心还有什么Spring那些我就不多说了。

+ 算法核心
> 算法核心这一块就是对数据进行清洗，模型搭建，这里我就不多说了，因为我没打算让你们插手这个，哈哈哈。

+ 项目概要介绍

+ 项目简介PPT

+ 项目详细方案

+ 项目演示视频

+ 需求分析文档完整

+ 系统设计文档完整

+ 测试案例完整

+ 算法模型、分析模型完整

+ 搭建数据库完整

+ 测试报告完整