
title: 快速入门
---

我们通过一个简单的一对一视频通话示例来说明 Video SDK 的用法。[前往快速入门](https://github.com/WildDogTeam/video-demo-web-conversation)

<div class="env">
    <p class="env-title">环境准备</p>
    <ul>
        <li> Chrome 49及以后、Firefox 47及以后、Safari 7及以后浏览器 </li>
    </ul>
</div>

## 1. 创建应用

首先，在控制面板中创建应用。

<img src='/images/video_quickstart_create.png' alt="video_quickstart_create">

## 2. 开启匿名登录

应用创建成功后，进入 管理应用-身份认证-登录方式，开启匿名登录。

<img src='/images/openanonymous.png' alt="video_quickstart_openanonymous">

## 3. 开启实时视频通话

进入 管理应用-实时视频通话，开启视频通话功能。此处注意记下配置页面的`VideoAppID`

<img src='/images/video_quickstart_openVideo.png' alt="video_quickstart_openVideo">

## 4. 启动本地 Web 服务

启动本地 Web 服务，建立 HTTPS 环境。快速入门中采用 Node.js 搭建本地服务，用户**也可以使用其他方式**启动本地 Web 服务。

<blockquote class="warning">
  <p><strong>注意：</strong></p>
  只有通过 HTTPS 服务加载的页面才可以成功获取本地摄像头和麦克风等资源，正常运行快速入门。
</blockquote>

使用 Node.js 开启本地 Web 服务：

```javascript
node https_channel_server.js
```

## 5. 运行快速入门

本地 Web 服务启动后，访问 [https://127.0.0.1:8080](https://127.0.0.1:8080) 就会看到快速入门页面。

<img src='/images/video_quickstart_js_login1.png' alt="video_quickstart_js_login">

## 6. 登录

输入`VideoAppID`

<img src='/images/video_quickstart_videoappid.png' alt="video_quickstart_videoappid">

输入`SyncAppID`，（ 地址栏 `wilddogio` 之前的字段），然后点击匿名登录（推荐使用非匿名登录方式）

<img src='/images/video_quickstart_js_syncAppId.png' alt="video_quickstart_js_syncAppId">

## 7. 邀请他人加入

在其它 PC 端（或在同一 PC 中打开当前浏览器的隐身窗口，注意：同一 PC 端的不同浏览器不能共用摄像头和麦克资源）再次访问[https://127.0.0.1:8080](https://127.0.0.1:8080)，输入同一应用 ID 并登录，然后邀请列表中的用户。
<img src='/images/video_quickstart_web_userList.png' alt="video_quickstart_createApp">

## 8. 接受邀请

被邀请人会受到邀请提示，点击确认加入，视频通话建立。

<img src='/images/video_quickstart_web_invite.png' alt="video_quickstart_createApp">

接受邀请后，等待视频通话建立成功。

<img src='/images/video_quickstart_wen_conversation.png' alt="video_quickstart_createApp">

更多详细信息请见 [完整指南](/video/Web/guide/core.html) 和  [API 文档](/video/Web/api/wilddogVideo.html)。
