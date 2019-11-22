---

title: 番茄种植指南  
date: 2017-10-11  
updated: 2019-11-23  
categories: [数字生活, 科学上网]  
tags:
- 数字生活
- 科学上网
- Shadowsocks
permalink: fq-diy  

---

在 qiáng 大的国家机器面前，我推荐 99% 的人直接去菜市场购买 [现成的番茄](https://tingtalk.me/fq/)。倘若动手能力还不错，可以买一块地（VPS），自己种番茄。但是要想自产自足，丰衣足食，得学不少网络知识。

<!-- more -->

## 前言

**搭建流程**

1. 在 VPS（服务器）上安装 Shadowsocks 服务端
2. 在电脑 / 手机上安装 Shadowsocks 客户端
3. 启动客户端，输入服务器地址、端口、密码和加密方式等，不出意外，即可访问 Google

**预计花费**

- 金额：$10+
- 时间：1 个小时
- 代码：4 行


## 购买 VPS

VPS 是英文 Virtual Private Servers （虚拟专用服务器）的缩写，你可以粗浅地理解为一台不关机的电脑。借助 VPS 这个「跳板」，我们就可以访问被屏蔽的网站。

如果你有外币单标国际信用卡，可以 [免费申请 Google Cloud Platform](https://tingtalk.me/gcp/) 作为你的 VPS。

如果薅不到 Google 的羊毛，可以试试 [Vultr](www.vultr.com/?ref=7230883) 按小时计费的 Cloud Compute，纵使被当局「封印」了，换一台即可，相比于月付和年付，灵活稳妥。但是开出没有「前科」的 IP 需要一点时间，所以普通用户（包括我）还是直接 [买番茄](https://tingtalk.me/fq/) 吧。


### 注册

- 打开 [Vultr 的官网](www.vultr.com/?ref=7230883)
- 点击 `Creat Account`，注册账户并验证邮箱

### 充值

- `Log in`（登录）后台
- 点击 `Billing`（账单）
- 选择 `Alipay`（支付宝）或 `WeChat Pay` （微信支付）并支付 $10



### 部署

- 选择 `Servers`（服务器）
- 默认进入 `Vultr Cloud Compute (VC2)` 选购页面
- 选择 `Server Location`（服务器地区）
  - 不同运营商，不同地区的出口带宽不一样，请 [实测](https://www.vultr.com/faq/) 为准
  - Server 按小时付费，搭建完不满意或 [测试](https://ipcheck.need.sh/) 已被墙，Deploy 一台新的 Server 即可，再把之前的服务器 Destroy 掉，换机成本低至 $0.01
- `Server Type`（操作系统）：推荐 `Cent OS 7 × 64`
- `Server Size`（配置）：`$5/mo`
  - 优先选择低于 `$5/mo` 的配置（`$2.5/mo`、`$3.5/mo` 经常售罄）
  - 请勿选择 `IPv6 ONLY` 的配置
- `Additional Features`（附加特性）：免费的都可以勾上
- `Deploy Now`
- 当服务器的状态 `Status` 由红色的 `Installing` 变为绿色的 `Running`，代表你购买的 VPS 已经启动了



## 连接 VPS

使用 SSH（Secure Shell）客户端可以远程控制你的刚刚购买的 VPS。macOS 用户可以使用苹果电脑自带的终端（Terminal）连接 VPS；Windows 用户可以使用 PuTTY（读 [ˈpʌti] ）连接 VPS。

### 下载 PuTTY

- 32 位系统（2.81 M）：[putty-0.70-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.70-installer.msi)
- 64 位系统（2.91 M）：[putty-64bit-0.70-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.70-installer.msi)



**PuTTY 中如何复制粘贴**

- 要将复制的文本**粘贴**到终端（PuTTY 的 SSH 登录后的界面）里，只需要右键单击就行了
- 要从终端中**复制**文本，只需要用鼠标左键拖拉选中即可



### 使用 PuTTY

- Host Name (or IP address)：输入 VPS 的 IP Address（以 44.55.666.777 为例）
- Port：22
- Connection type：SSH
- Open
- login as：root
- root@44.55.666.777's Password：复制 VPS 的 Password，鼠标右键粘贴（界面上不会显示任何内容），回车。显示 `[root@vultr ~]#` 则代表连接成功（第一次登录的时候，会出现安全警告，单击 `是（Y）`）



**如何快捷登录 PuTTY**

右键 PuTTY 的快捷方式，依次选择「属性」 - 「快捷方式」 - 「目标」 - 在 `"*:\Program Files\PuTTY\putty.exe"` 后面 `空一格` 输入 `root@IP Address -pw "Password"`，完整展示如下：

```
"D:\Program Files\PuTTY\putty.exe" root@44.55.666.777 -pw "FuckGFW"
```


## 安装 Shadowsocks 服务端

复制下面的 [Shadowsocks 一键安装脚本（四合一）](https://teddysun.com/486.html)，右键粘贴到 PuTTY 的 `[root@vultr ~]#` 后面：

```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

回车:

```
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

回车:

```
Which Shadowsocks server you'd select:
1) Shadowsocks-Python
2) ShadowsocksR
3) Shadowsocks-Go
4) Shadowsocks-libev 
Please enter a number (Default Shadowsocks-Python):
```

输入 `4` 选择 Shadowsocks-libev，回车：

```
You choose = Shadowsocks-libev

Please enter password for Shadowsocks-libev
(Default password: teddysun.com):
```

输入 `密码`（推荐先在记事本写好密码，再粘贴进来），回车：

```
password = ********

Please enter a port for Shadowsocks-libev [1-65535]
(Default port: *****):
```

输入一个喜欢的 `端口号`（推荐五位数），回车：

```
port = *****

Please select stream cipher for Shadowsocks-libev:
1) aes-256-gcm
2) aes-192-gcm
3) aes-128-gcm
4) aes-256-ctr
5) aes-192-ctr
6) aes-128-ctr
7) aes-256-cfb
8) aes-192-cfb
9) aes-128-cfb
10) camellia-128-cfb
11) camellia-192-cfb
12) camellia-256-cfb
13) xchacha20-ietf-poly1305
14) chacha20-ietf-poly1305
15) chacha20-ietf
16) chacha20
17) salsa20
18) rc4-md5
Which cipher you'd select(Default: aes-256-gcm):
```

加密方式选择支持 [AEAD Ciphers](https://wuyanteng.github.io/2018/05/16/%E5%B8%A6%E6%9C%89%E9%99%84%E5%8A%A0%E6%95%B0%E6%8D%AE%E7%9A%84%E8%AE%A4%E8%AF%81%E5%8A%A0%E5%AF%86-libsodium/) 的算法，小白直接选择 `13) xchacha20-ietf-poly1305`（[Why](https://download.libsodium.org/doc/secret-key_cryptography/aead#tldr-which-one-should-i-use)），回车：

```
cipher = xchacha20-ietf-poly1305

Do you want install simple-obfs for Shadowsocks-libev? [y/n]
(default: n):

```

输入 `n`，回车：

```
You choose = n

Press any key to start...or Press Ctrl+C to cancel

```

回车，稍等几分钟：

```
Congratulations, Shadowsocks-libev server install completed!
Your Server IP        :  44.55.666.777
Your Server Port      :  *****
Your Password         :  ********
Your Encryption Method:  xchacha20-ietf-poly1305

Your QR Code: (For Shadowsocks Windows, OSX, Android and iOS clients)
 ss://eGNoYWNoYTIwLWlldGYt**9seTEzMDU6NjM4OTAyMDM4OC5ANDUuNz**MTYwLjIwOTo1NTY2Ng==
Your QR Code has been saved as a PNG file path:
 /root/shadowsocks_libev_qr.png

Welcome to visit: https://teddysun.com/486.html
Enjoy it!

```

**为 Shadowsocks 加把劲（可选）**

这一步是开启 Google BBR 来提升网络速度（开挂）。具体操作如下：

1. 在 `[root@vultr ~]#:` 后粘贴以下代码：

   ```
   wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
   ```

   回车：

   ```
   Press any key to start...or Press Ctrl+C to cancel
   ```

   回车……

2. 安装完成后，脚本会提示需要重启 VPS，输入 `y`，回车后重启

3. 重连 SSH，验证 BBR 是否安装成功

4. 输入 `uname -r`，有 `4.13.0` 以上就表示内核更新成功



## 安装 Shadowsocks 客户端

参考 [番茄食用指南](https://tingtalk.me/fq/) 中的「吃番茄」章节。

## 后话

更多种植番茄的方法，参阅 [科学上网 - 左耳朵](https://haoel.github.io/)。