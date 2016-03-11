# [open.leancloud.cn](http://open.leancloud.cn/)
[![Build Status](https://travis-ci.org/leancloud/open.svg)](https://travis-ci.org/leancloud/open)
[![devDependency Status](https://david-dm.org/leancloud/open/dev-status.svg)](https://david-dm.org/leancloud/open#info=devDependencies)
[![Built with Almace Scaffolding](https://d349cztnlupsuf.cloudfront.net/amsf-badge.svg)](http://sparanoid.com/lab/amsf/)

这里是 LeanCloud 开放的一些与产品本身无关的资源

## 本地搭建烹饪指南（简易）

```sh
# Init project
$ git clone git@github.com:leancloud/open.git
$ bundle install && npm install
$ grunt serve

# Update AMSF
$ grunt update

# Release new version
$ grunt release
```

更多资讯请参考 [sparanoid/almace-scaffolding](https://github.com/sparanoid/almace-scaffolding)

## 维护指南

### 增加新条目

在 `./_app/_posts` 下的对应子目录增加新的 `.md` 文件，文件名应符合 `yyyy-mm-dd-title.md` 的格式。

### 更新现有条目

更新 `./_app/_posts` 下的对应 `.md` 文件。如果是重要更新应在文件末尾加注更新内容及日期。

### 样式／脚本自定义

在 `grunt serve` 激活的情况下编辑 [`./_app/assets/_less/user.less`](/_app/assets/_less/user.less) 或 [`./_app/assets/_js/user.js`](/_app/assets/_js/user.js)，文件变更后刷新浏览器即可实时查看变更

### 如何从 Atom feed 中隐藏文章

在该文章的 YAML front-matter 数据中添加如下字段：

```yaml
hidden: true
```

例子请参考 [./_app/_posts/note/2014-07-17-improve-chinese.md](/_app/_posts/note/2014-07-17-improve-chinese.md)

## Licenses

© LeanCloud
