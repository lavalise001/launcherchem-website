# LauncherChem 网站部署指南

## 方案A：使用 Vercel 免费部署（推荐）

Vercel 是一个免费的静态网站托管平台，支持自动部署、全球CDN加速，非常适合企业官网。

---

## 📋 部署步骤

### 第一步：注册 GitHub 账号

1. 访问 https://github.com
2. 点击 "Sign up" 注册账号
3. 验证邮箱，完成注册

---

### 第二步：创建 GitHub 仓库

1. 登录 GitHub
2. 点击右上角 "+" → "New repository"
3. 填写信息：
   - **Repository name**: `launcherchem-website`
   - **Description**: LauncherChem official website
   - 选择 **Public**（公开）
   - 勾选 **Add a README file**
4. 点击 "Create repository"

---

### 第三步：上传网站代码

#### 方法1：通过网页上传（简单）

1. 在 GitHub 仓库页面，点击 "Add file" → "Upload files"
2. 将 `launcherchem-website.zip` 解压后的所有文件拖入上传区域
3. 填写提交信息："Initial commit"
4. 点击 "Commit changes"

#### 方法2：使用 Git 命令（推荐）

```bash
# 1. 克隆仓库到本地
git clone https://github.com/你的用户名/launcherchem-website.git
cd launcherchem-website

# 2. 复制网站文件到该文件夹
# 将 launcherchem-website.zip 解压后的内容复制进来

# 3. 提交并推送
git add .
git commit -m "Initial commit"
git push origin main
```

---

### 第四步：注册 Vercel 账号

1. 访问 https://vercel.com
2. 点击 "Sign Up"
3. 选择 "Continue with GitHub"（用GitHub账号登录）
4. 授权 Vercel 访问您的 GitHub 仓库

---

### 第五步：部署网站

1. 登录 Vercel 后，点击 "Add New..." → "Project"
2. 在列表中找到 `launcherchem-website` 仓库，点击 "Import"
3. 配置项目：
   - **Framework Preset**: 选择 "Vite"
   - **Root Directory**: 保持默认 `./`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
4. 点击 "Deploy"

等待约 1-2 分钟，部署完成后会显示：
- 🎉 **Congratulations!** 
- 您的网站地址：https://launcherchem-website.vercel.app

---

### 第六步：绑定自定义域名（可选）

如果您已购买域名（如 launcherchem.com），可以绑定：

1. 在 Vercel 项目页面，点击 "Settings" → "Domains"
2. 输入您的域名，如 `launcherchem.com`
3. 点击 "Add"
4. 按照提示，在域名服务商处添加 DNS 记录：
   - 类型：A 记录
   - 主机：@
   - 值：76.76.21.21
5. 等待 DNS 生效（通常几分钟到几小时）

---

## 🔄 后续更新网站

当您需要修改网站内容时：

1. 修改本地代码
2. 提交到 GitHub：
   ```bash
   git add .
   git commit -m "Update content"
   git push origin main
   ```
3. Vercel 会自动检测更改并重新部署！

---

## 📞 需要帮助？

如果在部署过程中遇到问题，请告诉我具体步骤，我会协助您解决！
