---
title: SYS-KB-00002：输入法配置
description: 在 AOSC OS 桌面环境下配置输入法
published: true
date: 2020-08-10T13:03:24.142Z
tags: 
editor: undefined
---

在 AOSC OS，你可以选用下面的三种输入法框架的任意一种：

- [Fcitx](https://fcitx-im.org/)（Flexible Input Method Framework）。
- [IBus](https://github.com/ibus/ibus/wiki)（Intelligent Input Bus）。
- [SCIM](https://github.com/scim-im)（Smart Common Input Method）。

# 安装一个输入法框架

要安装一个输入法框架和输入方案插件，使用 `sudo apt install` 安装下面任意一个软件包即可：

> Fcitx 5 仍在开发中，如果你希望抢先预览，可以安装 `fcitx5*`。安装 `fcitx-base` 将得到 Fcitx 4。
{.is-info}


- Fcitx，`fcitx-base`。
- IBus，`ibus-base`。
- SCIM，`scim-base`。

# 激活输入法框架

要为当前用户设置默认的输入法框架，使用**当前用户**的身份运行下面的命令：

```
$ imchooser ${IM}
```

`${IM}` 可以被替换为下面的值：

- `fcitx`，指代 Fcitx 4。
- `fcitx5`，指代 Fcitx 5。
- `ibus`，指代 IBus。
- `scim`，指代 SCIM。

你可能需要注销并重新登录以使改动生效。
