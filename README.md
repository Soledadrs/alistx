<img align="right" width="240" src="https://gcore.jsdelivr.net/gh/ChirmyRam/ChirmyRam-OneDrive-Repository/odlogo.png">

# 🛖 Soledad的网盘资源管理站

> 本站旨在分享资源，用作学习交流。

> 使用方式：网页浏览下载、播放、WebDAV 浏览下载、播放。

## 🎤 一、资源介绍

- 各盘总文件粗略大小（截止2022年9月25）

|盘符|OnedriveA|OnedriveB|OnedriveC|Pikpak|aliyundrive|待添加|待添加|待添加|待添加|
|-|-|-|-|-|-|-|-|-|-|
|大小（TB）|0.918|0|0|1|27.31|0|0|0|0|

为缩短本页版面，我对文字说明进行了折叠处理，点击每个标题下的 **▶【查看详情】** 展开完整内容。


## 🚀 二、批量搬运

<details>
  <summary>【查看详情】</summary>

> 使用原始的批量下载工具进行下载也行，不过更推荐认识一下 [Rclone](https://rclone.org/) 。

[Rclone](https://rclone.org/) 是一个支持多种云储存平台、国外云盘、储存协议的命令行工具，兼容 OneDrive 独特的 WebDAV 功能，自行搜索挂载教程。分享资源时登录 OneDrive 网页端，管理资源文件夹的访问权限，赋予同域内空白账户（无任何订阅许可证）为**可查看**权限，即**只读权限**，使用 [Rclone](https://rclone.org/) 配置该空白账户及资源文件夹链接，自动加密空白账户密码，既可共享出来批量搬运资源，又能：限制文件操作权限、避免泄露密码、避免没有创建 API 权限的尴尬、不会出现 refresh token 过期。直接在 [Rclone](https://rclone.org/) 配置文件中填入下述配置，不能再逐步配置，再次配置会导致已被加密后的密码文本被再次加密， [Rclone](https://rclone.org/) 无法识别真实密码报错。配置名 `[rep]` 即为盘符名，在 [Rclone](https://rclone.org/) 中称为 `remote` 。

[Rclone](https://rclone.org/) 还有相对简便易用的图形界面程序 [RcloneBrowser](https://github.com/kapitainsky/RcloneBrowser/releases) ，如果命令行用起来不太顺手可以试试。下载核心程序 [Rclone](https://rclone.org/downloads/) 解压，下载图形界面程序 [RcloneBrowser](https://github.com/kapitainsky/RcloneBrowser/releases)  安装。新建一个 `rclone.conf` 文本文件，将下述配置文件复制进去。在图形程序中，点击左上角 `file` → `preferences` ， `rclone location` 选择解压出的 rclone 核心主程序 `rclone.exe` ， `rclone.conf location` 选择新建的 `rclone.conf` 文件。回到图形程序界面点击左下角 `refresh` 刷新出配置，最后就可以浏览文件批量下载了，在顶部第二行 `Jobs` 中查看传输进程。

- [Rclone](https://rclone.org/) 配置文件

```
[OnedriveA]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/pub_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

```
[OnedriveB]
type = webdav
url = https://chirmyram-my.sharepoint.com/personal/ani_chirmyram_top/Documents/
vendor = sharepoint
user = share@chirmyram.top
pass = 25es9-8BHYf1mDzSSaqMPBDAj3JjGh-95bjeWQ
```

</details>


</details>

## 📂 三、服务器运行一览

> **✅/🔴  服务器状态实时监控：[https://soledad.vpsl.tk/](https://soledad.vpsl.tk/)**

**特别提示：** 网页播放器无法识别内封字幕、不兼容 HEVC 视频编码，需使用挂载到本地播放器或下载后播放。PC 端播放器推荐 [Potplayer](https://potplayer.daum.net/?lang=zh_CN) ，安卓端多媒体播放器推荐 [Nplayer](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/nPlayer_1.7.7.7_191219.apk) ，可显示视频内封字幕、音乐内封歌词；安卓端音乐播放器推荐 [cloudbeats](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/CloudBeats_1.8.4.apk) ，可较快生成播放列表并串流播放，留下的缓存也极小；安卓端电子书阅读器推荐[静读天下](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/Moon_Reader_Pro-v7.0_build_700005-M.apk)，支持多种电子书格式。
- WebDAV 配置参数

|参数|值|
|-|-|
|链接 / URL|https://alistx.tk//dav/|
|主机 / Host|alistx.tk|
|路径 / Path|/dav/|
|协议 / HTTPS|SSL|
|端口 / Port|5244|
|账号 / User|admin|
|密码 / Password|OyFyUcg4|

注意：除非相关项目适配浏览器网页端，否则浏览器本身是不支持 WebDAV 协议的。
