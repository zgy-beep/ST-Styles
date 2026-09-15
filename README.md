# ✦ SillyTavern 双色盒子美化样式 (ST-Styles)

一款专为 **SillyTavern（酒馆）** 打造的轻奢质感主题样式库。

> **原作者致敬**：KAKAA（Discord: `@rech0_viixi`）  
> **发布社区**：类脑 ΟΔΥΣΣΕΙΑ · 旅程 ΟΡΙΖΟΝΤΑΣ  
> **许可协议**：[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)（署名-非商业性使用-相同方式共享）  
> **本项目优化**：修复语法解析错误、补充全局交互微动效、双色发光微光环算法升级、深度思考链（Reasoning）样式强化与全面屏安全区适配。

---

## 🚀 快速使用

### 方式一：在酒馆中在线引用（推荐）

打开 SillyTavern（酒馆）界面：
1. 点击顶栏的 **设置图标（小齿轮）** -> 找到 **「用户设置 (User Settings)」**；
2. 找到 **「自定义 CSS (Custom CSS)」** 输入框；
3. 填入以下任意一条导入语句，并点击保存即可即时生效：

```css
/* 首选国内高速 CDN 节点 */
@import url("https://testingcf.jsdelivr.net/gh/zgy-beep/ST-Styles/双色盒子.css");
```

#### 备用 CDN 节点（若主节点网络波动可替换）：
```css
/* 备用节点 1 (Fastly) */
@import url("https://fastly.jsdelivr.net/gh/zgy-beep/ST-Styles/双色盒子.css");

/* 备用节点 2 (官方全局) */
@import url("https://cdn.jsdelivr.net/gh/zgy-beep/ST-Styles/双色盒子.css");
```

---

### 方式二：本地全量载入

如果你需要在离线环境或无网络代理时使用：
1. 打开本仓库中的 [`双色盒子.css`](./双色盒子.css)；
2. 复制全部代码；
3. 直接粘贴至酒馆的 **自定义 CSS (Custom CSS)** 文本框中。

---

## ❓ 常见疑问解答 (FAQ)

### 为什么直接写 GitHub 链接（如 `https://github.com/.../双色盒子.css`）无法改变样式？

很多朋友在初次使用时会尝试这样写：
```css
/* ❌ 错误示范：完全无法生效 */
@import url("https://github.com/zgy-beep/ST-Styles/双色盒子.css");
/* 或 */
@import url("https://raw.githubusercontent.com/zgy-beep/ST-Styles/main/双色盒子.css");
```

**原因解析：**

1. **MIME 类型（Content-Type）不匹配：**
   - 浏览器和酒馆前端遵循严格的 CSS 安全规范（`CORB` 与 `X-Content-Type-Options: nosniff`）；
   - 打开 `github.com/...` 得到的是 GitHub 的**网页页面（HTML 文档）**，返回的响应头为 `Content-Type: text/html`；
   - 浏览器检测到不是 `text/css`，会直接**阻断并丢弃**该样式表，杜绝脚本混淆风险。

2. **GitHub Raw 的文本保护机制：**
   - 即使使用 `raw.githubusercontent.com`，GitHub 官方为了防止他人将其滥用为免费 CDN，故意将其 Content-Type 限制为 `text/plain`（纯文本），现代浏览器同样拒绝将其作为 CSS 解析执行。

3. **CDN 服务的核心作用：**
   - `testingcf.jsdelivr.net` / `cdn.jsdelivr.net` 是专门面向开源仓库的静态文件分发网络；
   - CDN 会自动将仓库中的 `.css` 文件以标准合规的 `Content-Type: text/css; charset=utf-8` 和 `Access-Control-Allow-Origin: *`（允许跨域）返回给浏览器，因此样式得以被浏览器顺利加载渲染。

---

## 🎨 特色与优化升级亮点

- 🌟 **双色动态发光头像框**：用户与 AI 头像分别融入主色1与主色2交织的光环，鼠标悬停时柔和微缩放并扩散光晕。
- ⚡ **丝滑交互触觉微动效**：所有按钮、抽屉图标与控制项注入贝塞尔曲线缓动，悬停微上浮、按压弹性微缩放。
- 🧠 **深度思考链（Reasoning Process）**：对 DeepSeek-R1、Claude 等思考输出块做了折叠与展开样式重构，带渐变星芒与次级遮罩。
- 📱 **全面屏手势区自适应**：底栏发送区域接入 `env(safe-area-inset-bottom)`，彻底解决 iPhone 及全面屏手机小白条手势遮挡问题。
- 🪄 **全站统一划词高亮**：划选任何文本均呈现轻奢半透主题色，告别系统原生刺眼的蓝底白字。
- 💊 **极简胶囊滚动条**：999px 全圆角半透悬浮滑块，拖拽时自适应渐变响应。

---

## 🛠️ 主题配色调节提示

《双色盒子》深度联动酒馆的主题系统，推荐在酒馆「主题设置」中调整以下几项以达到最佳视觉契合：
- **引用文本颜色 (Quote Color)** ➔ 对应主题主色 1（星芒、发光主色、顶栏下划线）
- **下划线文本颜色 (Underline Color)** ➔ 对应主题主色 2（辅助发光色、渐变融合色）
- **模糊色调 (Blur Tint Color)** ➔ 决定界面的基础暗色透明度与自适应次级灰阶

---

## 📄 开源声明

本美化样式在 原作者 KAKAA 的开源版本基础上进行体验重构与缺陷修复，遵守 **CC BY-NC-SA 4.0** 协议：
- 二改或衍生分享须保留原作者及出处信息；
- 严格禁止任何形式的商业用途与商业性引流。
