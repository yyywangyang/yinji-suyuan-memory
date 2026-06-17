# 印迹溯源数字记忆页

这是“印迹溯源——基于 AIGC + NFC 的文旅即时共创微工坊”的静态 H5 原型页。

当前 MVP 阶段采用二维码完成“实体载体—数字页面”的绑定验证；后续可将同一页面链接写入 NFC 标签，实现手机触碰访问。

## 文件结构

```text
.
├── index.html
├── assets/
│   ├── images/
│   │   ├── ai-pattern.png
│   │   ├── product-concept.png
│   │   ├── tech-architecture.png
│   │   └── workshop-concept.png
│   └── photos/
│       ├── memory-1.jpg
│       ├── memory-2.jpg
│       └── memory-3.jpg
└── tools/
    └── qr-helper.html
```

## 添加你的照片

把 3 张照片放入：

```text
assets/photos/
```

并命名为：

```text
memory-1.jpg
memory-2.jpg
memory-3.jpg
```

如果暂时没有照片，页面会显示占位说明。

## GitHub Pages 部署

1. 新建 GitHub 仓库：

```text
yinji-suyuan-memory
```

2. 将本项目所有文件推送到仓库根目录。

```bash
git init
git add .
git commit -m "Add digital memory page"
git branch -M main
git remote add origin https://github.com/你的用户名/yinji-suyuan-memory.git
git push -u origin main
```

3. 打开仓库 `Settings → Pages`。

4. 选择：

```text
Source: Deploy from a branch
Branch: main
Folder: /root
```

5. 等待 1-3 分钟后访问：

```text
https://你的用户名.github.io/yinji-suyuan-memory/
```

## 生成二维码

部署成功后打开：

```text
tools/qr-helper.html
```

输入 GitHub Pages 链接，即可生成并下载二维码。

二维码旁建议配文：

```text
扫码查看我的数字文旅记忆
MVP 阶段二维码验证，后续升级为 NFC 触碰访问
```

## 注意

页面中不得写成“已完成 NFC 写入”或“已内置 NFC 芯片”。当前展示口径是二维码等效验证。
