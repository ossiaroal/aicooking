# V-Cook 厨房AI助手 GitHub部署指南

本指南将帮助您将V-Cook厨房AI助手部署到GitHub Pages，使其可以在线访问。

## 步骤1：创建GitHub账号

如果您还没有GitHub账号，请前往 [GitHub官网](https://github.com/) 注册一个账号。

## 步骤2：创建新仓库

1. 登录GitHub账号
2. 点击右上角的"+"图标，选择"New repository"
3. 填写仓库名称，例如："v-cook-assistant"
4. 添加描述（可选）："V-Cook 厨房AI助手 - 智能烹饪指导应用"
5. 选择"Public"（公开）
6. 勾选"Initialize this repository with a README"
7. 点击"Create repository"按钮

## 步骤3：上传文件

### 方法一：使用GitHub网页界面

1. 在新创建的仓库页面，点击"Add file" > "Upload files"
2. 将以下文件拖拽到上传区域：
   - `v-cook-assistant.html`
3. 在"Commit changes"区域添加提交信息："初始上传V-Cook厨房AI助手"
4. 点击"Commit changes"按钮

### 方法二：使用Git命令行（推荐）

1. 在本地计算机上安装Git（如果尚未安装）：[下载Git](https://git-scm.com/downloads)
2. 打开命令提示符或PowerShell
3. 导航到包含V-Cook助手文件的文件夹：
   ```
   cd "d:\Trae\新建文件夹"
   ```
4. 初始化Git仓库：
   ```
   git init
   ```
5. 添加远程仓库（替换`YOUR_USERNAME`为您的GitHub用户名）：
   ```
   git remote add origin https://github.com/YOUR_USERNAME/v-cook-assistant.git
   ```
6. 添加文件到暂存区：
   ```
   git add v-cook-assistant.html
   ```
7. 提交更改：
   ```
   git commit -m "初始上传V-Cook厨房AI助手"
   ```
8. 推送到GitHub：
   ```
   git push -u origin master
   ```

## 步骤4：启用GitHub Pages

1. 在GitHub仓库页面，点击"Settings"
2. 滚动到"GitHub Pages"部分
3. 在"Source"下拉菜单中选择"master branch"
4. 点击"Save"按钮
5. 等待几分钟，GitHub Pages将被激活

## 步骤5：访问您的在线V-Cook助手

部署完成后，您可以通过以下URL访问您的V-Cook厨房AI助手：

```
https://YOUR_USERNAME.github.io/v-cook-assistant/v-cook-assistant.html
```

将`YOUR_USERNAME`替换为您的GitHub用户名。

## 注意事项

1. **API密钥安全**：请注意，如果您在代码中硬编码了API密钥，它们将在公开仓库中可见。建议使用环境变量或其他安全方法存储敏感信息。

2. **更新应用**：要更新应用，只需重复步骤3，上传新版本的文件即可。

3. **自定义域名**：如果您拥有自己的域名，可以在GitHub Pages设置中配置自定义域名。

4. **本地测试**：在部署前，建议在本地使用浏览器打开HTML文件进行测试，确保所有功能正常工作。

## 故障排除

- 如果页面显示404错误，请确保文件名和路径正确，并且GitHub Pages已成功激活。
- 如果AI功能不工作，请检查浏览器控制台中的错误信息，并确保API密钥和配置正确。
- 如果遇到CORS（跨域资源共享）问题，可能需要调整API调用方式或使用代理服务。

祝您部署顺利！如有任何问题，请参考[GitHub Pages文档](https://docs.github.com/en/pages)或在GitHub社区寻求帮助。