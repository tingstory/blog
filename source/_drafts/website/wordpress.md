

## 购买云服务器

阿里云服务器 ECS 一键购买 

- 地域：就近

- 实例规格：1 vCPU 1 GiB (突发性能实例 t5)  高效云盘 40GiB，打开 突发性能实例 无性能约束模式

- 镜像：最新的 CentOS 7.7 64 位（安全加固 ）

- 网络类型：专有网络

- 公网带宽：分配公网 IPv4 地址 - 按固定带宽：1 Mbps

- 购买数量：1 台

- 购买时长：1 年 至 3 年



[SSH登录Linux实例时出现"Disconnected:No supported authentication methods available"错误](https://help.aliyun.com/knowledge_detail/41489.html)

- 打开 [阿里云 ECS 控制台](https://ecs.console.aliyun.com/) -  实例 - [重置实例登录密码](https://help.aliyun.com/document_detail/25439.html)，并重启

- [使用管理终端连接 Linux 实例](https://help.aliyun.com/document_detail/25433.html)：如何粘贴，点击右上角的 `复制命令输入`
	
	- login: root
- Password: 实例登录密码
	
- 执行如下命令，查看 SSH 服务配置

	```
	cat /etc/ssh/sshd_config
	```
	
- 执行如下命令

	```
	vi /etc/ssh/sshd_config 
	```

- 按 i 键编辑 SSH 服务配置文件，将最底部的参数 PasswordAuthentication 设置为 no

	```
	PasswordAuthentication no
	```

- 按 Esc 键退出编辑模式，并输入 `:wq` 保存退出（英文半角冒号）

-  执行如下命令，重启 SSH 服务（或者在实例控制台重启）

	```
	service sshd restart
	```

	



### 连接 VPS

使用 SSH（Secure Shell）客户端可以远程控制你的刚刚购买的云服务器。macOS 用户可以使用苹果电脑自带的终端（Terminal）连接 VPS；Windows 用户可以使用 PuTTY（读 [ˈpʌti] ）连接 VPS。

**下载 PuTTY（3.0 M 左右）**

- 32 位系统：[putty-0.70-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w32/putty-0.73-installer.msi)
- 64 位系统：[putty-64bit-0.70-installer.msi](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.73-installer.msi)



**使用 PuTTY**

- Host Name (or IP address)：输入云服务器的公网 IP 地址（以 44.55.666.777 为例）
- Port：22
- Connection type：SSH
- Save
- Open：弹出 PuTTY Security Alert，选择 `是`
- login as：root
- root@44.55.666.777's Password：复制云服务器的 Password，鼠标右键粘贴（界面上不会显示任何内容），回车。显示 `[root@vultr ~]#` 则代表连接成功（第一次登录的时候，会出现安全警告，单击 `是（Y）`）



**如何快捷登录 PuTTY**

右键 PuTTY 的快捷方式，依次选择「属性」 - 「快捷方式」 - 「目标」 - 在 `"*:\Program Files\PuTTY\putty.exe"` 后面 `空一格` 输入 `root@IP Address -pw "Password"`，完整展示如下：

```
"D:\Program Files\PuTTY\putty.exe" root@44.55.666.777 -pw "FuckGFW"
```





**PuTTY 中如何复制粘贴**

- 要将复制的文本**粘贴**到终端（PuTTY 的 SSH 登录后的界面）里，只需要右键单击就行了
- 要从终端中**复制**文本，只需要用鼠标左键拖拉选中即可












https://www.solagirl.net/


## 域名

- bagflix.com
- passion4bag.com
- backnature.hk


Google Site Kit for Wordpress 已开放下载。这是谷歌为 Wordpress 做的插件，集合 

- 搜索来源分析工具 Search console 
- 流量分析工具 Google Analytics
- 页面加载速度分析 Page speed insight
- 广告联盟 Google Adsense 等

推荐使用 Wordpress的站长尝试。
内容站主题：2020主题



### One Piece

Anime Affiliate



https://onepiecemerchandise.com/

onepiece.gift

onepiecebest.com





## 主题


- avada
- enfold
- bethem
- divi


## 修复

https://www.imzhanghaoyu.com/how-to-protect-wordpress-from-hacker/


https://wpfixit.com/专业修复wp网站的



买sg主机后，上传到根目录的原文件压缩包和解压后的文件夹（内有完整的源码）在部署调试完成后一定要删除。不然，里面的程序得不到升级，又可以被访问，造成漏洞被利用。



## 插件

https://www.hellobar.com/



## 其他


- [Landing Pages](https://www.brizy.cloud/)

方法：替换后面的电话号码，记得加国际电话区号：
https://api.whatsapp.com/send?phone=`8615610241024`


## 参考网站

- Ted: https://universitycustoms.com/
- https://roverove.com/
