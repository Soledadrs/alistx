<img align="right" width="100" src="https://raw.githubusercontent.com/iosoledad/alistx/main/soledad.png">

# 🛖 Soledad的网盘资源管理站

> 本站旨在分享资源，用作学习交流。

> 使用方式：网页浏览下载、播放、WebDAV 浏览下载、播放。

> 联系方式：[【🐧Telegram】](https://t.me/ifsoledad) 

## 🎤 一、资源介绍

- 各盘总文件粗略大小（截止2022年10月03号持续更新）

|盘符|OnedriveA|OnedriveB|OnedriveC|Pikpak|aliyundrive|待添加|待添加|待添加|待添加|
|-|-|-|-|-|-|-|-|-|-|
|大小（TB）|0.918|0|0|1|27.31|0|0|0|0|

点击每个标题下的 **▶【查看详情】** 展开完整内容。

</details>

## 🚀 五、批量搬运

<details>
  <summary>【查看详情】</summary>

> 使用原始的批量下载工具进行下载也行，不过更推荐认识一下 [Rclone](https://rclone.org/) 。

[Rclone](https://rclone.org/) 是一个支持多种云储存平台、国外云盘、储存协议的命令行工具，兼容 OneDrive 独特的 WebDAV 功能，自行搜索挂载教程。分享资源时登录 OneDrive 网页端，管理资源文件夹的访问权限，赋予同域内空白账户（无任何订阅许可证）为**可查看**权限，即**只读权限**，使用 [Rclone](https://rclone.org/) 配置该空白账户及资源文件夹链接，自动加密空白账户密码，既可共享出来批量搬运资源，又能：限制文件操作权限、避免泄露密码、避免没有创建 API 权限的尴尬、不会出现 refresh token 过期。直接在 [Rclone](https://rclone.org/) 配置文件中填入下述配置，不能再逐步配置，再次配置会导致已被加密后的密码文本被再次加密， [Rclone](https://rclone.org/) 无法识别真实密码报错。配置名 `[rep]` 即为盘符名，在 [Rclone](https://rclone.org/) 中称为 `remote` 。

[Rclone](https://rclone.org/) 还有相对简便易用的图形界面程序 [RcloneBrowser](https://github.com/kapitainsky/RcloneBrowser/releases) ，如果命令行用起来不太顺手可以试试。下载核心程序 [Rclone](https://rclone.org/downloads/) 解压，下载图形界面程序 [RcloneBrowser](https://github.com/kapitainsky/RcloneBrowser/releases)  安装。新建一个 `rclone.conf` 文本文件，将下述配置文件复制进去。在图形程序中，点击左上角 `file` → `preferences` ， `rclone location` 选择解压出的 rclone 核心主程序 `rclone.exe` ， `rclone.conf location` 选择新建的 `rclone.conf` 文件。回到图形程序界面点击左下角 `refresh` 刷新出配置，最后就可以浏览文件批量下载了，在顶部第二行 `Jobs` 中查看传输进程。

- [Rclone](https://rclone.org/) 配置文件

```
[rep]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/pub_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[ani]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/ani_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[mov]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/mov_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[doc]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/doc_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[tlv1]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/tlv_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[tlv2]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/tlv2_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[4k1]
type = webdav
url = https://qimilan-my.sharepoint.com/personal/4k1_2_chirmyram_top/Documents/
vendor = sharepoint
user = share@2.chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[4k2]
type = webdav
url = https://qimilan-my.sharepoint.com/personal/4k2_2_chirmyram_top/Documents/
vendor = sharepoint
user = share@2.chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[4k3]
type = webdav
url = https://qimilan-my.sharepoint.com/personal/4k3_2_chirmyram_top/Documents/
vendor = sharepoint
user = share@2.chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[root]
type = webdav
url = https://al.chirmyram.com/dav/
vendor = other
user = alist
pass = kCJQSyuVJDmwgI0BM60Mtum8VGnI
```

最后一个配置文件由我用 [alist](https://github.com/Xhofe/alist) 自建，其余为 OneDrive 官方，自建远不如微软官方的稳定。 [alist](https://github.com/Xhofe/alist) 挂载网盘后能将已挂载的网盘转化为 WebDAV 服务提供给第三方管理器来浏览文件，由 OneDrive 转化而来的 WebDAV 挂载到第三方后批量搬运不会消耗自建服务器的流量，且访客账号对文件为**只读**权限，即只能读取无法操作，实属理想的公共 WebDAV 服务。更多实现 OneDrive WebDAV 的方式请参考我的博客文章[让 OneDrive 实现 WebDAV 服务](https://www.chirmyram.top/archives/onedrivewebdav) 。 

OneDrive 商业版本身不支持目前通行的 WebDAV 协议，但它确实有比较特殊的 WebDAV 功能。以我的 E5 OneDrive 登录后首页根目录地址为例：
```
https://chirmyram-my.sharepoint.com/personal/pub_chirmyram_top/_layouts/15/onedrive.aspx
```
则其对应的 WebDAV 链接为：
```
https://chirmyram-my.sharepoint.com/personal/pub_chirmyram_top/Documents/
```
观察其特点可发现，将末尾的 `/_layouts/15/onedrive.aspx` 替换为 `/Documents/` 就可以了。末尾 /Documents/ 即为 OneDrive 根目录，也可在其后继续添加子目录。建议分批次少量搬运，否则我修改部分资源的时候会导致搬运任务出错，前功尽弃。两个网盘对拷不会占用本地储存空间，流量还是烧的自己的，而且是双倍流量，可能部分 VPS 商家不会计算进入VPS 的入网流量。

</details>

## 🌟 六、特别推荐

<details>
  <summary>【查看详情】</summary>

酒香还怕巷子深，有部分资源初具规模但体积不够大（同类资源未超过5T），没有独立存放到一个盘上，而是杂七杂八散落在了仓库盘，不方便查找，于是在这里特别推荐。若链接无法访问请在第七章分站中按相同路径查找。

1. [欧路词典库](https://al.chirmyram.com/rep/Doc/%E6%AC%A7%E8%B7%AF%E8%AF%8D%E5%85%B8%E5%BA%93)

共25本英语词典，含离线语音文件，排版精美，与纸质版一致。

2. [音乐](https://al.chirmyram.com/rep/Music)

周杰伦全套 、许嵩全套、部分ACG音乐及其他杂七杂八我喜欢听的歌，能下到无损的均为无损，内嵌专辑封面、歌词。

3. [软件合集](https://al.chirmyram.com/rep/PC/sof)

包含由 [@vposy](https://weibo.com/u/1112829033) 修改的 Adobe 全家桶、 [NextITellYou](https://next.itellyou.cn/) 整站 Windows 官方镜像文件（截止2021-12-21）、[软件安装管家](https://mp.weixin.qq.com/s/3uYhgpRpkfo2hBNhuW-zpw)微信公众号软件目录整套软件（截止21年12月Win版），当然第一部分装机必备里面烂大街的软件没有搬。

</details>

## 📂 七、分站一览

> **✅/🔴  服务器状态实时监控：[https://soledad.vpsl.tk/](https://soledad.vpsl.tk)**

### 1.总盘

- ▶ 1.1 [https://al.chirmyram.com/](https://al.chirmyram.com/) [![](https://img.shields.io/badge/Northflank-brightgreen?&style=flat)](https://northflank.com/) [![](https://img.shields.io/github/stars/Xhofe/alist?style=flat&label=star)](https://github.com/Xhofe/alist) [![](https://img.shields.io/badge/Root-orange?&style=flat)](https://al.chirmyram.com/)

**特别提示：** 网页播放器无法识别内封字幕、不兼容 HEVC 视频编码，需使用挂载到本地播放器或下载后播放。PC 端播放器推荐 [Potplayer](https://potplayer.daum.net/?lang=zh_CN) ，安卓端多媒体播放器推荐 [Nplayer](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/nPlayer_1.7.7.7_191219.apk) ，可显示视频内封字幕、音乐内封歌词；安卓端音乐播放器推荐 [cloudbeats](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/CloudBeats_1.8.4.apk) ，可较快生成播放列表并串流播放，留下的缓存也极小；安卓端电子书阅读器推荐[静读天下](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/Moon_Reader_Pro-v7.0_build_700005-M.apk)，支持多种电子书格式。
- WebDAV 配置参数

|参数|值|
|-|-|
|链接 / URL|https://al.chirmyram.com/dav/|
|主机 / Host|al.chirmyram.com|
|路径 / Path|/dav/|
|协议 / HTTPS|SSL|
|端口 / Port|443|
|账号 / User|alist|
|密码 / Password|alist|

注意：除非相关项目适配浏览器网页端，否则浏览器本身是不支持 WebDAV 协议的。

- ▶ 1.2 [https://om.chirmyram.com/](https://om.chirmyram.com/) [![](https://img.shields.io/badge/Euserv-brightgreen?&style=flat)](https://euserv.com/) [![](https://img.shields.io/github/stars/qkqpttgf/OneManager-php?style=flat&label=star)](https://github.com/qkqpttgf/OneManager-php) [![](https://img.shields.io/badge/Root-orange?&style=flat)](https://om.chirmyram.com/)

- ▶ 1.3 [https://op.chirmyram.com/](https://op.chirmyram.com/) [![](https://img.shields.io/badge/Goorm-brightgreen?&style=flat)](https://ide.goorm.io/)  [![](https://img.shields.io/github/stars/ukuq/onepoint?style=flat&label=star)](https://github.com/ukuq/onepoint) [![](https://img.shields.io/badge/Root-orange?&style=flat)](https://op.chirmyram.com/)

- ▶ 1.4 [https://zf.chirmyram.com/](https://zf.chirmyram.com/) [![](https://img.shields.io/badge/Northflank-brightgreen?&style=flat)](https://northflank.com/) [![](https://img.shields.io/github/stars/zhaojun1998/Zfile?style=flat&label=star)](https://github.com/zhaojun1998/Zfile) [![](https://img.shields.io/badge/Root-orange?&style=flat)](https://zf.chirmyram.com/)

- ▶ 1.5 [https://zf.chirmyram.top/](https://zf.chirmyram.top/) [![](https://img.shields.io/badge/Android-brightgreen?&style=flat)](https://f-droid.org/packages/com.termux/) [![](https://img.shields.io/github/stars/zhaojun1998/Zfile?style=flat&label=star)](https://github.com/zhaojun1998/Zfile) [![](https://img.shields.io/badge/Root-orange?&style=flat)](https://zf.chirmyram.top/)

- ▶ 1.6 [https://oli.chirmyram.top/](https://oli.chirmyram.top/) [![](https://img.shields.io/badge/Android-brightgreen?&style=flat)](https://f-droid.org/packages/com.termux/) [![](https://img.shields.io/github/stars/WangNingkai/OLAINDEX?style=flat&label=star)](https://github.com/WangNingkai/OLAINDEX) [![](https://img.shields.io/badge/Root-orange?&style=flat)](https://oli.chirmyram.top/)

### 2. 仓库盘

- ▶ 2.1 [https://oi.chirmyram.com/](https://oi.chirmyram.com/) [![](https://img.shields.io/badge/Euserv-brightgreen?&style=flat)](https://euserv.com/) [![](https://img.shields.io/github/stars/motao123/oneindex?style=flat&label=star)](https://github.com/motao123/oneindex) [![](https://img.shields.io/badge/Rep-orange?&style=flat)](https://oi.chirmyram.com/)

- ▶ 2.2 [https://cfdrep.chirmyram.com/](https://cfdrep.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/Rep-orange?&style=flat)](https://cfdrep.chirmyram.com/)

- ▶ 2.3 [https://vcrep.chirmyram.com/](https://vcrep.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/Rep-orange?&style=flat)](https://vcrep.chirmyram.com/)

- ▶ 2.4 [https://gl.chirmyram.top/](https://gl.chirmyram.top/) [![](https://img.shields.io/badge/Android-brightgreen?&style=flat)](https://f-droid.org/packages/com.termux/) [![](https://img.shields.io/github/stars/gonelist/gonelist?style=flat&label=star)](https://github.com/gonelist/gonelist) [![](https://img.shields.io/badge/Rep-orange?&style=flat)](https://gl.chirmyram.top/)

- ▶ 2.5 [https://oi.chirmyram.top/](https://oi.chirmyram.top/) [![](https://img.shields.io/badge/Android-brightgreen?&style=flat)](https://f-droid.org/packages/com.termux/) [![](https://img.shields.io/github/stars/motao123/oneindex?style=flat&label=star)](https://github.com/motao123/oneindex) [![](https://img.shields.io/badge/Rep-orange?&style=flat)](https://oi.chirmyram.top/)

### 3. 动画盘

- ▶ 3.1 [https://cfdani.chirmyram.com/](https://cfdani.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/Ani-orange?&style=flat)](https://cfdani.chirmyram.com/)

- ▶ 3.2 [https://vcani.chirmyram.com/](https://vcani.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/Ani-orange?&style=flat)](https://vcani.chirmyram.com/)

### 4. 电影盘

- ▶ 4.1 [https://cfdmov.chirmyram.com/](https://cfdmov.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/Mov-orange?&style=flat)](https://cfdmov.chirmyram.com/)

- ▶ 4.2 [https://vcmov.chirmyram.com/](https://vcmov.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/Mov-orange?&style=flat)](https://vcmov.chirmyram.com/)

### 5. 图书盘

- ▶ 5.1 [https://cfddoc.chirmyram.com/](https://cfddoc.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/Doc-orange?&style=flat)](https://cfddoc.chirmyram.com/)

- ▶ 5.2 [https://vcdoc.chirmyram.com/](https://vcdoc.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/Doc-orange?&style=flat)](https://vcdoc.chirmyram.com/)

### 6. 剧集一盘

- ▶ 6.1 [https://cfdtlv.chirmyram.com/](https://cfdtlv.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/Tlv-orange?&style=flat)](https://cfdtlv.chirmyram.com/)

- ▶ 6.2 [https://vctlv.chirmyram.com/](https://vctlv.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/Tlv-orange?&style=flat)](https://vctlv.chirmyram.com/)

### 7. 剧集二盘

- ▶ 7.1 [https://cfdtlv2.chirmyram.com/](https://cfdtlv2.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/Tlv2-orange?&style=flat)](https://cfdtlv2.chirmyram.com/)

- ▶ 7.2 [https://vctlv2.chirmyram.com/](https://vctlv2.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/Tlv2-orange?&style=flat)](https://vctlv2.chirmyram.com/)

### 8. 4K一盘

- ▶ 8.1 [https://cfd4k1.chirmyram.com/](https://cfd4k1.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/4K1-orange?&style=flat)](https://cfdtlv2.chirmyram.com/)

- ▶ 8.2 [https://vc4k1.chirmyram.com/](https://vc4k1.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/4K1-orange?&style=flat)](https://vctlv2.chirmyram.com/)

### 9. 4K二盘

- ▶ 9.1 [https://cfd4k2.chirmyram.com/](https://cfd4k2.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/4K2-orange?&style=flat)](https://cfdtlv2.chirmyram.com/)

- ▶ 9.2 [https://vc4k2.chirmyram.com/](https://vc4k2.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/4K2-orange?&style=flat)](https://vctlv2.chirmyram.com/)

### 10. 4K三盘

- ▶ 10.1 [https://cfd4k3.chirmyram.com/](https://cfd4k3.chirmyram.com/) [![](https://img.shields.io/badge/CFW_CFP-brightgreen?&style=flat)](https://www.cloudflare.com/zh-cn/) [![](https://img.shields.io/github/stars/vcheckzen/FODI?style=flat&label=star)](https://logi.im/back-end/fodi-on-cloudflare.html) [![](https://img.shields.io/badge/4K3-orange?&style=flat)](https://cfdtlv2.chirmyram.com/)

- ▶ 10.2 [https://vc4k3.chirmyram.com/](https://vc4k3.chirmyram.com/) [![](https://img.shields.io/badge/Vercel-brightgreen?&style=flat)](https://vercel.com/) [![](https://img.shields.io/github/stars/spencerwooo/onedrive-vercel-index?style=flat&label=star)](https://github.com/spencerwooo/onedrive-vercel-index) [![](https://img.shields.io/badge/4K3-orange?&style=flat)](https://vctlv2.chirmyram.com/)
