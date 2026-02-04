# 如何将网站发布到 GitHub Pages / How to Publish the Website to GitHub Pages

[English](#english) | [中文](#chinese)

---

<a name="chinese"></a>
## 中文说明

### 快速开始

本仓库已经配置了 GitHub Actions 工作流，可以自动将 Jekyll 网站部署到 GitHub Pages。

#### 启用 GitHub Pages 的步骤：

1. **转到仓库设置**
   - 在 GitHub 上打开您的仓库 `cybericha/WACV`
   - 点击 `Settings`（设置）标签

2. **配置 Pages**
   - 在左侧边栏中，点击 `Pages`
   - 在 "Source"（源）部分下：
     - 选择 `GitHub Actions` 作为部署源

3. **触发部署**
   - 工作流会在您推送到 `main` 分支时自动运行
   - 您也可以在 `Actions` 标签中手动触发工作流

4. **访问您的网站**
   - 部署完成后，您的网站将在以下地址可用：
   - `https://cybericha.github.io/WACV/`

### 本地预览

在提交更改之前，您可以在本地预览网站：

```bash
# 安装依赖
bundle install

# 启动 Jekyll 服务器
bundle exec jekyll serve

# 访问 http://localhost:4000/WACV/
```

### 文件说明

- `index.md` - 网站主页
- `_config.yml` - Jekyll 配置文件
- `.github/workflows/pages.yml` - GitHub Pages 部署工作流
- `_layouts/` - 页面布局模板
- `_includes/` - 可重用的页面组件
- `assets/` - 静态资源（图片、CSS、JS 等）

---

<a name="english"></a>
## English

### Quick Start

This repository is configured with a GitHub Actions workflow to automatically deploy the Jekyll site to GitHub Pages.

#### Steps to Enable GitHub Pages:

1. **Go to Repository Settings**
   - Open your repository `cybericha/WACV` on GitHub
   - Click on the `Settings` tab

2. **Configure Pages**
   - In the left sidebar, click on `Pages`
   - Under the "Source" section:
     - Select `GitHub Actions` as the deployment source

3. **Trigger Deployment**
   - The workflow will automatically run when you push to the `main` branch
   - You can also manually trigger the workflow from the `Actions` tab

4. **Access Your Website**
   - After deployment completes, your website will be available at:
   - `https://cybericha.github.io/WACV/`

### Local Preview

You can preview the site locally before committing changes:

```bash
# Install dependencies
bundle install

# Start Jekyll server
bundle exec jekyll serve

# Visit http://localhost:4000/WACV/
```

### File Structure

- `index.md` - Main homepage
- `_config.yml` - Jekyll configuration
- `.github/workflows/pages.yml` - GitHub Pages deployment workflow
- `_layouts/` - Page layout templates
- `_includes/` - Reusable page components
- `assets/` - Static assets (images, CSS, JS, etc.)

### Workflow Details

The deployment workflow (`.github/workflows/pages.yml`) performs the following steps:

1. **Build**: Builds the Jekyll site using Ruby and Bundler
2. **Upload**: Uploads the built site as an artifact
3. **Deploy**: Deploys the artifact to GitHub Pages

The workflow is triggered on:
- Push to `main` branch
- Manual trigger via GitHub Actions UI

### Troubleshooting

**Issue**: Deployment fails
- Check the Actions tab for error details
- Ensure GitHub Pages is enabled in Settings > Pages
- Verify that the repository has Pages deployment permissions

**Issue**: Site shows 404 error
- Verify the `baseurl` in `_config.yml` matches your repository name
- Current setting: `baseurl: /WACV`

**Issue**: Styles not loading
- Ensure all asset paths use `{{ site.baseurl }}` prefix
- Example: `{{ site.baseurl }}/assets/css/style.css`

### Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Cayman Theme Documentation](https://github.com/pages-themes/cayman)
