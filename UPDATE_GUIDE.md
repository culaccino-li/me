# 个人主页更新说明

本文档用于后续维护个人主页时参考，包括更新内容、推荐频率、发布步骤和检查清单。

## 一、什么时候需要更新

建议将主页更新分为三类：即时更新、定期更新和年度整理。

### 1. 即时更新

出现以下变化时，建议尽快更新：

- 新论文发表、接收、投稿状态发生变化
- 工作论文有新标题、新摘要或新版本
- 学术会议报告确认
- 获奖、项目入选、实践项目结项
- 邮箱、GitHub、Google Scholar、ORCID 等链接发生变化
- CV 下载文件更新
- 头像、身份状态或院系信息变化

建议频率：事情发生后 1 周内更新。

### 2. 定期更新

即使没有重大变化，也建议固定检查页面：

- 每月快速检查一次链接和页面显示
- 每学期整理一次研究项目、论文状态和 CV
- 每次申请、会议投稿、博士阶段节点前集中检查一次

建议频率：每月 1 次小检查，每学期 1 次完整整理。

### 3. 年度整理

每年年末或新学年开始前，建议做一次结构性更新：

- 检查 “Last updated” 年月
- 重新排序 publications、talks、fieldwork
- 删除过时或不再重要的条目
- 更新研究方向表述
- 检查 SEO 描述是否还准确
- 检查社交分享图、头像、favicon 是否合适

建议频率：每年 1 次。

## 二、更新哪些文件

常见更新位置如下：

```text
index.html              # 英文内容
cn.html                 # 中文内容
assets/portrait.jpg     # 头像与分享图
assets/favicon.svg      # 网站图标
```

如果只改中文内容，通常只需要改 `cn.html`。

如果只改英文内容，通常只需要改 `index.html`。

如果更新身份、论文、项目、CV 摘要等核心内容，建议中英文两页同步检查。

## 三、内容更新清单

每次更新前后建议检查：

- 姓名、身份、学校、院系是否准确
- 邮箱、GitHub、Scholar、ORCID 是否可点击
- 中英文内容是否一致
- 论文状态是否准确：working paper、published、award、in progress
- 会议名称、年份、地点是否准确
- Fieldwork 与 Talks 是否按时间倒序
- CV 区块是否保留必要信息，避免放太多私人信息
- 页面底部更新时间是否需要修改
- 手机端显示是否正常

## 四、发布步骤

在项目目录执行：

```bash
cd "/Users/kaijuan/Documents/New project"
git status
git add index.html cn.html assets README.md UPDATE_GUIDE.md
git commit -m "Update homepage"
git push origin main
```

如果只修改了一个文件，也可以只添加那个文件：

```bash
git add cn.html
git commit -m "Update Chinese homepage"
git push origin main
```

## 五、发布后检查

推送后等待几十秒到几分钟，然后检查：

- 英文首页：https://culaccino-li.github.io/me/
- 中文页面：https://culaccino-li.github.io/me/cn.html

需要确认：

- 页面能正常打开
- 头像能正常加载
- 中英文切换正常
- tab 切换正常
- Publications 筛选正常
- 摘要展开/收起正常
- 手机浏览器显示正常

如果线上页面没有更新，可以尝试：

- 强制刷新浏览器
- 等待 5 分钟
- 检查 GitHub 仓库的 `Actions` 或 `Settings → Pages`
- 确认 GitHub Pages 发布分支是 `main`，目录是 `/ root`

## 六、SEO 与分享信息维护

页面头部已经包含：

- `meta description`
- Open Graph 信息
- Twitter Card 信息
- favicon
- 中英文 `hreflang`
- canonical 链接

当主页正式绑定自定义域名后，建议将以下内容从相对路径改为完整网址：

```html
<link rel="canonical" href="https://your-domain.com/">
<meta property="og:url" content="https://your-domain.com/">
<meta property="og:image" content="https://your-domain.com/assets/portrait.jpg">
```

中文页也要同步改成对应地址。

## 七、推荐更新频率

建议采用这个节奏：

```text
每月：检查链接、联系方式、页面是否正常访问
每学期：整理论文、项目、报告、CV 摘要
每年：重写一次简介和研究方向，使其匹配当前阶段
重要节点后：立即更新成果、获奖、会议、身份变化
```

对学术主页来说，不需要频繁小修外观；更重要的是让信息准确、稳定、可信。

## 八、维护原则

- 优先保持学术信息准确，而不是追求频繁改版
- 中英文内容要尽量同步
- 不确定是否公开的信息不要放上主页
- 链接没有准备好时，可以先隐藏，避免大量 `#` 占位链接
- 每次上线前至少检查一次手机端显示
- 重大修改前可以先本地打开 `index.html` 与 `cn.html` 预览
