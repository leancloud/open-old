---
layout: post
title: 代码分支管理指南
category: guide
lang: zh
---

## 介绍

这是我们团队的 Git 分支管理规范。每个人对工具的使用往往各有偏好，各种方法各有利弊，无所谓对错。但涉及团队协作的方面需要有一些一致的规范，所以请大家务必遵守。

除了一致性之外，这个规范的目的是以下几点：

- 确保可以轻易确定特定时间发布或运行的版本。在新发布的程序存在重大缺陷时，可以尽快 rollback 到上一个稳定版本。
- 在需要修复紧急 bug 并尽快发布时，可以只发布必要的 bugfix 而不同时发布还不应发布的其他改动。

## branch 和 tag

每个官方的 repo（`leancloud/` 下的都是官方 repo）有且仅有以下的 branch 和 tag。

Branch: `master` 和 `release`。其中 `master` 对应目前的开发分支，所有的 pull request 都应该发到这个分支。`release` 是当前发布的分支，在这个分支只能增加从 `master` cherrypick 过来的 commit。详见本文后面的说明。

Tag: 对应每个发布版本的 tag。SDK 和应用程序的 tag 遵照 `<major>.<minor>.<patch>` 的命名，如 `2.5.1`；服务端程序的 tag 以发布的日期命名，如 `2014.11.13`，如果有 bugfix，则在后面增加小写字母，如 `2014.11.13` 后是 `2014.11.13a`，然后是 `2014.11.13b`。

目前还有部分 repo 包含多个独立部署的项目（如 `uluru-platform`）。在这样的 repo 打 tag 时需要附上项目名做前缀，如 `bigquery-2.5.1`。但我们需要逐步把这些项目拆分到独立的 repo。

## 发布新版流程

- 确保所有要发布的 pull request 都已经 merge 到 `master`；
- 使用 `master` branch 的代码进行测试，如果发现 bug，把对应的 bugfix merge 到 `master`；
- 删除旧的 `release` branch，并从当前的 `master` 创建新的 `release` branch；
- 在 Jenkins 上从 `release` branch 发起新的 build 并发布；
- 发布完成后在当前的 `release` branch 打上对应版本的 tag。

## Bugfix 流程

这里的 bugfix 指的是修复已经发布的程序（`release` branch）中的缺陷。`master` 里的 bug 请直接 merge bugfix 到 `master`。

- 如果此缺陷在 `master` 中还存在，请先 merge bugfix 到 `master`，否则跳到下一步；
- 在 `release` branch 从 `master` cherrypick 修复该缺陷的一个或多个 commit；
- 在 Jenkins 上发布当前 `release` branch；
- 发布完成后在当前的 `release` branch 打上递增的 tag。比如，如果上一个 tag 是 `2.5.1`，这个 tag 应该是 `2.5.2`；如果上一个是 `2014.11.13`，这个就是 `2014.11.13a`。

## 其他

并不是每个 bug 都有专门发布 bugfix 版的必要，对于不紧急的 bug，可以在 `master` 里 fix 后随下一个版本发布。

在一个官方 repo 下只应该有以上说的 branch 和 tag，在开发过程中使用到的 feature branch 等请都放在个人的 fork，一律通过向 `master` 发 pull request 的方式给官方 repo 提交代码。
