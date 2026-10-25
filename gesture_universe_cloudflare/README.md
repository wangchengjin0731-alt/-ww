# 手势宇宙 Gesture Universe — Cloudflare Pages

## 部署
1. 解压 ZIP。
2. 在 Cloudflare Dashboard 打开 **Workers & Pages → Create → Pages**，选择静态资源直接上传（Direct Upload，界面文案可能略有不同）。
3. 上传解压后这四个文件，确认 `index.html` 位于部署目录根部。
4. 部署后通过 `https://项目名.pages.dev` 访问。

## 交互
- 鼠标移动 / 手机触摸：星球焦点跟随。
- 点击画布：触发粒子爆发。
- 点击三张手势卡：切换创造、捕捉、探索模式。
- 点击开启摄像头并授权：尝试识别张开手掌、捏合动作（MediaPipe Hands）。

## 注意
- 摄像头需要 HTTPS 或 localhost；Cloudflare Pages 默认提供 HTTPS。
- 手势识别依赖 jsDelivr CDN 和 MediaPipe 模型，首次打开需联网。
- 摄像头视频只在浏览器本地处理，代码没有上传视频的逻辑。
- 若 CDN/权限不可用，鼠标、触摸与卡片交互仍可使用。
