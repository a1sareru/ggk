# ごがく

基于 Hugo 的日语学习博客。

## 本地开发

### 前置条件

- 安装 [Hugo](https://gohugo.io/installation/)（extended 版本）

### 本地预览

```bash
hugo server -D
```

启动后访问 http://localhost:1313/ggk/ 即可预览站点。`-D` 参数会同时渲染 draft 状态的文章。

### 构建静态文件

```bash
hugo --minify
```

生成的文件位于 `public/` 目录。

## 部署

项目使用 GitHub Actions 自动部署到 GitHub Pages。

### 流程

1. 将代码推送到 `main` 分支
2. GitHub Actions 自动触发（`.github/workflows/deploy.yml`）
3. CI 环境安装 Hugo extended，执行 `hugo --minify` 构建
4. 构建产物发布到 `gh-pages` 分支
5. GitHub Pages 从 `gh-pages` 分支提供服务

### 手动触发

无需手动操作，推送到 `main` 即自动部署。如需本地验证构建结果：

```bash
hugo --minify
# 检查 public/ 目录下的输出
```

## 项目结构

```
content/posts/   - 博客文章（Markdown）
layouts/         - 页面模板
static/          - 静态资源（CSS、音频等）
hugo.toml        - Hugo 配置文件
```
