# GitHub Pages发布指南

本指南将帮助你将数据初步处理网站发布到GitHub Pages上，使其可以通过互联网访问。

## 准备工作

在开始之前，请确保你已经完成以下准备：

1. 拥有一个[GitHub](https://github.com)账号
2. 已安装[Git](https://git-scm.com/downloads)到你的计算机

## 步骤一：创建GitHub仓库

1. 登录你的GitHub账号
2. 点击右上角的"+"图标，选择"New repository"
3. 填写仓库信息：
   - Repository name: 可以使用如"data-processor"这样的名称
   - Description: 简要描述你的项目功能
   - Visibility: 选择"Public"或"Private"（如果选择Private，只有你和授权用户可以看到）
   - 不要勾选"Add a README file"（因为我们已经有自己的README文件了）
4. 点击"Create repository"按钮

## 步骤二：初始化本地Git仓库

打开命令提示符（Windows）或终端（Mac/Linux），执行以下命令：

```bash
# 进入你的项目目录
cd f:\桌面\数据初步处理网站搭建\67f0b534-5c0c-4242-8a8a-b76cb94453a4

# 初始化Git仓库
git init

# 添加所有文件到暂存区
git add .

# 提交更改
git commit -m "Initial commit"
```

## 步骤三：连接GitHub仓库

复制你刚刚创建的GitHub仓库的URL（通常在仓库页面的"Code"按钮下可以找到），然后执行以下命令：

```bash
# 添加远程仓库，将YOUR_USERNAME替换为你的GitHub用户名，REPO_NAME替换为你创建的仓库名
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# 将本地代码推送到GitHub
git push -u origin main
```

如果这是你第一次使用Git，可能需要设置你的用户名和邮箱：

```bash
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub邮箱"
```

## 步骤四：启用GitHub Pages

1. 回到GitHub上你的仓库页面
2. 点击顶部导航栏中的"Settings"选项
3. 在左侧导航栏中找到并点击"Pages"
4. 在"Build and deployment"部分，从"Source"下拉菜单中选择"Deploy from a branch"
5. 从"Branch"下拉菜单中选择"main"分支，然后点击"Save"

## 步骤五：查看发布的网站

1. 保存设置后，GitHub会自动开始构建和部署你的网站
2. 通常需要等待1-2分钟完成部署
3. 部署完成后，你会在GitHub Pages设置页面看到一个绿色的成功提示和你的网站URL
4. 点击这个URL就可以访问你的网站了

## 网站更新

当你修改了项目文件后，需要将更新推送到GitHub以更新网站：

```bash
# 添加所有更改的文件
git add .

# 提交更改
git commit -m "更新内容描述"

# 推送到GitHub
git push
```

推送完成后，GitHub Pages会自动重新构建和部署你的网站，通常在几分钟内完成。

## 常见问题

- **网站无法访问**：确保你已经正确启用了GitHub Pages，并且选择了正确的分支
- **页面显示不完整**：检查文件路径是否正确，特别是HTML、CSS和JavaScript文件之间的引用关系
- **部署失败**：可以在仓库的"Actions"选项卡中查看详细的构建和部署日志

如果遇到其他问题，可以参考[GitHub Pages官方文档](https://docs.github.com/cn/pages)获取更多帮助。