# GitHub Pages 部署指南

## 快速部署步骤

### 1. 创建 GitHub 仓库
```bash
# 在 GitHub 上创建一个新仓库
# 例如：tech-algorithms-prototype
```

### 2. 初始化本地仓库
```bash
git init
git add index.html
git commit -m "Initial commit - 产业链深度分析模型原型"
```

### 3. 关联 GitHub 仓库
```bash
git remote add origin https://github.com/你的用户名/tech-algorithms-prototype.git
git branch -M main
git push -u origin main
```

### 4. 启用 GitHub Pages
1. 进入仓库页面
2. 点击 **Settings** → **Pages**
3. 在 **Build and deployment** → **Source** 选择 **Deploy from a branch**
4. 在 **Branch** 选择 **main** 和 **/ (root)**
5. 点击 **Save**

### 5. 访问网站
等待 1-2 分钟后，访问：
```
https://你的用户名.github.io/仓库名/
```

例如：https://yourname.github.io/tech-algorithms-prototype/

---

## 完整部署脚本

```bash
# 克隆或初始化仓库
cd /home/zhangzhong/src/tech-algorithms-prototype
git init

# 添加文件
git add index.html
git commit -m "feat: 产业链深度分析模型原型

- 13个产业链深度分析模块
- 10种不同的可视化类型
- 左右布局设计
- 完全静态，无后端依赖"

# 关联 GitHub 仓库（替换为你的仓库地址）
git remote add origin https://github.com/YOUR_USERNAME/tech-algorithms-prototype.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

---

## 添加其他文档（可选）

如果也想部署文档文件：

```bash
# 添加所有文档
git add README.md FEATURES.md speech.md demo-guide.md docs/ IMPLEMENTATION_SUMMARY.md

# 提交
git commit -m "docs: 添加项目文档"

# 推送
git push
```

---

## 自定义域名（可选）

### 1. 购买域名
在域名提供商（阿里云、腾讯云、Cloudflare等）购买域名

### 2. 在 GitHub Pages 设置域名
1. Settings → Pages
2. Custom domain: 输入你的域名（如 `demo.yourdomain.com`）
3. 点击 Save

### 3. 配置 DNS
在你的域名提供商处添加 DNS 记录：
```
类型: CNAME
主机记录: demo（或 www）
记录值: yourname.github.io
TTL: 600
```

---

## 更新网站

修改代码后：
```bash
git add index.html
git commit -m "update: 更新功能"
git push
```

GitHub Pages 会自动重新部署，通常 1-2 分钟生效。

---

## 故障排查

### 1. 页面显示 404
- 检查 GitHub Pages 是否已启用
- 等待 2-3 分钟让部署完成
- 确认 branch 和 folder 设置正确

### 2. 页面样式错乱
- 检查 index.html 文件是否完整
- 清除浏览器缓存（Ctrl+F5 或 Cmd+Shift+R）

### 3. 部署失败
- 检查仓库是否有 index.html 文件
- 查看 Actions 页面查看部署日志
- 确保文件大小不超过 GitHub Pages 限制（100MB）

---

## 访问统计

GitHub Pages 默认不提供访问统计，可以集成：
- Google Analytics
- Cloudflare Web Analytics
- Vercel Analytics

---

## 示例

演示网站：https://yourname.github.io/tech-algorithms-prototype/

---

## 支持

遇到问题？
- GitHub Pages 文档：https://docs.github.com/en/pages
- 项目 README.md：README.md
- 实现总结：IMPLEMENTATION_SUMMARY.md
