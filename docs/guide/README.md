# 概要

## Anywhere- 是什么？
Anywhere- 是我有一天突然有了灵感并开始着手制作的工具类 App。它支持将你常用的页面 (Activity) 收集到一个界面并保存，方便快速打开。在手机 App 数量繁多的今天，Anywhere- 也许能帮助你节约一些时间，做一些微小的工作。

![Android CI](https://github.com/zhaobozhen/Anywhere-/workflows/Android%20CI/badge.svg)

## Anywhere- 能做什么？
Anywhere- 目前有 3 个工作模式：
- Normal
- Root
- Shizuku

### 1.Normal
此模式无需任何运行时权限，通过[ URL Scheme 协议](https://en.m.wikipedia.org/wiki/Uniform_Resource_Identifier)打开特定页面，也可以通过 Intent 打开 Exported 页面。
- 优点：无需任何运行时权限，可打开指定界面。
[像这样](anywhere://url?param1=alipays://platformapi/startapp?appId=60000002&param2=&param3=) 
[像这样](anywhere://url?param1=orpheus://song/478127&param2=&param3=) 
或者
[像这样](anywhere://url?param1=coolmarket://www.coolapk.com/feed/271681&param2=&param3=)

- 缺点：需要应用支持；不支持所有页面。

[使用方法](/guide/URL-Scheme-Usage.html)

### 2.Root
Root 模式通过使用 ADB 指令打开指定的页面(Activity)。
- 优点：可以打开任何 **Activity** 页面。
[像这样](anywhere://url?param1=com.android.settings&param2=.wifi.WifiSettings&param3=)
或者
[像这样](anywhere://url?param1=tv.danmaku.bili&param2=.MainActivityV2&param3=)

- 缺点：暂时不支持打开 **Fragment**；

[使用方法](/guide/Root-Mode-Usage.html)

### 3.Shizuku
Shizuku 模式可以通过使用 [Shizuku Manager](https://www.coolapk.com/apk/moe.shizuku.privileged.api) 实现无需授予本程序 Root 权限获得与 Root 模式相同的功能。
- 优点：无需授予 Root 权限实现 Root 模式功能。
- 缺点：需要额外下载 Shizuku Manager，Shizuku 需要 Root 模式激活。

[使用方法](/guide/Shizuku-Mode-Usage.html)

## 添加方式
目前有如下几种 Anywhere- 添加方式：
- URL Scheme
- 活动列表
- 扫码合集
- Collector
- 其他应用分享至 Anywhere-

它们分别适用于不用的场景。[查看详情](/guide/Adding-Approach.html)

## 添加 Intent Extras
[使用方法](/guide/Put-Intent-Extras.html)

## 备份与恢复
Anywhere- 提供基础的备份与恢复功能，在 **设置 - 备份和恢复** 页面即可进行操作。

### 1.备份和分享
#### 1.1备份
通过 Document API，Anywhere- 无需读写权限即可完成备份。点击**创建新的备份文件**即可打开**文档**程序，选择保存位置，备份所有的 Anywhere-。

#### 1.2分享配置
点击**分享配置**选项，Anywhere- 会生成一串加密数据。此数据包含所有的 Anywhere-，将其复制后即可分享给其他人。

### 2.恢复和应用
#### 2.1恢复
点击**从存储文件中恢复**选项即可打开**文档**程序，选择备份的 ***.awbackups** 文件，App 提示备份成功后即恢复完成。

#### 2.2应用配置
点击**应用配置**选项，粘贴其他人分享的数据串，点击**确定**，即可应用配置。

## Anywhere- 将要做什么
- 毛玻璃
- 自定义 Page
- Workflow
- ... 
