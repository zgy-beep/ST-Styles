# ✦ SillyTavern 双色盒子美化样式 (ST-Styles 独家特色版)

一款专为 **SillyTavern（酒馆）** 深度打造的轻奢质感主题样式库。

> **原作者致敬**：KAKAA（Discord: `@rech0_viixi`）  
> **发布社区**：类脑 ΟΔΥΣΣΕΙΑ · 旅程 ΟΡΙΖΟΝΤΑΣ  
> **许可协议**：[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)（署名-非商业性使用-相同方式共享）  
> **本仓库独家特色升级**：浮空轻奢双色卡片气泡、悬浮流光底栏、极客胶囊元数据标签、灵动呼吸星芒、深度思考 HUD 舱与全面屏手势区适配。

---

## 🚀 快速使用

打开 SillyTavern（酒馆）界面：
1. 点击顶栏的 **设置图标（小齿轮）** ➔ **「用户设置 (User Settings)」**；
2. 找到 **「自定义 CSS (Custom CSS)」** 输入框；
3. 填入以下导入语句，保存即可即时生效：

```css
/* 推荐：直接引入最新特色版 */
@import url("https://testingcf.jsdelivr.net/gh/zgy-beep/ST-Styles/双色盒子.css");
```

> 💡 **提示（若遇 CDN 缓存未刷新）**：  
> CDN 边缘服务器默认可能会有短时缓存，若想**100% 立即强制加载最新特色版**，可直接使用以下带版本锁定的直链：
> ```css
> @import url("https://testingcf.jsdelivr.net/gh/zgy-beep/ST-Styles@main/双色盒子.css?v=2.0");
> ```

---

## 🌟 独家特色设计一览

| 特色亮点 | 原版表现 | 本仓库【独家特色版】表现 |
| :--- | :--- | :--- |
| **消息气泡** | 0px 直角死板平铺贴边 | **14px 浮空轻奢圆角卡片**，左右保留呼吸缝隙与微投影 |
| **消息边框饰条** | 无侧边指引 | **AI 专属左侧主题色1光条**，**用户专属右侧主题色2光条** |
| **底栏发送框** | 贴底平铺矩形 | **16px 胶囊悬浮岛 (Floating Island)** + 聚焦呼吸微霓虹光环 |
| **消息元数据** | 普通纯文本排布 | **极客胶囊徽章化**（耗时 `⏱️`、Token 数、消息 ID 独立胶囊） |
| **标题装饰星芒** | 静态符号 | **✦ 动态呼吸慢速光影**，主色1与主色2交织微发光 |
| **深度思考舱** | 单薄左边线 | **Reasoning HUD 舱**，渐变折叠条与次级背景内嵌阴影 |
| **全面屏适配** | 易被手势横条遮挡 | **原生安全区适配**（`env(safe-area-inset-bottom)`） |

---

## ❓ 常见问题：为什么直接写 GitHub 链接不能生效？

```css
/* ❌ 错误写法：浏览器会直接丢弃阻断 */
@import url("https://github.com/zgy-beep/ST-Styles/双色盒子.css");
```

- **MIME 类型（Content-Type）拦截**：GitHub 网页返回的是 `text/html`（网页文档），而浏览器遵循严格的 CSS 安全规范（`nosniff`），非 `text/css` 类型会被直接拦截。
- **CDN 的核心作用**：通过 `testingcf.jsdelivr.net` 引入时，CDN 会将 GitHub 上的代码转为合规的 `Content-Type: text/css; charset=utf-8` 和 `Access-Control-Allow-Origin: *`（允许跨域），酒馆才能正确应用样式。

---

## 🎨 调色盘联动建议

在酒馆「主题设置」中调整：
- **引用文本颜色 (Quote Color)** ➔ 对应主色 1（AI 发光环、左侧光条、星芒）
- **下划线文本颜色 (Underline Color)** ➔ 对应主色 2（用户发光环、右侧光条、微霓虹）
- **模糊色调 (Blur Tint Color)** ➔ 决定界面的基础暗色透明度与次级灰阶

---

## 📄 开源声明

本美化样式在 原作者 KAKAA 的开源版本基础上进行体验重构与缺陷修复，遵守 **CC BY-NC-SA 4.0** 协议：
- 二改或衍生分享须保留原作者及出处信息；
- 严格禁止任何形式的商业用途与商业性引流。
