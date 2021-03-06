# 极客兔兔的博客

[![github actions](https://github.com/geektutu/geektutu-blog/workflows/public%20blog/badge.svg)](https://github.com/geektutu/geektutu-blog/actions)
  
## 在线阅读

Coding 创建有趣的开源项目，戳：[https://geektutu.com/](https://geektutu.com/)

## 订阅我的博客

最新动态可以关注：知乎 [Go语言](https://www.zhihu.com/people/gzdaijie) 或微博 [极客兔兔](https://weibo.com/geektutu)

订阅方式：右上角 **watch** [geektutu/blog](https://github.com/geektutu/blog) ，每篇文章都能收到邮件通知，或通过 [RSS](https://geektutu.com/feed.xml) 订阅。

**较为完整的系列有：**

- 一篇文章入门系列
  - [一篇文章入门 Python](https://geektutu.com/post/quick-python.html)
  - [一篇文章入门 Go](https://geektutu.com/post/quick-golang.html)
  - [一篇文章入门 Rust](https://geektutu.com/post/quick-rust.html)

- Go 语言
  - [七天用Go从零实现系列](https://geektutu.com/post/gee.html)
  - [Go 语言高性能编程](https://geektutu.com/post/high-performance-go.html)
  - [Go 语言笔试面试题](https://geektutu.com/post/qa-golang.html)

- 机器学习
  - [tensorflow mnist 入门系列](https://geektutu.com/post/tensorflow-mnist-simplest.html)
  - [tensorflow openai 强化学习系列](https://geektutu.com/post/tensorflow2-gym-nn.html)
  - [tensorflow 2.0 文档](https://geektutu.com/post/tf2doc.html)
  
- 经历与感悟
  - [建站经历](https://geektutu.com/post/blog-experience-1.html)
  - [年终总结](https://geektutu.com/post/2020.html)

## 关于 hexo 主题

使用主题 [hexo-theme-geektutu](https://github.com/geektutu/hexo-theme-geektutu)

```bash
yarn install      # 安装依赖模块
yarn update # 下载主题到 themes/geektutu
yarn build  # 将posts的文章拷贝到source目录下的_posts，并执行hexo clean, hexo generate
yarn deploy # 部署到_config.xml中配置的仓库地址
```

如果你使用的是 yarn，将下面的 npm 换成 yarn 即可。

`posts` 目录的存在仅仅是为了博主做博客分类使用， `yarn build` 时会拷贝到 `source/_posts`。
因此， 直接新建 `source/_posts` 目录，并直接在该文件夹下写文章是没有问题的。

可以在 package.json 里的 scripts 部分，定制你自己的 npm/yarn 命令。

本站使用对象存储 + CDN 方式托管在[七牛云](https://marketing.qiniu.com/cps/redirect?redirect_id=4&cps_key=1hetil5x65e8i)

- [账号配置](https://github.com/qiniu/qshell)
- [上传配置](https://github.com/qiniu/qshell/blob/master/docs/qupload.md)

```
qshell user ls
qshell account -- <Your AccessKey> <Your SecretKey> <Your Name>
qshell qupload xxx.conf
```
