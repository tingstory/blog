---

title: Dropshipping on 独立站（自建电商平台）  
date: 2019-03-28  
updated: 2019-10-21
categories: [外贸, Dropshipping]   
tags: 
- 外贸
- Dropshipping
- 网站
permalink: dropshipping-website  
---

eBay 虐我千百遍，我待……Fuck this shit，老子不伺候。走，自立门户去。

<!-- more -->


## 前言

- [什么是 Dropshipping ](https://tingtalk.me/find-dropshipping-products/)
- 双管齐下：eBay（多类目产品） + 自建站（垂直类目的批发 + 零售）


**自建站流程**
- 购买 VPS/虚拟主机，并搭建环境
- 选品：Google、eBay、速卖通、亚马逊多端对比
- 购买域名
- 上架产品：多种价格，零售 + 批发
- 网站推广：主动 + 被动



**参考教程**
- [教程跨境电商，自建站基础](http://reads.pw/?p=42)
https://www.vnlee.com/vultr-vps-and-serverpilot-install-wordpress/




## 购买空间

**VPS/虚拟主机提供商**
- [Linode](https://www.linode.com/)：推荐用国外的邮箱（例如 Outlook、Gmail）
- [Vultr](https://www.vultr.com/?ref=7230883)
    - 价格：每月最低 $3.5 ~ $5.0
    - 优点：可以低成本换 IP（$0.01）；支持微信和支付宝付款
- [SiteGround](https://www.siteground.com/)：WordPress 官方推荐，续费价格较高，胜在稳定


## 开始搭建

- 系统镜像：CentOS
- [宝塔服务器面板](https://www.bt.cn)：一键全能部署及管理（密码不要设置太简单）
- 选择自适应的模板，移动端的流量是大头


runcloud 搭建




### 用 OpenCart 外贸版搭建

- [OpenCart 下载地址](https://www.opencart.com/index.php?route=cms/download) 
- [OpenCart 使用指引](http://docs.opencart.com/zh-hk/introduction/)
- [Tawk.to](https://www.tawk.to/)：Free live chat，免费在线聊天工具，可作为线上客服
- 主题：挑选一个简洁的模板（淘宝、群友团购）


```
# 邮件自动提醒

system->settings->store->E-mail这里的邮件需要和system->settings->store->Mail里的发送邮件相同
要用ssl发送的话,SMTP Hostname需要填上ssl://
SMTP Port填465
要注册和有订单自动发送邮件的话,把下面alert mail里的register和orders勾上
```



### 用 WordPress 搭建

- [获取 WordPress](https://cn.wordpress.org/download/)
- 主题推荐：enfold（较轻，推荐），the 7，divi（轻便），avada（速度不够，配上个wprocket插件）


**插件**
- AMP 类
- Yoast SEO：Edit Snippest。缩短层级，去掉分类页
- Contact From 7，是一个提交表单的插件，如果是做B2B网站都是必备的，用来接收询盘
- Page Builders：排版编辑
- Fastest Cache
- Simple SSL

- URL 结构改为：post-name的结构
- 安装Google Search Console、google analytics
- 网站的状态，他叫monsterinsight。


### Tips

- CDN：[Cloudflare](https://www.cloudflare.com/zh-cn/)
- SSL：[Let's Encrypt](https://letsencrypt.org/)


## 确定选品

- [选品指南](https://tingtalk.me/find-dropshipping-products/)


## 确定货代

- [国际快递时效查询](https://www.trackingmore.com/estimated-delivery-time-calculator-cn)


**从哪里找货代（货运代理）**
- 用 Google / Baidu 搜索：`深圳 + 货代`、`广州 + 货代`、`上海 + 货代`、`北京 + 货代`……
- 从淘宝找货代
- 从 [91出口网](http://www.91chukou.com/) 找

## 购买域名

**哪里购买**
- 推荐在 [NameSilo](https://www.namesilo.com/?rid=d1eaf64se ) 购买。
- [NameBeta](https://namebeta.com/)：共收录 1583 种 [顶级域名](https://namebeta.com/tlds)，汇集互联网上 27 家 [知名域名注册商](https://namebeta.com/registrars)，并且每日更新价格信息（截至。

**挑选意见**

- 首选 `.com`，次选 `.net`，不要选 `.cn`。
- 越短越好。
- 容易朗读和拼写
  - 由能拼读的 1 个 ~ 2 个单词组成，避免使用拼音。
  - 避免使用数字。
  - 避免使用连字符 `-`，例如 `www.ting-talk.com`。
- 带关键词
  - 你经营的项目是玻璃替代品，你可以注册 `GlassRepair.com`  或是 `GlassReplacement.com`。
  - 如果你的产品或服务涉及较多本地业务：`ShanghaiGlassRepair.com`。
  - 品牌词 + 关键词：`TKBattery.com`。
  - 行业词 + 另外一个词（例如动物名称）：`mailchimp.com`。
  - 形容词 + 关键词：`happybasketball.com`
- 被占用怎么办
  - 单词的变化：`storify.com`。
  - 后缀的变化（首选 `com`）：`.store`、`.shop`、`.adult`……


**域名生成器**
- [Business Name Generator by Namelix](https://namelix.com/)
- [Business Name Generator by Oberlo](https://www.oberlo.com/tools/business-name-generator)
- [Domain Name Generator](https://www.namemesh.com/)
- [LeanDomainSearch](https://leandomainsearch.com/)
- [Slogan generator by Oberlo](https://www.oberlo.com/tools/slogan-generator)



**解析域名到空间**
- 上一步你已经租好了房间（VPS / 虚拟主机），你现在需要把你的门牌号（域名）挂在门头上，相当于入住登记
- 国外：免费的 [CloudFlare](https://www.cloudflare.com/)够用，还能免费 CDN
- 国内：选择支持云解析的注册商，比如阿里云



## 上架产品

- 零售客户：免运费
- 批发客户：双方协商运费
- 同类产品设置高中低价
- 有时间的话自己撰写产品描述，有助于 SEO。但不要像淘宝那样赘述，写清楚以下信息即可
    - 产品参数（与图片一致）
    - 应用场景
    - 发货时效（deliver time）
    - 退换货政策
    - 卖家秀（从速卖通）
        - 贵在真实
        - 不要露脸（或者打上马赛克），避免侵犯肖像权
        - 如果有时间，文字评价也可以带上
- 分析差评，改进产品描述。例如买家说大小不合适，就在产品描述中加入尺寸大小相关的参数
- 排版利器：[Typora](https://typora.io/) + [Markdown](https://sspai.com/post/25137)
- [单位换算](https://yue.52wmb.com/tools/convert)




## 吸引流量


### 主动出击

如果你有价格优势（从 1688 进货 / 在速卖通跟卖家砍价），可以选择主动出击。

**如何找客户**
- Google 搜索海外门店，连锁超市
    - `wholesale + product name`
    - `retail + product name`
    - `shop + product name`
    - `distributor + product name`
    - `reseller + product name`
    - `bulk + product name`
    - `warehouse + product name`
    - `supplier + product name`
- 主动联系 eBay 的外国卖家，这类卖家从速卖通或阿里巴巴国际站进货，我们从 1688 进货，价格更有优势
- 用邮件（小号）主动 Contact（联络）自建站（批发）的站长：发邮件，发询盘

> example.com webmaster:
> 
> I am example.com webmaster. Our website provides professional purchasing products you need from China. All the products you need can be wholesaled at a low price. Welcome to contact us. we provide procurement quality audit. The quotation is attached. Please check it.
> 
> Thx, Business is booming. 
> 
> James  
> james@example.com

- 如何防止 email 被丢进垃圾箱：把网址、邮箱、价目表做成图片，而不是放在附件


### 被动出击


- 增加 Blog：发布新闻，新增物流方式，付款方式……
- 搜索引擎优化（SEO）、SNS 推广
- 站群干扰
- 付费投放 Google Ads：后期做大做强了，可以试试


## 出单发货

- 优选有跟踪单号的物流
- 零售：2kg 以内发 ePacket（e 邮宝）包邮
- 批发：费用跟卖家协商，让其承担一部分
    - 空运较快：货不多
    - 海运较慢：货很多
- 给单据、证明、箱体拍照，以免出现纠纷




## 后记


- 下单按钮：Buy Now + Add to Cart  
- 收款
    - 除了 PayPal，可以增加电汇、西联……等收款方式
    - 购买按钮下方有 `付款安全认证`
    - 页面底部有付款渠道图标
- 域名绑定免费的腾讯 [企业邮箱](https://exmail.qq.com/)，例如你的独立站是 www.example.com，就申请 sales@example.com，并确保卖家下单后，手机可以及时收到邮件通知
- 分析海外市场，搭建小语种独立站（韩语站、法语站、日语站、非洲站……）
- 中东站(波斯语、希伯来语和阿拉伯语)的阅读顺序是从右往左