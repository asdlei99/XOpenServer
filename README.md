# XOpenServer

    XOpenServer是由极客联盟烽烟工作室即将开发的开源服务器框架，是基于c++/Lua的架构开发的高性能、分布式游戏服务器框架， 也可作为需要实时交互的移动或web应用框架。

    官方博客网址：geek.iyplay.com

    中国在开源软件方面相比国外是很弱势的，但是近几年中国开源软件也有比较成功的， 比如cocos2d-x....
但是cocos2d-x是客户端的， 目前服务器方面的还比较少，虽然有网易的pomelo，云风的skynet。但是开发文档不全，应用不广。当然我开源XOpenServer的目的并不是要做服务器端的cocos2d-x，我们的主要目的是分享经验。
    俗话说授人以鱼不如授人以渔, 我们并非一次性公布全部代码, 而是以工作的形式, 一步一步把搭建框架的过程呈现出来, 让关注我们项目的每个人都能够看懂, 真正了解服务器开发过程, 并结合实际游戏开发, 分享给大家更多的工作经验.

XOpenServer的理念
    XOpenServer意在让游戏开发工作者不必在乎服务器底层架构设计，只需编写自己游戏相应的逻辑，让游戏开发变得更简单，让客户端程序也能轻松构建自己的服务器。同时，我们尽所能详尽编写我们游戏架构的制作过程，让所有服务器端程序，客户端程序都能读懂我们的设计，能够根据自己的需求随心所欲地去修改。
    在框架设计中，我们后期会加入拓展模块， 让第三方很容易拓展自己的模块， 第三方拓展插件作者也可以分享自己编写的模块， 让游戏及应用开发变得更自由，更简单。

XOpenServer的应用范围
    XOpenServer最适合的应用场景是网络游戏（不限于页游、手游、社交游戏、html5游戏），联网应用（移动应用，需要实时交互的web应用）等。
    从性能上，对大型MMO，ARPG游戏，启用多个逻辑进程来均衡负载， 大致最高同时在线2000以下服务器是没有问题，对于大于2000以上的亦可使用，但是性能上暂时无法保证满足需求。性能的主要瓶颈在于主程的存在，同一进程无法容纳太多用户。另外目前采用mysql也是性能的瓶颈，后期会采用redis来做缓存数据库，解决这个瓶颈问题。当然前面说的人数是笼统的说法， 对于不同游戏和应用， 需要根据逻辑的复杂性进行分析。对于逻辑简单的游戏或者应用来说， 同时在线自然可以更多一些。如卡牌类的游戏没有主城概念， 则只需要多配几个逻辑服务器即可， 理论上优化好登陆模块，在线可以无限增加，主要看物理机配置。