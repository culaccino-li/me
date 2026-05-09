# Kaijuan Li · Personal Homepage

这是李凯娟的个人学术主页，一个小而完整的线上名片。

它用来放置我的研究兴趣、论文与工作论文、田野经历、学术报告、简历摘要，以及中英文两个版本的个人介绍。

## 在线访问

- English: https://culaccino-li.github.io/me/
- 中文版: https://culaccino-li.github.io/me/cn.html

## 这个主页里有什么

- 一张正式头像
- 中英文个人简介
- 研究方向与关键词
- Publications / Working Papers
- Fieldwork & Practice
- Talks
- 简历摘要
- 中英文切换
- 适合搜索和社交分享的页面信息

## 日常怎么更新

大多数时候，只需要改这两个文件：

```text
index.html    # 英文页
cn.html       # 中文页
```

如果换头像，就替换：

```text
assets/portrait.jpg
```

如果只是改内容，不需要安装任何东西，也不需要跑复杂命令。打开文件，找到对应文字，改掉，再本地预览即可。

## 什么时候值得更新

有这些变化时，就可以来更新一下：

- 新论文、新工作论文、新会议报告
- 获奖、项目入选、田野或实践项目结项
- 研究方向表述变得更清楚了
- CV 或个人身份信息发生变化
- Google Scholar、ORCID、GitHub 等链接准备好了
- 头像想换得更正式一点

一个轻松的节奏是：每月看一眼，每学期整理一次，重要节点马上更新。

## 发布到线上

修改完成后，在项目目录运行：

```bash
git status
git add index.html cn.html assets README.md UPDATE_GUIDE.md
git commit -m "Update homepage"
git push origin main
```

推送后等一小会儿，GitHub Pages 会自动更新。

## 维护说明

更详细的更新清单、发布流程和频率建议在这里：

[UPDATE_GUIDE.md](UPDATE_GUIDE.md)

这份 README 主要是给自己快速找路用的；真正要认真检查页面时，看更新说明文档就好。
