# 拾光映画 · 交互艺术相册 (GitHub Pages 部署包)

这是一个为您定制的交互式静态相册网页，内置坂本龙一《Merry Christmas Mr. Lawrence》背景音乐与全套 3D 丝滑过渡动画。

## 一、照片文件夹放在哪里？（目录结构）

请保持以下文件夹结构，**将您所有的照片直接放进与 `index.html` 同级的 `photos` 文件夹内**：

```text
photo-album/             <-- 您的项目根目录（上传到 GitHub 仓库的内容）
├── index.html           <-- 相册主网页代码
├── photos/              <-- 【把您的所有照片放在这个文件夹里！】
│   ├── 1.jpg
│   ├── 2.jpg
│   ├── 3.jpg
│   └── ...
└── music/               <-- 音乐文件夹
    └── bgm.mp3          <-- 已内置您上传的《Merry Christmas Mr. Lawrence - 坂本龍一》
```

### 如何替换成您自己的照片？
1. **最简单方式（免改代码）**：直接将您的 8 张照片命名为 `1.jpg`、`2.jpg` ... `8.jpg`，覆盖放入 `photos/` 文件夹即可。
2. **自定义任意张数、文件名与文字说明**：用记事本或 VS Code 打开 `index.html`，找到第 430 行左右的 `USER_CONFIG` 配置区，按照里面的格式增删照片文件名、标题和寄语即可。

---

## 二、如何免费部署到 GitHub Pages（让朋友直接点击观看）

1. **创建仓库**：
   - 登录 [GitHub](https://github.com/)，点击右上角的 **`+`** -> **`New repository`**。
   - **Repository name** 填写例如 `my-album`。
   - 选择 **Public（公开）**，然后点击底部的 **Create repository**。

2. **上传相册文件**：
   - 在新建好的仓库页面中，点击 **uploading an existing file**。
   - 将本压缩包解压后的 **`index.html`、`photos` 文件夹、`music` 文件夹** 一起拖拽到网页上传框中（注意：确保 `index.html` 直接在仓库根目录下，而不是再套一层外层文件夹）。
   - 等待文件上传完毕后，点击底部的绿色按钮 **Commit changes**。

3. **开启 GitHub Pages 网页服务**：
   - 点击仓库顶部的 **Settings（设置）** 选项卡。
   - 在左侧菜单栏找到并点击 **Pages**。
   - 在 **Build and deployment -> Branch** 下，将 `None` 改为 **`main`**（或 `master`），右侧目录保持 **`/(root)`**，点击 **Save**。
   - 等待约 **1 ~ 2 分钟**后刷新该页面，顶部会出现一行提示：
     `Your site is live at https://您的GitHub用户名.github.io/my-album/`
   - 复制这个链接发给朋友，朋友在手机或电脑上点击即可直接伴随着音乐浏览您的相册！
