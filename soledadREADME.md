<img align="left" width="100" src="https://cdn.jsdelivr.net/gh/iosoledad/alistx@main/hanke.gif">

# 🛖  🏡 Soledadの电影屋

<img align="right" width="100" src="https://cdn.jsdelivr.net/gh/iosoledad/alistx@main/%E5%BE%AE%E4%BF%A1%E8%B5%9E%E8%B5%8F%E7%A0%81.png">

<details>
  <summary>【点我查看详情】</summary>

> 本站旨在分享资源，用作学习交流。

> 使用方式：网页浏览下载、播放，WebDAV 挂载浏览下载同埋播放。

> 联系方式：[【🐧Telegram】](https://t.me/soledaday)[【🐧Telegram-bot】](https://t.me/Ifsoledad_bot)

### 1. 微信赞赏码：

![微信赞赏码](https://cdn.jsdelivr.net/gh/iosoledad/alistx@main/%E5%BE%AE%E4%BF%A1%E8%B5%9E%E8%B5%8F%E7%A0%81.png)

## 🎤 一、资源介绍

点击每个标题下嘅 **▶【查看详情】** 展开完整内容。

<details>
  <summary>【点我查看详情】</summary>

>- 各盘总文件粗略大小（截止2022年11月01号更新）

|盘符|OD-A|OD-B|GD-个人盘|GD-soledad团队盘|PikPak|AliyunDrive|
|-|-|-|-|-|-|-|
|大小（TB）|1.361|1.361|很多T|很多T|1|27.31|0|0|0|

</details>

### 🚀 二、批量搬运

<details>
  <summary>【点我查看详情】</summary>

- [Rclone](https://soledad.me) 配置文件

```
[OnedriveA]
type = webdav
url = https://ifsoledad-my.sharepoint.com/personal/ifsoledad/Documents/
vendor = sharepoint
user = 暂无
pass = 暂无
```

```
[OnedriveB]
type = webdav
url = https://ifsoledad-my.sharepoint.com/personal/ifsoledad/Documents/
vendor = sharepoint
user = 暂无
pass = 暂无
```

```
[Pikpak]
type = webdav
url = https://ifsoledad-my.sharepoint.com/personal/ifsoledad/Documents/
vendor = sharepoint
user = 暂无
pass = 暂无
```

```
[aliyundrive]
type = webdav
url = https://ifsoledad-my.sharepoint.com/personal/ifsoledad/Documents/
vendor = sharepoint
user = 暂无
pass = 暂无
```

</details>

#### 📂 三、服务器运行一览
<details>
  <summary>【点我查看详情】</summary>

> **✅/🔴  服务器状态实时监控：[https://soledad.vpsl.tk/](https://soledad.vpsl.tk)**

##### 配置注意事项

**特别提示：** 网页播放器无法识别内封字幕、不兼容 HEVC 视频编码，需使用挂载到本地播放器或下载后播放。PC 端播放器推荐 [Potplayer](https://potplayer.daum.net/?lang=zh_CN) ，安卓端多媒体播放器推荐 [Nplayer](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/nPlayer_1.7.7.7_191219.apk) ，可显示视频内封字幕、音乐内封歌词；安卓端音乐播放器推荐 [cloudbeats](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/CloudBeats_1.8.4.apk) ，可较快生成播放列表并串流播放，留下的缓存也极小；安卓端电子书阅读器推荐[静读天下](https://al.chirmyram.com/rep/Android/%E8%B0%B7%E6%AD%8C%E5%95%86%E5%BA%97/Moon_Reader_Pro-v7.0_build_700005-M.apk)，支持多种电子书格式。
- WebDAV 配置参数

|参数|值|
|-|-|
|链接 / URL|https://soledad.me/dav/|
|主机 / Host|https://soledad.me|
|路径 / Path|/dav/|
|协议 / HTTPS|SSL|
|端口 / Port|5244|
|账号 / User|guest|
|密码 / Password|guest|

注意：除非相关项目适配浏览器网页端，否则浏览器本身是不支持 WebDAV 协议的。
