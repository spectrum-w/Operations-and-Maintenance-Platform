# Operations-and-Maintenance-Platform

这是“数字能源运维平台-移动端原型”的 GitHub Pages 发布仓库。

## 目录结构

```text
Operations-and-Maintenance-Platform/
├── prototype/
│   └── index.html
├── .github/workflows/pages.yml
├── .gitignore
└── README.md
```

## 重要说明

当前原型是一个单文件 HTML，推荐将原文件复制或重命名为：

```text
prototype/index.html
```

这样发布后的固定地址会直接打开原型：

```text
https://spectrum-w.github.io/Operations-and-Maintenance-Platform/
```

如果原型后续拆分出 CSS、JS、图片或字体，请继续放在 `prototype/` 下，例如：

```text
prototype/
├── index.html
├── css/
├── js/
└── assets/
```

HTML 中使用相对路径：

```html
<link rel="stylesheet" href="./css/style.css">
<script src="./js/app.js"></script>
<img src="./assets/logo.png" alt="Logo">
```

不要使用电脑本地路径，例如 `E:\...` 或 `file:///...`。

## 第一次发布

在本地仓库根目录执行：

```powershell
git init -b main
git add .
git commit -m "feat: publish mobile prototype v1.0.0"
git remote add origin https://github.com/spectrum-w/Operations-and-Maintenance-Platform.git
git push -u origin main
```

然后在 GitHub 仓库中打开：

```text
Settings → Pages → Source → GitHub Actions
```

到 `Actions` 页面等待 `Deploy prototype to GitHub Pages` 完成。

## 后续更新

替换或修改 `prototype/index.html` 后执行：

```powershell
git add prototype
git commit -m "update: revise mobile prototype"
git push
```

固定 URL 不变，GitHub Actions 会自动发布最新版本。

## 历史版本

```powershell
git log --oneline
git show <commit-id>
git revert <commit-id>
git push
```

推荐用 `git revert` 恢复历史版本，因为它会保留完整提交记录。
