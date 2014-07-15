# [open.avoscloud.com](http://open.avoscloud.com/)
[![Build Status](https://travis-ci.org/avoscloud/open.svg)](https://travis-ci.org/avoscloud/open)
[![devDependency Status](https://david-dm.org/avoscloud/open/dev-status.svg)](https://david-dm.org/avoscloud/open#info=devDependencies)

这里是 AVOS Cloud 开放的一些与产品本身无关的资源

## 本地搭建烹飪指南（簡易）

```sh
$ git clone git@github.com:avoscloud/open.git
$ bundle install && npm install
$ grunt serve
```

更多資訊請參考 [sparanoid/almace-scaffolding#setup](https://github.com/sparanoid/almace-scaffolding#setup)

## 維護指南

### 增加新条目

1. 在 `./_app/_posts` 下的对应子目录增加新的 `.md` 文件，文件名应符合 `yyyy-mm-dd-title.md` 的格式。

### 更新现有条目

1. 更新 `./_app/_posts` 下的对应 `.md` 文件。如果是重要更新应在文件末尾加注更新内容及日期。
2. 重命名文件以反映最近更新的日期。

### 樣式更新

1. 在 `grunt serve` 激活的情況下編輯 [`./_app/assets/_less/custom.less`](/_app/assets/_less/custom.less)，文件變更後刷新瀏覽器即可實時查看變更

## Licenses

© AVOS Cloud
