# Social media account intro promo

A Claude Fable 5.2 motion design video by [@Leviwoyun](https://x.com/Leviwoyun). [Original post](https://x.com/Leviwoyun/status/2119970987827749068) · [Watch on MotionVideo](https://motionvideo.xyz/videos/leviwoyun-35cc7c?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

[![Social media account intro promo](https://assets.motionvideo.xyz/motion/leviwoyun-35cc7c/poster-89cb6ae4f5.jpg)](https://motionvideo.xyz/videos/leviwoyun-35cc7c?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

- **Creator:** [@Leviwoyun](https://x.com/Leviwoyun)
- **Model:** Claude Fable 5.2
- **Stack:** node + ffmpeg
- **Categories:** Kinetic typography, Photo motion
- **Posted:** 2026-11-10

## Prompt

```text
给我的社交媒体账号做一条 [15–30] 秒的账号介绍动态图形短片，让第一次刷到我的人看完就知道我是谁、发什么、为什么值得关注。节奏紧、动效细节多、看完想关注。请尽情发挥创意。

账号的真实信息（只能用这些，不要编造任何数据、名字、经历或作品）：
- 名字：[昵称]，账号 @[账号]，平台：[X / 小红书 / B站 / 抖音…]
- 一句话定位：[我是谁、做什么]
- 内容方向：[3 个以内的关键词]
- 代表作或成绩：[真实的作品、数据、经历，没有就删掉这行]
- 粉丝 [粉丝数]，已发 [作品数] 条，获赞 [获赞数]（不想露数据就删掉这行）
- 简介原文：[粘贴简介]
- 头像：assets/avatar.jpg（可以用；有作品截图也放 assets/，并说明每张图是什么）

交付要求（技术约束）：
- 在当前目录里用代码生成画面，技术栈自选，可用本机 node / ffmpeg，npm 包装在本目录。
- 成片放到 out/intro.mp4：[1920×1080 横屏 / 1080×1920 竖屏]，30fps，H.264；带配乐或音效，和画面节奏对齐，响度适中（约 -14 LUFS）。
- 视觉风格从头像和内容方向里长出来，别套通用科技风模板。
- 画面文字以 [中文] 为主，口吻真诚、有记忆点，不要空洞的 AI 腔口号；最后一屏要有名字、账号和一句话定位。
- 再导出一张 out/cover.jpg 当视频封面，尺寸和成片一致，从最好看的一帧取。
- 渲染完用 ffprobe 核规格，逐帧查空白帧、文字溢出、错位，有问题自己修。
- 做完写 out/说明.md：创意思路、分镜时间线、已知不足。
- 不要 git commit / push，不要联网发布任何东西。
```

More Claude Fable 5.2 motion design, each with its prompt: [motionvideo.xyz/model/fable-5-2](https://motionvideo.xyz/model/fable-5-2?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)
