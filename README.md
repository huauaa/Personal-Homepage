# 张华祯个人主页

这是一个不依赖框架的静态个人主页，直接修改 HTML 与 CSS 就可以更新内容。

## 文件夹说明

```text
Personal-Homepage-main/
├─ index.html                         # 页面内容、SEO 信息、百度统计代码
└─ assets/
   ├─ css/
   │  └─ main.css                     # 全部页面样式与手机适配
   └─ images/
      ├─ profile/                     # 个人照片与网站图标
      ├─ publications/
      │  ├─ published/                # 已发表论文图片
      │  └─ submitted/                # 投稿中论文图片
      ├─ projects/                    # 项目和笔记图片
      └─ social/                      # 社交平台分享预览图
```

## 最常见的修改

### 修改个人信息

打开 `index.html`，找到注释“左侧个人信息栏”，修改姓名、学校、地点、邮箱或外部链接。

### 添加最新动态

当前页面没有 Recent News 栏目。需要恢复时，可在 `index.html` 的页脚前新增一个 `content-section`，并在其中加入 `news-list` 与 `news-item`。

### 添加论文

1. 将论文图片放进 `assets/images/publications/published/` 或 `submitted/`。
2. 在 `index.html` 中找到相应栏目。
3. 复制一整段 `publication-card`，修改图片路径、论文标题、期刊和链接。
4. 同时修改栏目右上角的论文数量，例如 `02 publications`。

### 修改颜色和页面宽度

打开 `assets/css/main.css`，优先修改最上方 `:root` 中的变量。样式文件已经按功能分区，并配有中文注释。

## 本地查看

可以直接双击 `index.html`。如果需要更接近线上环境的效果，也可以在项目目录启动任意静态文件服务器。

## 注意事项

- 百度统计代码位于 `index.html` 的 `<head>` 内，请勿删除或更改统计标识。
- 手机端布局在 `assets/css/main.css` 的 `@media (max-width: 860px)` 中维护。
- 投稿中论文目前没有公开链接，因此使用普通卡片展示；有链接后可参考“已发表论文”的写法添加链接。
