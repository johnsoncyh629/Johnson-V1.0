# Johnson V1.0 设计系统提示词

## 概述
这是一个工业/制造业领域的暗黑风格网站设计系统，具有强烈的视觉冲击力和现代感。在使用AI工具时，请粘贴此提示词以保持设计风格的一致性。

---

## 核心设计原则

### 1. 设计风格定位
- **整体风格**：暗黑工业风，高端制造业
- **视觉特点**：科技感、力量感、专业性
- **用户体验**：沉浸式、动态交互、视觉引导

### 2. 品牌特征
- **品牌调性**：专业、创新、可靠、高端
- **设计语言**：几何、斜切、渐变、动态

---

## 色彩系统

### 主色调
```
品牌红色（主要强调色）：#A72A29
深红色（渐变/阴影）：#431616
```

### 背景色系
```
纯黑：#000000（主背景）
深灰黑：#131313
炭黑：#111111
暗灰：#242424（次级背景）
深灰：#1A1A1A（卡片/模块背景）
```

### 文字色系
```
主文字：#FFFFFF（纯白）
次要文字：#CCCCCC（浅灰）
辅助文字：#999999（中灰）
说明文字：#666666（灰色）
标题文字：#333333（深灰，用于浅色背景）
正文文字：#222222（深灰，用于浅色背景）
```

### 功能色系
```
背景浅色：#E2E2E2（表单、卡片）
浅灰背景：#F6F6F6（输入框）
边框色：#DEDEDE, #CBCBCB, #C5C5C5
错误/警告：#A72A29（复用品牌色）
成功：使用白色高亮
```

### 透明度规范
```
遮罩层：rgba(0,0,0,0.6) - rgba(0,0,0,0.7)
半透明背景：rgba(0,0,0,0.4) - rgba(0,0,0,0.5)
边框透明：rgba(255,255,255,0.1) - rgba(0,0,0,0.1)
文字透明：rgba(255,255,255,0.6) - rgba(255,255,255,0.8)
```

### 渐变使用
```css
/* 品牌红色渐变 */
background: linear-gradient(#A72A29, #431616);

/* 黑色渐变 */
background: linear-gradient(#000000, #242424);
background: linear-gradient(#242424, #000000);

/* 文字渐变效果 */
background: #FFFFFF linear-gradient(#A72A29, #431616) no-repeat;
-webkit-background-clip: text;
background-clip: text;
-webkit-text-fill-color: transparent;
```

---

## 字体系统

### 字体族
```css
font-family: 'DoHyeon', 'PingFang SC', 'Microsoft YaHei',
             'Microsoft YaHei UI', 'SimSun', 'SimHei', 'Arial';
```

**使用场景**：
- **DoHyeon**：品牌标题、大标题、强调性文字
- **PingFang SC/Microsoft YaHei**：中文正文、界面文字
- **Arial**：英文/数字备选

### 字体大小系统

#### 桌面端字体（1280px - 1760px响应式）
```
超大标题：--font200 (200px) - 品牌展示
特大标题：--font140 (140px) - 页面主标题
大标题1：--font120 (120px) - 区块标题
大标题2：--font100 (100px) - 次级标题
大标题3：--font86 (86px) - 三级标题
标题系列：--font72 (72px) - --font68 (68px) - --font54 (54px)
中等标题：--font38 (38px) - --font36 (36px) - --font32 (32px)
小标题：--font26 (26px) - --font24 (24px)
正文大：--font20 (20px) - --font18 (18px)
正文：--font16 (16px)
辅助文字：--font14 (14px)
```

#### 移动端调整
```
@media (max-width: 1580px) { font-size: 66px }
@media (max-width: 767px) { font-size: calc(100vw/7.5) }
```

### 行高规范
```
标题行高：1.0 - 1.2
正文行高：1.375 - 1.5
特殊场景：1.556
紧凑文本：1.2
```

### 字重
```
常规：normal (400)
中等：500
加粗：使用字体族变化，不使用font-weight: bold
```

---

## 间距系统

### 间距变量（响应式）
```
--spacing-20: 14px - 20px
--spacing-25: 18px - 25px
--spacing-30: 20px - 30px
--spacing-40: 20px - 40px
--spacing-44: 22px - 44px
--spacing-50: 26px - 50px
--spacing-60: 30px - 60px
--spacing-70: 36px - 70px
--spacing-80: 40px - 80px
--spacing-90: 50px - 90px
--spacing-100: 58px - 100px
--spacing-110: 64px - 110px
--spacing-120: 68px - 120px
--spacing-130: 72px - 130px
--spacing-140: 76px - 140px
--spacing-150: 78px - 150px
--spacing-160: 82px - 160px
--spacing-170: 96px - 170px
--spacing-180: 100px - 180px
```

### 使用建议
- **组件内间距**：使用 spacing-20 ~ spacing-40
- **组件间间距**：使用 spacing-50 ~ spacing-80
- **区块间距**：使用 spacing-100 ~ spacing-160
- **页面区段**：使用 spacing-120 ~ spacing-180

---

## 圆角系统

```
--border-radius10: 5px - 10px（小按钮、标签）
--border-radius12: 6px - 12px（卡片、输入框）
--border-radius14: 7px - 14px（中等卡片）
--border-radius16: 8px - 16px（大卡片）
--border-radius18: 9px - 18px（特大卡片）
--border-radius20: 10px - 20px（超大卡片）
```

**注意**：大部分情况使用直角（0px），圆角仅用于表单元素和特定卡片

---

## 布局系统

### 响应式断点
```css
/* 超大屏 */
@media (min-width: 1901px) { /* 100px base */ }
@media (min-width: 1760px) { /* 最大内容宽度 */ }

/* 桌面 */
@media (max-width: 1580px) { /* 66px base */ }
@media (max-width: 1440px) { /* 标准桌面 */ }
@media (max-width: 1366px) { /* 笔记本 */ }
@media (max-width: 1280px) { /* 小屏桌面 */ }

/* 平板 */
@media (max-width: 1024px) { /* 横屏平板 */ }
@media (max-width: 991px) { /* 竖屏平板 */ }
@media (max-width: 768px) { /* 小平板 */ }
@media (max-width: 767px) { /* 移动端开始 */ }

/* 手机 */
@media (max-width: 640px) { /* 大屏手机 */ }
@media (max-width: 480px) { /* 标准手机 */ }
@media (max-width: 360px) { /* 小屏手机 */ }
```

### 容器宽度
```css
.container {
    width: 91.667%; /* 桌面 */
    max-width: 1760px;
    margin: 0 auto;
}

@media (max-width: 991px) {
    .container {
        width: 100%;
        padding: 0 20px; /* 移动端留白 */
    }
}
```

### Grid布局规范
```css
/* 3栏布局 */
grid-template-columns: repeat(3, 1fr);
grid-gap: 20px;

/* 4栏布局 */
grid-template-columns: repeat(4, 1fr);
grid-gap: var(--spacing-30);

/* 响应式调整 */
@media (max-width: 768px) {
    grid-template-columns: repeat(2, 1fr);
}
@media (max-width: 480px) {
    grid-template-columns: 1fr;
}
```

### Flexbox使用
```css
/* 水平居中 */
display: flex;
justify-content: center;
align-items: center;

/* 两端对齐 */
display: flex;
justify-content: space-between;
align-items: center;

/* 垂直布局 */
display: flex;
flex-direction: column;
```

---

## 特色组件设计

### 1. 斜切角按钮（idx-more）
这是网站的标志性设计元素：

```css
.idx-more {
    height: var(--value-h); /* 44px - 56px */
    display: flex;
    align-items: flex-end;
}

/* 斜线装饰 */
.idx-more .line {
    width: 1px;
    height: 150%;
    transform: rotate(26deg);
    background: #A72A29;
}

/* 按钮主体 */
.idx-more .active {
    height: 100%;
    background: #A72A29;
    color: #FFFFFF;
    padding: 0 1.25em;
}

/* 斜切角效果 */
.idx-more .active::before {
    border: solid;
    border-width: calc(var(--value-h) / 2) calc(var(--value-h) / 4);
    border-color: transparent #A72A29 #A72A29 transparent;
}

.idx-more .active::after {
    border: solid;
    border-width: calc(var(--value-h) / 2) calc(var(--value-h) / 4);
    border-color: #A72A29 #FFFFFF #FFFFFF #A72A29;
}

/* Hover动画 */
.idx-more:hover .active::before {
    border-color: transparent #FFFFFF #FFFFFF transparent;
}
.idx-more:hover .active::after {
    border-color: #FFFFFF #A72A29 #A72A29 #FFFFFF;
}
.idx-more:hover .active .word {
    background: #FFFFFF;
    color: #A72A29;
}
```

**设计原理**：
- 26度斜切角创造动感
- 红白配色反转增强交互反馈
- 动画线条引导用户注意力

### 2. 自定义滚动条
```css
::-webkit-scrollbar {
    width: 3px;
    height: 1px;
}

::-webkit-scrollbar-thumb {
    border-radius: 3px;
    background: #A72A29;
    box-shadow: inset 0 0 5px rgba(0,0,0,0.2);
}

::-webkit-scrollbar-track {
    border-radius: 3px;
    background: #ededed;
    box-shadow: inset 0 0 5px rgba(0,0,0,0.2);
}
```

### 3. 图片容器比例
```css
/* 正方形 */
.pb { padding-bottom: 100%; }

/* 16:9 视频比例 */
.pb { padding-bottom: 56.25%; }

/* 产品卡片 */
.pb { padding-bottom: 63.79%; }

/* 竖版卡片 */
.pb { padding-bottom: 119.44%; }

/* 通用图片容器 */
.pb {
    width: 100%;
    height: 0;
    position: relative;
    overflow: hidden;
}
.ab {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
}
```

### 4. 头部导航
```css
header {
    height: var(--head-height); /* 80px / 70px */
    position: fixed;
    top: 0;
    z-index: 100;
    background: transparent;
    transition: all 0.35s ease;
}

/* 滚动后样式 */
header.active,
header:hover {
    background: #FFFFFF;
}

/* Logo颜色变化 */
header.active .logo {
    color: #A72A29;
}
```

### 5. 卡片Hover效果
```css
.item {
    position: relative;
    overflow: hidden;
    transition: all 0.6s ease;
}

/* 图片缩放 */
.item:hover .img img {
    transform: scale(1.05);
}

/* 信息显示 */
.item .info-box {
    position: absolute;
    bottom: 0;
    transform: translateY(100%);
    transition: all 0.35s ease;
}

.item:hover .info-box {
    transform: translateY(0);
}

/* 标题颜色变化 */
.item:hover .title {
    color: #A72A29;
}
```

---

## 动画系统

### 过渡时长
```css
/* 标准过渡 */
transition: all 0.35s ease;

/* 图片/大元素 */
transition: all 0.6s ease;

/* 快速反馈 */
transition: all 0.4s;
```

### 关键动画

#### 1. 线条动画
```css
@keyframes moreLinesAfter {
    0% { top: -100%; }
    100% { top: 100%; }
}

.line::after {
    animation: moreLinesAfter 1.5s ease infinite;
}
```

#### 2. 渐显动画
```css
@keyframes grow2 {
    0% {
        transform: scale(1.2);
        opacity: 0;
    }
    100% {
        transform: scale(1);
        opacity: 1;
    }
}
```

#### 3. 波纹扩散
```css
@keyframes scaleZ {
    0% {
        transform: translate(-50%, -50%) scale(1);
        opacity: 0;
    }
    20% {
        opacity: 0.8;
    }
    75% {
        transform: translate(-50%, -50%) scale(12);
        opacity: 0;
    }
}
```

#### 4. 进度条
```css
@keyframes linesh {
    0% { height: 0; }
    100% { height: 100%; }
}

.progress {
    animation: linesh 5s linear;
}
```

### Transform使用
```css
/* 斜切 */
transform: skewX(-26deg);
transform: skewX(-30deg);

/* 旋转 */
transform: rotate(26deg);
transform: rotate(-30deg);
transform: rotate(45deg); /* 关闭按钮 */

/* 平移 */
transform: translateY(-50%);
transform: translateX(-50%);
transform: translate(-50%, -50%); /* 绝对居中 */

/* 3D变换 */
transform: translate3d(-50%, -50%, 0);
```

---

## 交互设计规范

### 1. 按钮状态
```css
/* 默认状态 */
button {
    background: #A72A29;
    color: #FFFFFF;
    cursor: pointer;
    transition: all 0.35s ease;
}

/* Hover状态 */
button:hover {
    background: #FFFFFF;
    color: #A72A29;
}

/* 禁用状态 */
button.disabled,
button:disabled {
    background: #E1E1ED;
    cursor: not-allowed;
    opacity: 0.6;
}

/* 激活状态 */
button.active {
    background: #431616;
}
```

### 2. 链接效果
```css
a {
    color: #FFFFFF;
    text-decoration: none;
    position: relative;
    transition: all 0.35s ease;
}

/* 下划线动画 */
a::after {
    content: '';
    width: 0;
    height: 1px;
    position: absolute;
    right: 0;
    bottom: -5px;
    background: #A72A29;
    transition: all 0.35s ease;
}

a:hover {
    color: #A72A29;
}

a:hover::after {
    width: 100%;
    left: 0;
}
```

### 3. 表单输入
```css
input, textarea {
    height: 60px;
    padding: 0 20px;
    border: 1px solid #DEDEDE;
    background: #F6F6F6;
    font-size: var(--font16);
    color: #222222;
    transition: all 0.35s ease;
}

input:focus,
textarea:focus {
    border-color: #A72A29;
    outline: none;
    box-shadow: none;
}

input::placeholder {
    color: #999999;
}
```

### 4. 下拉选择
```css
.layui-form-select .layui-input {
    background: #F6F6F6;
    border: 1px solid #DEDEDE;
    color: #A72A29; /* 已选项 */
}

.layui-form-select dl dd.layui-this {
    background: #A72A29;
    color: #FFFFFF;
}
```

---

## 图标与图形

### 1. SVG图标规范
```css
.icon {
    width: 1em;
    height: 1em;
    color: currentColor;
}

.icon svg {
    width: 100%;
    height: 100%;
}

.icon svg path {
    fill: currentColor;
    transition: all 0.35s ease;
}
```

### 2. 装饰性图形
```css
/* 斜线装饰 */
.line-decoration {
    width: 1px;
    height: 100%;
    background: rgba(255,255,255,0.1);
    transform: rotate(26deg);
}

/* 三角装饰 */
.triangle::before {
    content: '';
    border-style: solid;
    border-width: 0.5em 0.4em;
    border-color: #A72A29 transparent transparent #A72A29;
}

/* 播放按钮 */
.play-icon {
    border-style: solid;
    border-width: 5.5px 0 5.5px 9px;
    border-color: transparent transparent transparent currentColor;
}
```

### 3. Logo使用
```css
.logo svg path {
    fill: #FFFFFF; /* 深色背景 */
    fill: #A72A29; /* 浅色背景 */
}
```

---

## 特殊效果

### 1. 毛玻璃/模糊背景
```css
.overlay {
    background: rgba(0,0,0,0.6);
    backdrop-filter: blur(10px);
}
```

### 2. 渐变文字
```css
.gradient-text {
    background: #FFFFFF linear-gradient(#A72A29, #431616) no-repeat;
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
}
```

### 3. 阴影效果
```css
/* 轻微阴影 */
box-shadow: 0 2px 8px rgba(0,0,0,0.1);

/* 卡片阴影 */
box-shadow: 0 4px 12px rgba(0,0,0,0.15);

/* 内阴影 */
box-shadow: inset 0 0 5px rgba(0,0,0,0.2);
```

### 4. 遮罩效果
```css
/* 图片遮罩 */
.image-mask {
    -webkit-mask: linear-gradient(to right, rgba(0,0,0,0.5), black);
    mask: linear-gradient(to right, rgba(0,0,0,0.5), black);
}

/* Clip-path */
.clipped {
    -webkit-clip-path: inset(0 0 0 0);
    clip-path: inset(0 0 0 0);
}
```

---

## 页面结构规范

### 1. Banner/Hero区域
```css
.banner {
    width: 100%;
    height: 100vh;
    position: relative;
    background: #000000;
    overflow: hidden;
}

.banner .info-box {
    position: absolute;
    left: 0;
    bottom: 0;
    z-index: 10;
    padding: var(--spacing-60);
}

.banner .title {
    font-family: 'DoHyeon', ...;
    font-size: var(--font72);
    color: #FFFFFF;
    line-height: 1.2;
}
```

### 2. 内容区块
```css
.section {
    width: 100%;
    padding: var(--spacing-120) 0;
    background: #242424;
    position: relative;
    z-index: 1;
}

.section .inner-headline {
    font-family: 'DoHyeon', ...;
    font-size: var(--font38);
    color: #FFFFFF;
    margin-bottom: var(--spacing-60);
}
```

### 3. 卡片布局
```css
.card-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: var(--spacing-30);
}

.card {
    background: #1A1A1A;
    overflow: hidden;
    transition: all 0.35s ease;
}

.card:hover {
    background: #E2E2E2;
    transform: translateY(-5px);
}
```

---

## 辅助类

### 布局辅助
```css
.flex { display: flex; }
.f_column { flex-direction: column; }
.f_row { flex-direction: row; }
.j_center { justify-content: center; }
.j_end { justify-content: flex-end; }
.j_justify { justify-content: space-between; }
.a_center { align-items: center; }
.a_end { align-items: flex-end; }
.flex_wrap { flex-wrap: wrap; }
```

### 显示控制
```css
.public-pc { display: block; }
.public-mb { display: none; }

@media (max-width: 991px) {
    .public-pc { display: none; }
    .public-mb { display: block; }
}
```

### 文字辅助
```css
.text-overflow {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

/* 多行省略 */
.line-clamp-2 {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
}
```

### 动画辅助
```css
.dh {
    transition: all 0.35s ease;
}
```

---

## 最佳实践建议

### 1. 性能优化
- 使用 `transform` 代替 `position` 进行动画
- 使用 `will-change` 优化动画性能
- 图片使用 `object-fit: cover`
- 使用 CSS 变量实现主题

### 2. 可访问性
- 保持足够的对比度（白底黑字 > 4.5:1）
- 为交互元素提供 `:focus` 状态
- 使用语义化 HTML
- 为图标添加 `aria-label`

### 3. 响应式设计
- 移动优先或桌面优先一致性
- 关键断点：991px（平板/手机）、768px（大小手机）
- 字体大小至少 14px（移动端）
- 触摸目标至少 44x44px

### 4. 代码组织
- 使用 CSS 变量管理颜色、间距
- 按模块组织样式
- 遵循 BEM 命名规范
- 使用注释分隔区块

---

## 组件清单

### 必备组件
- ✅ 固定头部导航（带滚动变化）
- ✅ 斜切角按钮（idx-more）
- ✅ 轮播图（Swiper）
- ✅ 卡片网格
- ✅ 表单元素
- ✅ 模态框/弹窗
- ✅ 页脚
- ✅ 移动端菜单
- ✅ 滚动到顶部按钮
- ✅ Cookie提示
- ✅ 搜索框

### 特色组件
- ✅ 视差滚动
- ✅ Canvas动画
- ✅ 视频背景
- ✅ 地图集成
- ✅ 时间轴
- ✅ 数字跳动
- ✅ 图片画廊
- ✅ 产品筛选

---

## 使用说明

### 给AI的指令示例

```
我正在设计一个【具体页面/组件】，请遵循以下设计系统：

1. **色彩**：使用黑色背景（#242424），品牌红色强调（#A72A29），白色文字
2. **字体**：标题使用 DoHyeon 字体，大小 var(--font68)，正文 var(--font16)
3. **布局**：3栏网格布局，间距 var(--spacing-30)，移动端单栏
4. **按钮**：使用斜切角按钮设计（idx-more样式）
5. **动画**：Hover时图片放大1.05倍，过渡时间0.35s
6. **响应式**：991px以下切换为移动布局

请生成完整的HTML和CSS代码。
```

### 设计检查清单

在完成设计后，请检查：
- [ ] 色彩使用符合规范
- [ ] 字体大小和层级正确
- [ ] 间距使用CSS变量
- [ ] 响应式断点完整
- [ ] Hover效果流畅
- [ ] 移动端适配良好
- [ ] 加载性能优化
- [ ] 浏览器兼容性

---

## 技术栈

- **CSS预处理**：原生CSS + CSS变量
- **响应式**：媒体查询 + rem/vw
- **布局**：Flexbox + Grid
- **动画**：CSS Transitions + Keyframes
- **字体**：Web字体 + 系统字体
- **图标**：SVG
- **轮播**：Swiper.js
- **表单**：Layui
- **滚动**：GSAP ScrollTrigger

---

## 版本信息

- **版本号**：V1.0
- **最后更新**：2025
- **维护者**：Johnson Team
- **适用范围**：工业制造业网站、暗黑风格企业站、高端B2B平台

---

## 附录：快速参考

### 常用颜色
```
#A72A29 - 品牌红
#000000 - 纯黑
#242424 - 深灰
#FFFFFF - 纯白
#E2E2E2 - 浅灰
```

### 常用字体大小
```
var(--font72) - 主标题
var(--font38) - 副标题
var(--font26) - 小标题
var(--font18) - 大正文
var(--font16) - 正文
var(--font14) - 辅助文字
```

### 常用间距
```
var(--spacing-30) - 小间距
var(--spacing-60) - 中间距
var(--spacing-100) - 大间距
var(--spacing-120) - 区块间距
```

### 常用过渡
```css
transition: all 0.35s ease; /* 标准 */
transition: all 0.6s ease;  /* 慢速 */
```

---

**使用本提示词时，请根据具体需求调整，但核心设计原则保持不变。**
