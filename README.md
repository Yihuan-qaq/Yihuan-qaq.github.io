# Yihuan Huang — Academic Homepage

个人学术主页 + 研究博客,基于 GitHub Pages 的 Jekyll 静态站点。

设计主题:**「取证证据册」**(Forensic Case File)——纸墨配色 + 荧光笔批注 + 证据编号标签,
突出作者在多媒体安全/深度伪造检测领域的研究个性。

## 快速开始

### 本地预览(需 Ruby)

```bash
gem install bundler
bundle install
bundle exec jekyll serve
# 打开 http://localhost:4000
```

> 提示:若本地缺 ruby-dev 导致原生扩展编译失败,可直接依赖 GitHub Pages 在线构建,
> 或在任意 Markdown/静态服务器预览 `preview.html`(自包含的单文件预览)。

### 部署到 GitHub Pages

1. 把本项目文件推送到 `https://github.com/Yihuan-qaq/Yihuan-qaq.github.io`
2. 仓库 Settings → Pages → Source 选择 `main` 分支 / root
3. GitHub Pages 会自动用 Jekyll 构建

## 内容管理

所有论文数据都在 **`_data/publications.yml`**(单一数据源),改论文不用动模板:

```yaml
categories:
  - id: speech-deepfake
    name_en: Speech Deepfake Detection
    name_zh: 语音深度伪造检测
    papers:
      - title: "..."
        authors: "Y. Huang, ..."
        venue: "IEEE TIFS"
        year: 2025
        type: journal          # journal | conference | preprint | chinese-journal
        role: first-author     # first-author | co-author
        tags: [adversarial]
        url: "https://..."
        highlight: "一句话研究亮点(荧光笔高亮显示)"
```

其他数据:

- **`_data/timeline.yml`** — 学术轨迹时间轴
- **`_posts/`** — 博客文章(文件名 `YYYY-MM-DD-title.md`),会自动出现在首页 Blog 区

## 自定义

- **配色 / 字体**:`assets/css/main.css` 顶部的 `:root` tokens
- **头像**:替换 `images/hyh.JPG`
- **导航**:`_layouts/default.html` 的 `.nav-links`

## 目录结构

```
_config.yml          # 站点配置
Gemfile              # Jekyll 依赖
index.html           # 首页(含所有区块)
_layouts/            # 页面布局
_includes/icon.html  # 内联 SVG 图标
_data/               # 论文 / 时间轴数据
_posts/              # 博客文章
assets/css/main.css  # 全部样式
preview.html         # 自包含单文件预览(可直接双击打开)
```
