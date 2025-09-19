# 我的Scoop Bucket

这是一个自定义的Scoop软件包仓库。

## Manifest字段说明
- `checkver`: 自动检测软件新版本（通过GitHub API）
- `autoupdate`: 根据新版本号自动生成下载URL
- `architecture`: 指定不同系统架构的下载地址
- `persist`: 用于指定需要持久化保存的文件或目录，这些数据会在软件更新时被保留。

## 使用方法

1. 初始化Git仓库并推送到GitHub:
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/jiyuchen1/scoop-bucket.git
git push -u origin main
```

2. 添加bucket到本地Scoop:
```bash
scoop bucket add my-bucket https://github.com/jiyuchen1/scoop-bucket.git
# 实际使用时可以github后添加fast来加速下载
```

3. 安装软件包:
```bash
scoop install marktext
```

## 包含软件包
- marktext - 简洁优雅的Markdown编辑器
