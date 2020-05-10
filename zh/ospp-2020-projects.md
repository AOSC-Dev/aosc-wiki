---
title: 开源软件供应链点亮计划暑期 2020 项目
description: 
published: true
date: 2020-05-08T08:47:06.372Z
tags: ospp
---

欢迎！以下是 AOSC 提供的可供参与的项目主题。你可以从中挑选并联系项目导师，也可以在社区 IRC、Telegram 群组或邮件列表（随意）中和我们讨论你感兴趣的话题。

# 发行版构建自动化

社区主要项目 AOSC OS 的一部分构建过程仍然依赖手工操作。即使大部分繁杂的工作已经能为数个社区项目很好地完成，AOSC OS 仍然面临着社区人手严重不足而带来的更新速度不足及潜在质量缺陷问题。于是我们希望建立一套切合社区实际情况的，能将发行版构建 95% 的操作自动化的基础设施来解决上述问题，以求 AOSC OS 的可持续发展。

_（请补充更多描述）_

- 项目难度：高 _（请再三确认工作量在三个月以内）_
- 项目社区导师：
- 导师联系方式：
- 项目产出要求：
  - _（请补充）_
- 项目技术要求：
  - 了解 Linux 发行版的从头构建，例如 [Linux From Scratch][lfs]
  - 熟悉至少一门编程语言，Python 3 更佳（这是开发主要语言）
  - _（请补充）_
- 相关的仓库：
  - https://github.com/AOSC-Dev/aoinb （自动化项目主仓库）
  - https://github.com/AOSC-Dev/ciel （基于 Systemd 容器和 Overlayfs 的容器化构建设施）
  - https://github.com/AOSC-Dev/acbs （使用构建定义树的构建设施）
  - https://github.com/AOSC-Dev/autobuild3 （使用单个软件包构建定义的构建设施）

[lfs]: http://www.linuxfromscratch.org/lfs/

# 安装程序 DeployKit 的实现

社区项目 [DeployKit][dk] 是未来 AOSC OS 的安装和恢复程序。该程序有两种模式：

1. 作为安装向导指引用户正确地安装 AOSC OS；
2. 作为恢复向导指引用户在轻微的系统配置错误中恢复系统；

目前，DeployKit 使用 [GTK][gtk] 3 和 [Vala 编程语言][vala]基本实现了安装向导的图形用户界面，但尚未实现安装向导的实际操作部分（即 DeployKit 还只是个“空壳”）。本项目的目标是按照社区提供的 [AOSC OS 安装指引][inst-guide]，将这部分原本需要手动操作的安装流程实现到 DeployKit 上。

- 项目难度：低
- 项目社区导师：黎民雍（以俊德）
- 导师联系方式：lmy441900@aosc.xyz
- 项目产出要求：
  - 实现 DeployKit 的系统安装部分
  - 实现安装过程在图形用户界面上的可视化（进度展示）
- 项目技术要求：
  - 了解基本的 Linux 命令
  - 了解 Vala 或其类似编程语言，如 C# 和 Java
  - 了解 GObject、GLib 和 GTK 编程
- 相关的仓库：
  - https://github.com/AOSC-Dev/DeployKit

[dk]: https://github.com/AOSC-Dev/DeployKit
[gtk]: https://www.gtk.org/
[vala]: https://wiki.gnome.org/Projects/Vala
[inst-guide]: /sys-installation-amd64

# 自由及开源软件中文本地化工作

_（请补充更多描述）_

- 项目难度：低
- 项目社区导师：
- 导师联系方式：
- 项目产出要求：
  - _（请补充）_
- 项目技术要求：
  - 从事过软件“汉化”工作，或有科技文本翻译经验
  - 了解一般自由及开源软件进行国际化的方法，如 [GNU Gettext][gettext]
  - _（请补充）_
- 相关的仓库：
  - https://github.com/AOSC-Dev/translations

[gettext]: http://www.gnu.org/software/gettext/

---

以下内容由主办方提供

# 说明

1. 项目设置说明
   - 项目难度分为高、中、低三档，对应税前奖金分别为高（12000 元）、中（9000 元）、低（6000 元）。
   - 难度分级由社区导师根据项目任务自行决定。难度参考标准：  
     - 高：奖金 12000
       - 目标：能力相当于编程能力很强的计算机专业的研究生
       - 典型高难度是优化类的工作，提高时间、降低内存占用、提供性能等。
     - 中：奖金 9000
       - 目标：能力相当于研一、研二计算机专业的学生
     - 低：奖金 6000
       - 目标：能力相当于大三、大四计算机专业的学生
     - 注：以上奖金额度为税前金额。
2. 项目类别说明
   “暑期2020” 活动优先支持开发类项目，同时兼顾各类有利于社区发展的项目，例如，技术文档汉化等，非开发类项目预估总占比不超过 20%
3. 项目奖励说明
   项目奖金分 2 笔发放：中期达标 50%，最终结果分通过或不通过，由主办方和社区导师根据实际项目完成程度和完成质量评判给出。
4. 项目参与人限制说明  
   - 每个项目最终确定唯一一位学生作为中选者参与开发
   - 建议每位社区导师负责的项目任务不超过 3 个
5. 项目成果相关知识产权说明  
   学生在中选后相关的开发工作，需满足提供该项目社区的规定，具体要求由该社区负责在社区活动页面说明，例如要求学生签订 CLA、申明对应的成果的开源协议等
6. 项目信息说明  
   社区除需要收集汇总项目清单及详细信息提交给“暑期2020”工作组外，还需要提供本社区的介绍信息（见社区信息），用于活动的统一宣传。

# 项目任务示例

**说明**：**为便于学生理解，建议项目详情至少要有中文描述**

注意：下面的“精简版的树莓派镜像”只是一个例子，不是真实需求。请把需求写在示例后面。所有项目需求中，都需要留下有效的联系方式（姓名+邮箱）。

1. 项目标题：精简版的树莓派镜像
2. 项目描述：树莓派（英语：Raspberry Pi）是基于 Linux 的单片机电脑，目的是以低价硬件及自由软件促进学校的基本计算机科学教育。树莓派需要刷写文件系统镜像来实现启动，镜像文件常常都较大，不利于快速分发和安装，本项目目标是实现一个小于 NNN MB 的树莓派镜像，并能够通过 DNF 安装软件源中更多的软件进来。
3. 项目难度：高
4. 项目社区导师：姓名 或 ID
5. 导师联系方式：电子邮箱
6. 合作导师联系方式（选填）：ID或姓名，电子邮箱
7. 项目产出要求：
   - 小于 NNN MB 的树莓派镜像，该镜像可刷写在树莓派 Pi 4 上
   - 镜像中版本号信息
   - 镜像支持 DNF 安装软件源中的软件
8. 项目技术要求：
   - 基本的 Linux 命令
   - DNF/RPM 包管理
   - 具备一种脚本语言，如 Python、Bash script 等
   - 压缩算法
9. 相关的开源软件仓库列表：
   - https://gitee.com/openeuler/raspberrypi
   - https://gitee.com/openeuler/raspberrypi-kernel