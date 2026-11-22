# 条码 / 二维码生成器

纯前端静态网站，浏览器本地实时生成条形码与二维码，支持导出 PNG / SVG，无需后端和数据库。

## 功能

- **条形码**：Code 128（自动/A/B/C）、EAN-13、EAN-8、UPC-A、Code 39、Code 93、ITF-14、ITF、MSI 全系、Pharmacode，共 17 种格式
- **条码排版**：可调条宽、高度、字号、边距、文本间距、字体族、对齐方式、粗体 / 斜体、线条与背景颜色
- **二维码**：支持链接 / 文本，可调尺寸、纠错等级（L/M/Q/H）、码点与背景颜色，可下载 PNG
- 实时预览，一键下载高清 PNG / SVG，支持复制到剪贴板；支持仅打印当前码图
- 6 款个性主题（明亮、暗夜、紫罗兰、薄荷、落日、赛博），选择自动记忆
- 响应式布局，手机 / 平板 / 桌面均可正常使用
- 全部计算在本地完成，数据不上传

## 本地运行

直接用浏览器打开 `index.html` 即可，无需安装依赖。

## 部署到 GitHub Pages

1. 在 GitHub 上新建一个仓库（例如 `barcode-generator`）。
2. 把 `index.html` 和 `README.md` 提交到仓库：

   ```bash
   git init
   git add .
   git commit -m "初始化条形码生成器"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/barcode-generator.git
   git push -u origin main
   ```

3. 进入仓库 **Settings → Pages**，在 **Build and deployment** 中：
   - Source 选择 **Deploy from a branch**
   - Branch 选择 `main`，目录选 `/ (root)`，保存
4. 等待 1–2 分钟，访问：

   ```
   https://<你的用户名>.github.io/barcode-generator/
   ```

## 技术说明

- 条码：[JsBarcode](https://github.com/lindell/JsBarcode)，二维码：[qrcodejs](https://github.com/davidshimjs/qrcodejs)
- 两个库的代码已内联进 `index.html`，**整个项目只有一个 HTML 文件，无需联网、无外部依赖**
- 原生 HTML / CSS / JavaScript，无构建工具

> 部署到 GitHub 时，只需把 `index.html` 提交即可；`README.md` 为说明文档，可选提交。

> （注：部分内容由豆包 AI 生成）