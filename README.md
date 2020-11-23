
![Release](https://img.shields.io/github/release/lh1me/hexo-theme-aomori.svg)
![NPM version](https://badge.fury.io/js/hexo.svg)
![Required Node version](https://img.shields.io/node/v/hexo)
![Action](https://github.com/lh1me/hexo-theme-aomori/workflows/Action/badge.svg)
![License](https://img.shields.io/github/license/lh1me/hexo-theme-aomori.svg)

<br/>

![image](https://raw.githubusercontent.com/lh1me/hexo-theme-aomori/master/docs/cover.jpg)

# Aomori

Hexo is a fast, simple, powerful blog framework, with ultra-fast generation speed, support for Markdown, one-click deployment and high scalability. This project is a theme developed based on a series of advantages of Hexo.

- Rich Website Style
- Rich Theme Configuration
- Optimize multimedia playback
- Excellent SEO optimization
- Responsive layout
- Open source and continuously updated
- ...

[中文文档](/README_CN.md) | [CHANGELOG](/CHANGELOG.md)

## Demo

[https://linhong.me](https://linhong.me)


## 安装主题

将 [下载](https://github.com/lh1me/hexo-theme-aomori/releases) 的 ZIP 包解压放置到 Hexo 主题目录下即可

## 开始使用

基本使用配置，需要在全局 `_config.yml` 进行以下设置

1. 启用主题

```
theme: hexo-theme-aomori
```

2. 关闭 Hexo 默认 Highlight 代码高亮

```
highlight:
  enable: false
```

---

## 主题可选功能

主题可选配置，需要在全局 `_config.yml` 进行以下设置

#### 头像

``` yml
aomori_logo: /images/avatar.jpg
```

#### Site Title Animated

``` yml
aomori_logo_typed_animated: true
```

#### Navigation Menu

``` yml
aomori_menu:
  Home: /
  Archives: /archives
```

#### 侧边栏菜单

``` yml
aomori_widgets:
  - toc # 文章导航
  - category  #文章分类
  - tag # 文章标签
  - recent_posts  # 最新文章
  - archive #文章归档
```

#### 知识共享使用许可

``` yml
aomori_copyright: true # or false
```

#### 社交媒体

`icon` 填入 [Boxicons](https://boxicons.com/) Icon Name

`url` 链接地址

``` yml
aomori_social:
  -
    icon:
    type:
    url:
  -
    icon:
    type:
    url:
```

#### 百度链接提交

``` yml
aomori_baidu_sitepush: true  # or false
```

#### 百度统计

``` yml
aomori_baidu_analytics: ''
```

#### Google 统计

``` yml
aomori_google_analytics: 'UA-XXXXX-X'
```

#### 不蒜子 统计

由 [不蒜子](https://busuanzi.ibruce.info/) 提供的计数服务

``` yml
aomori_busuanzi: true
```

---

## 文章可选功能

配置文件：文章 Front-matter

#### 封面图片

使用 `相对路径`，参照 [资源文件夹](https://hexo.io/zh-cn/docs/asset-folders)

``` yml
cover: xxx.jpg
```

#### Cover Video

Use `Full Link` recommend CDN

Each article can only have one cover video, and only one of the cover image and the cover video can exist at the same time.

``` yml
video:
  src: src # Full Video Link
  poster: poster # Full Poster Link
```

#### Article Header Image

可配多张，使用 `相对路径 `，参照 [资源文件夹](https://hexo.io/zh-cn/docs/asset-folders)

``` yml
photos:
- xxx.jpg
- xxx.jpg
```

#### 转载链接

可配多条

`url` 跳转链接 / `title` 显示标题

``` yml
link_reprint:
  -
    url: url
    title: title
  -
    url: url
    title: title
```

#### 参考链接

可配多条

`url` 跳转链接 / `title` 显示标题

``` yml
link_refer:
  -
    url: url
    title: title
  -
    url: url
    title: title
```

#### Top

Install dependencies in the Hexo directory

```
npm i hexo-generator-index -S
```

Add options in the article Front-matter

```
sticky: 100
```

More ways to use [hexo-generator-index](https://github.com/hexojs/hexo-generator-index)

---

## 文章可选风格

配置文件：文章头部

#### Tweet

``` yml
layout: tweet
```

---

## 文章评论

配置文件：全站 `_config.yml`

#### Disqus

填入 Disqus ID

``` yml
aomori_disqus_shortname: ''
```

#### Gitalk

``` yml
aomori_gitalk:
  enable: true
  clientID: GitHub Application Client ID
  clientSecret: GitHub Application Client Secret
  repo: GitHub repo
  owner: GitHub repo owner
  admin: 
    - GitHub repo owner and collaborators
    - GitHub repo owner and collaborators
  distractionFreeMode: true // Facebook-like distraction free mode
```

---

## 页面

#### 友情链接

1. First create the page,

```
hexo new page friends
```

2. Go to `source/friends/index.md`，Set up `Front-matter`

```
title: 友情链接 # 文章标题
layout: friends
comment: true # 是否需要评论 true: 是 false: 否
```

3. Create data, refer to [Data Files](https://hexo.io/zh-cn/docs/data-files)

4. Create `source/_data/friends.json`，The format is as follows

```
[
  {
    "name": "test1",
    "url": "https://linhong.me"
  },
  {
    "name": "test2",
    "url": "https://linhong.me"
  }
  ...
]
```

---

## Search

#### Algolia

1. First create [Algolia](https://www.algolia.com/) Account. After registration is complete, create a new Index, which will be used later.

2. Install [hexo-algolia](https://github.com/oncletom/hexo-algolia)

```
npm install --save hexo-algolia
```

3. Configure Algolia integration to site `_config.yml`:

```
algolia:
    applicationID: 'applicationID'
    apiKey: 'apiKey'
    indexName: '...'
```

4. Run the following command to upload Index data.

```
$ export HEXO_ALGOLIA_INDEXING_KEY=High-privilege API key # Use Git Bash
# set HEXO_ALGOLIA_INDEXING_KEY=High-privilege API key # Use Windows command line
$ hexo clean
$ hexo algolia
```

4. Turn on theme configuration at site `_config.yml`

```
aomori_search_algolia: true
```

Enjoy.

---

# Copyright & License

Copyright (c) 2020 LIN HONG - Released under the [MIT license](LICENSE).