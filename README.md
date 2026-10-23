# studio3d-prototype

**在线演示 / Live demo**: https://love8868.github.io/studio3d-prototype/

**源码 / Source**: https://github.com/love8868/studio3d

浏览器里的 3D 产品出图工作台静态构建：充电柜、线缆、显示器支架三种代理场景，支持多画幅取景与 AI 交接包导出。

## 本版说明 / What's in this build

- 8 种导出画幅：4:3、1:1、4:5、3:4、2:3、3:2、16:9、9:16；预览与导出共用同一 aspect。
- AI 交接包 ZIP：干净图、深度图、机位 JSON、`prompt.txt`、`README.txt`。
- `prompt.txt` 按当前模式/机位/焦段/画幅生成，可直接复制给 Gemini / 图生图模型；面板也提供“复制提示词”。
- 对比度达到 WCAG AA；Lighthouse Accessibility 1.0。
- “当前机位”压缩为单行指标，并保留滚动提示。
- 多视角导出暂缓到 P2；线缆模式保留。

## 构建 / Build

此分支是构建产物，源码与开发说明见 source 仓库。部署到 GitHub Pages 子路径时使用：

```bash
npx vite build --base=./
```

请勿直接编辑本目录的 `assets/`；重新构建后再发布。
