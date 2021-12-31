---
title: macOS 设置打开应用快捷键
summary: 不使用第三方软件
tags:
- macOS
- applescript
# date: "2019-08-21T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

# image:
#   caption: by大喵
#   focal_point: Smart

links:
#- icon: twitter
#  icon_pack: fab
#  name: Follow
#  url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

share: false
profile: false

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

## 前言

众所周知，Windows 系统下打开文件资源管理器有快捷键 `Win+E`，系统设置有快捷键 `Win+I`，以及大量其他预置快捷键……Ubuntu 系统下同样有海量快捷键可用，例如 `Ctrl+Alt+T` 打开终端，并且由于开源的优势，是高度可定制的。然而一切到了 macOS 这里就拉了胯了……

虽然有很多第三方软件给 macOS 提升体验，但快捷键这个问题其实有一个完全不依赖第三方软件的解决方法 --- macOS 自带的 `自动操作` 应用。结合简单的 applescript 脚本即可。作为强迫症还是要追求一下解决方法的普适性的（

## 教程

### 1.打开自动操作应用

![](iShot2021-12-31-1.png)
