# Christmas Tree v17.6

HTML 圣诞树，带金色粒子、飘雪、手势识别、照片挂饰和音乐。支持电脑拖动旋转与手机触摸。

在线地址：<https://timonrr.github.io/christmas-tree-v17.6/>

GitHub 仓库：<https://github.com/TimonRR/christmas-tree-v17.6>

## 来源

源码来自 <https://github.com/liq47317-boop/christmas-tree-v17.6> 的 `main/index.html`。
仓库名称为 v17.6，源码内部版本标注为 **Grand Luxury Tree v17.6.5**。
保留原项目的视觉效果和功能；补充 GitHub Pages 部署配置、字体加载修复及加载失败提示。手势模块增加主动启用按钮、可见摄像头预览、独立模型状态、超时与重试，并按手掌大小判断动作。

## 本地预览

在本目录运行：

```sh
python3 -m http.server 8080 --bind 127.0.0.1
```

浏览器打开 <http://127.0.0.1:8080>。页面 CSS 和 JavaScript 写在 `index.html` 内，MediaPipe 与手势模型放在 `assets/` 并从本站加载。Three.js 和可选字体仍通过外部网络加载，因此它不是离线 HTML。部署时必须一起上传 `assets/`。

## 发布到 GitHub Pages

1. 将本目录文件上传至自己的 GitHub 仓库，分支名使用 `main`，包含 `.github/workflows/pages.yml`。
2. 在仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
3. 在 **Actions** 页运行 **Deploy Christmas Tree to GitHub Pages**，或向 `main` 推送一次提交。
4. 部署完成后，访问该工作流显示的网站地址。

也可以上传 `index.html`、`.nojekyll` 与完整 `assets/` 目录，在 Pages 的 Source 选择 **Deploy from a branch**，并指定 **main / (root)**。

## 操作

- 鼠标或单指拖动：旋转圣诞树；双指拖动：缩放。
- `Space`：聚合；`Z`：散开；`X`：抓取照片；`H`：显示或隐藏面板。
- 左侧面板可修改祝福语、字体、颜色、粒子与雪花参数。
- 上传照片或 MP3 后，可作为树上的挂饰或背景音乐；内容保存在当前浏览器内，不会传至 GitHub。
- 点击右上角 **启用手势**，允许摄像头权限；整个手掌进入预览画面后，张手散开、握拳聚合、拇指与食指捏合抓取照片。再次点击可关闭摄像头。
- 预览中的绿色点表示识别到了手；底部显示当前动作。摄像头、模型加载失败分别提示，点击 **重试手势** 可以重试。
- 手势识别需要 HTTPS 或 localhost；首次从本站加载约 8 MB 模型和约 9 MB 运行时。没有摄像头也可使用按钮与拖动。
- 若提示“摄像头没有输出画面”，请在 Chrome 或 Edge 中直接打开在线地址，允许浏览器和操作系统使用摄像头；避免在不能输出摄像头视频的应用内嵌浏览器中使用。

本仓库使用 GitHub Actions 发布到 GitHub Pages。向 `main` 推送更新后，工作流自动更新在线页面。
