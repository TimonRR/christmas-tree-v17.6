# Christmas Tree v17.6

单文件 HTML 圣诞树，带金色粒子、飘雪、手势识别、照片挂饰和音乐。支持电脑拖动旋转与手机触摸。

## 来源

源码来自 <https://github.com/liq47317-boop/christmas-tree-v17.6> 的 `main/index.html`。
仓库名称为 v17.6，源码内部版本标注为 **Grand Luxury Tree v17.6.5**。
保留原项目的视觉效果和功能；本地补充 GitHub Pages 部署配置、字体加载修复及加载失败提示。

## 本地预览

在本目录运行：

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

浏览器打开 <http://127.0.0.1:8080>。CSS 和 JavaScript 写在 `index.html` 内；Three.js、MediaPipe、手势模型与可选字体仍通过网络加载，因此它不是离线 HTML。

## 发布到 GitHub Pages

1. 将本目录文件上传至自己的 GitHub 仓库，分支名使用 `main`，包含 `.github/workflows/pages.yml`。
2. 在仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
3. 在 **Actions** 页运行 **Deploy Christmas Tree to GitHub Pages**，或向 `main` 推送一次提交。
4. 部署完成后，访问该工作流显示的网站地址。

也可以只上传 `index.html` 与 `.nojekyll`，在 Pages 的 Source 选择 **Deploy from a branch**，并指定 **main / (root)**。

## 操作

- 鼠标或单指拖动：旋转圣诞树；双指拖动：缩放。
- `Space`：聚合；`Z`：散开；`X`：抓取照片；`H`：显示或隐藏面板。
- 左侧面板可修改祝福语、字体、颜色、粒子与雪花参数。
- 上传照片或 MP3 后，可作为树上的挂饰或背景音乐；内容保存在当前浏览器内，不会传至 GitHub。
- 摄像头权限允许后，可用手势控制；没有摄像头也可使用按钮与拖动。
- 手势识别需要 HTTPS 或 localhost；首次加载需联网下载依赖和模型。

本目录只准备了部署文件。远程仓库创建、上传和上线须使用自己的 GitHub 登录身份完成。
