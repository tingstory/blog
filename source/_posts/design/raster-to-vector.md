---

title: Inkscape：位图矢量化的最佳工具    
date: 2019-06-21   
updated: 2019-08-25  
categories: 设计  

tags: 
- 设计
- Inkscape
- 位图矢量化

permalink: raster-to-vector  

---

免费开源的矢量图像编辑器，小巧而强大，强烈推荐设计师人手一份。

<!-- more -->

## 区别

首先看一下「矢量图」和平常我们所见的「位图」有什么区别：

| 项目 | 位图                | 矢量图                     |
| ---- | ------------------- | -------------------------- |
| 别称 | 栅格图、像素图      | 向量图                     |
| 构成 | 由像素（Pixel）组成 | 由数学方程组成（基于路径） |
| 格式 | JPEG、PNG、GIF、PSD | SVG、EPS、AI、DWG          |
| 优点 | 色彩丰富，效果逼真  | 无损缩放、体积小           |
| 缺点 | 放大会变模糊        | 不能真实地还原物理世界     |
| 用途 | 场景复杂的图像      | Logo、插画                 |
| 软件 | Photoshop           | Illustrator、Inkscape      |

位图就好比在（巨大的）沙盘上画好的画，当你远观时，真美。但当你靠得非常近的时候，就能看到细腻多彩的画面是由每粒（颜色不可变化的）沙子组成的。还是没搞懂，请看啃芝士的科普视频：[位图和矢量图有什么区别？为啥图片放大就变模糊了？](https://www.bilibili.com/video/av25573962/)



## 寻找

为了把简单的图像（例如 Logo）矢量化，我尝试过 Adobe Illustrator 的 [图像临摹](https://helpx.adobe.com/cn/illustrator/using/image-trace.html) 和在线图像矢量转换工具 [Autotrace](https://www.autotracer.org/zh.html)，直到遇见 [Inkscape](https://inkscape.org/)，我才停下搜寻的脚步：

- 免费、开源、小巧、无广告
- 全平台适用：支持 [Windows](https://inkscape.org/release/0.92.4/windows/)、[macOS](https://inkscape.org/release/0.92.4/mac-os-x/) 和 [Linux](https://inkscape.org/release/0.92.4/gnulinux/)
- 怎么读：Ink（墨水） + scape（景色）



## 使用

- 双击 `inkscape.exe` 打开
- 打开（`Ctrl + O`）想要矢量化的图片，`确定`
- 选中图片，依次点击菜单栏 `路径` > `临摹位图轮廓`（`Shift + Alt + B`）
- 打开 `即时预览`，选择对应的模式，`确定` 执行临摹
- 效果不满意，「拖走」处于顶层的矢量图，点击原图，修改设定，`确定` 再次矢量化
- 另存为（`Shift + Ctrl + S`）矢量格式
