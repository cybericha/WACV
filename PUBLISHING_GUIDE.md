# GitHub Pages 发布指南 / GitHub Pages Publishing Guide

## 中文版

### 第一步：启用 GitHub Pages

1. 访问仓库设置页面：https://github.com/cybericha/WACV/settings/pages
2. 在 "Source" 下拉菜单中选择 **GitHub Actions**
3. 保存设置

### 第二步：触发部署

部署会在以下情况自动触发：
- 推送代码到 `main` 分支时
- 或者手动在 Actions 标签页触发

### 第三步：访问您的网站

部署成功后，您的网站将在以下地址可用：

**https://cybericha.github.io/WACV/**

---

## English Version

### Step 1: Enable GitHub Pages

1. Go to repository settings: https://github.com/cybericha/WACV/settings/pages
2. Under "Source" dropdown, select **GitHub Actions**
3. Save the settings

### Step 2: Trigger Deployment

Deployment will automatically trigger when:
- Code is pushed to the `main` branch
- Or manually triggered from the Actions tab

### Step 3: Access Your Website

After successful deployment, your website will be available at:

**https://cybericha.github.io/WACV/**

---

## 技术细节 / Technical Details

### 已配置的文件 / Configured Files

- ✅ `.github/workflows/pages.yml` - GitHub Pages 部署工作流 / Deployment workflow
- ✅ `_config.yml` - Jekyll 配置 / Jekyll configuration
- ✅ `index.md` - 网站主页 / Homepage
- ✅ `.gitignore` - 忽略构建文件 / Ignores build artifacts

### 工作流功能 / Workflow Features

1. 自动构建 Jekyll 网站 / Automatic Jekyll site build
2. 上传构建产物 / Upload build artifacts  
3. 部署到 GitHub Pages / Deploy to GitHub Pages
4. 支持手动触发 / Manual trigger support

### 更多信息 / More Information

详细说明请查看：See detailed instructions:
📄 [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md)
