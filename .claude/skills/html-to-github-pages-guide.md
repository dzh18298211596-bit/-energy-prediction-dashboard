# HTML to GitHub Pages Skill 使用说明

## 功能简介

这个skill可以帮您快速将HTML文件部署到GitHub Pages，使其可以通过 `username.github.io/repo-name` 格式在线访问。

## 如何使用

### 方式1：直接调用skill命令

在Claude Code中输入：
```
/html-to-github-pages
```

### 方式2：自然语言触发

您可以说：
- "将我的 index.html 部署到GitHub Pages"
- "把这个HTML文件转为bit.github.io格式"
- "帮我把HTML文件推送到GitHub并启用Pages"
- "将HTML文件转为在线可访问的格式"

## Skill会做什么

1. **检查Git状态**：确认是否已有Git仓库，如没有则初始化
2. **收集信息**：询问您的GitHub用户名、仓库名和HTML文件路径
3. **配置远程仓库**：添加或更新GitHub远程仓库地址
4. **提交文件**：将HTML文件添加到Git并创建提交
5. **创建README**：生成包含访问链接和使用说明的README文件
6. **推送到GitHub**：将所有文件推送到GitHub
7. **提供配置指引**：详细告诉您如何启用GitHub Pages

## 所需信息

使用前请准备：
- ✅ GitHub用户名
- ✅ GitHub仓库名（需要提前在GitHub上创建好仓库）
- ✅ HTML文件路径

## 输出结果

Skill执行完成后会提供：
- ✅ 成功推送的文件列表
- 📦 GitHub仓库URL
- 🌐 预期的GitHub Pages访问URL
- 📋 详细的GitHub Pages启用步骤

## 示例流程

```
用户: 把我的 dashboard.html 转为GitHub Pages格式

Claude:
[执行skill]
- 初始化Git仓库
- 询问GitHub用户名：dzh18298211596-bit
- 询问仓库名：my-dashboard
- 添加并提交 dashboard.html
- 创建README.md
- 推送到GitHub

完成！访问链接：
https://dzh18298211596-bit.github.io/my-dashboard/dashboard.html

请按以下步骤启用GitHub Pages：
1. 访问 https://github.com/dzh18298211596-bit/my-dashboard
2. 点击 Settings → Pages
3. 选择 main 分支
4. 等待1-2分钟部署完成
```

## 注意事项

⚠️ **使用前必须：**
- 在GitHub上创建好目标仓库
- 确保本地已配置Git身份验证（SSH密钥或令牌）

⚠️ **资源文件：**
- 如果HTML引用了CSS、JS、图片等文件，需要手动添加这些文件
- 建议使用相对路径而非绝对路径

⚠️ **部署时间：**
- GitHub Pages部署通常需要1-2分钟
- 首次部署可能需要更长时间

## 故障排除

### 问题1：推送失败 "repository not found"
**解决方案**：先在GitHub上创建仓库 https://github.com/new

### 问题2：权限错误
**解决方案**：
- 检查GitHub登录状态
- 配置SSH密钥或个人访问令牌
- 确认对仓库有写入权限

### 问题3：页面无法访问
**解决方案**：
- 确认已在仓库Settings → Pages中启用
- 等待1-2分钟让部署完成
- 检查HTML文件中的资源路径

## 相关链接

- [GitHub Pages官方文档](https://docs.github.com/pages)
- [创建GitHub仓库](https://github.com/new)
- [配置Git认证](https://docs.github.com/authentication)

---

创建时间：2026-03-04
Skill文件位置：`.claude/skills/html-to-github-pages.skill`
