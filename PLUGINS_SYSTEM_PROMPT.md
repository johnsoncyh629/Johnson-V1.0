# 网站通用插件系统提示词

## 概述
这是一个通用网站插件集合的CSS库，包含了常用的交互功能插件。这些插件可以快速集成到任何网站项目中，提供标准化的用户交互体验。

---

## 插件清单

### 核心插件列表
1. **wow.min.js** - 页面滚动动画触发器
2. **owo** - 页面入场动画
3. **视频弹窗** - 原生video标签弹窗播放
4. **iframe视频弹窗** - 嵌入式视频（YouTube/Vimeo等）
5. **视频全屏** - HTML5全屏视频播放
6. **图片弹窗** - 图片查看器
7. **投递简历弹窗** - 招聘表单弹窗
8. **Animate.css 3.7.2** - CSS动画库
9. **Swiper 4.5.0** - 轮播图插件
10. **FullPage 4.0.22** - 全屏滚动插件

---

## 色彩变量

```css
:root {
  --color: #005CE6; /* 主题蓝色 */
}
```

**用途**：贯穿所有插件的主题色，用于按钮、链接、高亮等元素。

---

## 1. 滚动动画系统

### WOW.js 配合使用
```css
.wow {
  visibility: hidden;
  animation-name: none;
}
```

### OWO 入场动画
```css
.owo {
  visibility: hidden;
  animation-name: none;
}
```

**使用方法**：
- 在HTML元素上添加 `.wow` 或 `.owo` 类
- 配合 `animated` 和具体动画类使用（如 `fadeInUp`）
- 元素进入视口时自动触发动画

---

## 2. 视频弹窗系统

### 原生视频弹窗 (#hi-video-pop)

```css
#hi-video-pop {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.7);
}
```

**特点**：
- 暗色半透明遮罩（70%透明度）
- 垂直水平居中布局
- 白色边框包裹视频
- 圆形关闭按钮（底部居中，85%高度位置）
- 响应式：移动端最大宽度90%

**关闭按钮样式**：
```css
.hi-close {
  width: 40px;
  height: 40px;
  background: #FFFFFF;
  border-radius: 50%;
}

.hi-close:hover {
  background: #005CE6; /* 主题色 */
}
```

### iframe视频弹窗 (#hi-iframe-video)

**用途**：嵌入YouTube、Vimeo等第三方视频

```css
#hi-iframe-video iframe {
  width: 100vh;
  height: 60vh;
  max-width: 90%;
  max-height: 70%;
}

@media (max-width: 991px) {
  #hi-iframe-video iframe {
    width: 90vw;
    height: 60vw;
  }
}
```

### 全屏视频 (#hi-video-pop2)

```css
#hi-video-pop2 {
  display: none;
  height: 0;
  width: 0;
}
```

**用途**：触发HTML5全屏API，无需UI

---

## 3. 图片弹窗 (#hi-img-pop)

```css
#hi-img-pop > img {
  position: fixed;
  left: 50%;
  top: 50%;
  max-width: 90%;
  max-height: 65%;
  transform: translate(-50%, -50%);
}
```

**特点**：
- 图片最大宽度90%、最大高度65%
- 自动居中显示
- 保持图片原始比例
- 与视频弹窗共享关闭按钮样式

---

## 4. 投递简历弹窗 (#hi-resume-pop)

### 整体布局
```css
#hi-resume-pop form {
  width: 90%;
  max-width: 500px;
  background: #FFFFFF;

  /* 响应式 */
  @media (max-width: 1580px) {
    max-width: 400px;
  }
}
```

### 头部设计
```css
.hi-title-box {
  padding: 0 0.4rem;
  background: #005CE6; /* 主题蓝色背景 */
}

.hi-title {
  line-height: 0.8rem;
  font-size: 20px;
  color: #FFFFFF;
}
```

### 表单元素
```css
/* 输入框 */
.hi-box input {
  height: 0.6rem;
  border: 1px solid #cccccc;
  padding: 0 0.15rem;
}

/* 提交按钮 */
.hi-box button {
  width: 100%;
  height: 0.6rem;
  background: #005CE6;
  color: #FFFFFF;
}

/* 文件上传按钮 */
.hi-input-box {
  background: #005CE6;
  color: #FFFFFF;
  padding: 0.05rem 0.15rem;
}
```

### 验证码布局
```css
.hi-code-box {
  display: flex;
  justify-content: space-between;
}

.hi-code-box input {
  width: calc(100% - 1.4rem);
}

.hi-code-box img {
  max-width: 1.3rem;
  max-height: 0.6rem;
}
```

---

## 5. Animate.css 动画库

### 动画分类

#### 弹跳系列 (Bounce)
```css
.bounce          /* 弹跳 */
.bounceIn        /* 弹入 */
.bounceInDown    /* 从上弹入 */
.bounceInLeft    /* 从左弹入 */
.bounceInRight   /* 从右弹入 */
.bounceInUp      /* 从下弹入 */
.bounceOut       /* 弹出 */
.bounceOutDown   /* 向下弹出 */
.bounceOutLeft   /* 向左弹出 */
.bounceOutRight  /* 向右弹出 */
.bounceOutUp     /* 向上弹出 */
```

#### 淡入淡出系列 (Fade)
```css
.fadeIn          /* 淡入 */
.fadeInDown      /* 从上淡入 */
.fadeInLeft      /* 从左淡入 */
.fadeInRight     /* 从右淡入 */
.fadeInUp        /* 从下淡入 - 常用！*/
.fadeOut         /* 淡出 */
.fadeOutDown     /* 向下淡出 */
.fadeOutLeft     /* 向左淡出 */
.fadeOutRight    /* 向右淡出 */
.fadeOutUp       /* 向上淡出 */
```

#### 翻转系列 (Flip)
```css
.flip            /* 翻转 */
.flipInX         /* X轴翻入 */
.flipInY         /* Y轴翻入 */
.flipOutX        /* X轴翻出 */
.flipOutY        /* Y轴翻出 */
```

#### 缩放系列 (Zoom)
```css
.zoomIn          /* 放大进入 */
.zoomInDown      /* 从上放大进入 */
.zoomInLeft      /* 从左放大进入 */
.zoomInRight     /* 从右放大进入 */
.zoomInUp        /* 从下放大进入 */
.zoomOut         /* 缩小退出 */
.zoomOutDown     /* 向下缩小退出 */
.zoomOutLeft     /* 向左缩小退出 */
.zoomOutRight    /* 向右缩小退出 */
.zoomOutUp       /* 向上缩小退出 */
```

#### 滑动系列 (Slide)
```css
.slideInDown     /* 从上滑入 */
.slideInLeft     /* 从左滑入 */
.slideInRight    /* 从右滑入 */
.slideInUp       /* 从下滑入 */
.slideOutDown    /* 向下滑出 */
.slideOutLeft    /* 向左滑出 */
.slideOutRight   /* 向右滑出 */
.slideOutUp      /* 向上滑出 */
```

#### 特殊效果系列
```css
.flash           /* 闪烁 */
.pulse           /* 脉冲 */
.rubberBand      /* 橡皮筋 */
.shake           /* 抖动 */
.headShake       /* 摇头 */
.swing           /* 摇摆 */
.tada            /* 跳动强调 */
.wobble          /* 摇晃 */
.jello           /* 果冻效果 */
.heartBeat       /* 心跳 */
.lightSpeedIn    /* 光速进入 */
.lightSpeedOut   /* 光速退出 */
.rotateIn        /* 旋转进入 */
.rotateOut       /* 旋转退出 */
.rollIn          /* 滚入 */
.rollOut         /* 滚出 */
.hinge           /* 铰链掉落 */
.jackInTheBox    /* 玩偶盒 */
```

### 动画控制类

```css
/* 基础类 - 必须添加 */
.animated        /* 启用动画 */

/* 时长控制 */
.fast            /* 0.8s */
.faster          /* 0.5s */
.slow            /* 2s */
.slower          /* 3s */

/* 延迟控制 */
.delay-1s        /* 延迟1秒 */
.delay-2s        /* 延迟2秒 */
.delay-3s        /* 延迟3秒 */
.delay-4s        /* 延迟4秒 */
.delay-5s        /* 延迟5秒 */

/* 循环播放 */
.infinite        /* 无限循环 */
```

### 使用示例

```html
<!-- 基础用法 -->
<div class="animated fadeInUp">内容</div>

<!-- 带延迟 -->
<div class="animated fadeInUp delay-1s">延迟1秒出现</div>

<!-- 快速动画 -->
<div class="animated bounceIn faster">快速弹入</div>

<!-- 无限循环 -->
<div class="animated pulse infinite">持续脉冲</div>

<!-- 配合WOW.js -->
<div class="wow animated fadeInUp" data-wow-delay="0.3s">
  滚动到视口时触发
</div>
```

### 推荐搭配

| 场景 | 推荐动画 | 说明 |
|------|---------|------|
| 标题入场 | `fadeInUp` | 从下淡入，专业感强 |
| 卡片入场 | `fadeIn` / `zoomIn` | 简洁或有趣味性 |
| 按钮强调 | `pulse` / `heartBeat` | 吸引点击 |
| 错误提示 | `shake` / `headShake` | 明确表达错误 |
| 成功提示 | `bounceIn` / `tada` | 积极正面反馈 |
| 删除动画 | `fadeOutUp` / `zoomOut` | 优雅退出 |
| 页面切换 | `slideInRight` + `slideOutLeft` | 流畅过渡 |

---

## 6. Swiper 轮播插件 (v4.5.0)

### 基础结构

```html
<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">Slide 1</div>
    <div class="swiper-slide">Slide 2</div>
    <div class="swiper-slide">Slide 3</div>
  </div>
  <!-- 分页器 -->
  <div class="swiper-pagination"></div>
  <!-- 导航按钮 -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
  <!-- 滚动条 -->
  <div class="swiper-scrollbar"></div>
</div>
```

### 容器设置

```css
.swiper-container {
  position: relative;
  overflow: hidden;
  z-index: 1;
}

.swiper-wrapper {
  position: relative;
  width: 100%;
  height: 100%;
  z-index: 1;
  display: flex;
  box-sizing: content-box;
}

.swiper-slide {
  width: 100%;
  height: 100%;
  flex-shrink: 0;
}
```

### 导航按钮

```css
.swiper-button-prev,
.swiper-button-next {
  position: absolute;
  top: 50%;
  width: 27px;
  height: 44px;
  margin-top: -22px;
  z-index: 10;
  cursor: pointer;
}

.swiper-button-prev {
  left: 10px;
}

.swiper-button-next {
  right: 10px;
}

/* 颜色变体 */
.swiper-button-white  /* 白色箭头 */
.swiper-button-black  /* 黑色箭头 */
```

### 分页器样式

```css
/* 圆点分页 */
.swiper-pagination-bullet {
  width: 8px;
  height: 8px;
  border-radius: 100%;
  background: #000000;
  opacity: 0.2;
}

.swiper-pagination-bullet-active {
  opacity: 1;
  background: #007aff;
}

/* 分页器位置 */
.swiper-pagination-bullets  /* 底部 */
.swiper-pagination-fraction /* 分数显示 */
.swiper-pagination-progressbar /* 进度条 */
```

### 特殊效果

```css
/* 3D效果 */
.swiper-container-3d {
  perspective: 1200px;
}

/* 淡入淡出 */
.swiper-container-fade .swiper-slide {
  pointer-events: none;
  transition-property: opacity;
}

/* 立方体 */
.swiper-container-cube

/* 翻转 */
.swiper-container-flip

/* 3D流 */
.swiper-container-coverflow
```

### 响应式设置

```css
/* 自动高度 */
.swiper-container-autoheight

/* 垂直方向 */
.swiper-container-vertical

/* 多行显示 */
.swiper-container-multirow

/* 自由模式 */
.swiper-container-free-mode
```

### 懒加载

```css
.swiper-lazy-preloader {
  width: 42px;
  height: 42px;
  animation: swiper-preloader-spin 1s steps(12, end) infinite;
}
```

---

## 7. FullPage 全屏滚动 (v4.0.22)

### 基础结构

```html
<div id="fullpage">
  <div class="section">第一屏</div>
  <div class="section">第二屏</div>
  <div class="section">
    <div class="slide">水平滑动1</div>
    <div class="slide">水平滑动2</div>
  </div>
</div>
```

### 核心样式

```css
/* 禁用页面滚动 */
.fp-enabled body,
html.fp-enabled {
  margin: 0;
  padding: 0;
  overflow: hidden;
}

/* 区块 */
.fp-section {
  position: relative;
  box-sizing: border-box;
  height: 100%;
  display: block;
}

/* 水平滑动 */
.fp-slides {
  z-index: 1;
  height: 100%;
  overflow: hidden;
  position: relative;
  transition: all 0.3s ease-out;
}
```

### 侧边导航

```css
#fp-nav {
  position: fixed;
  z-index: 100;
  top: 50%;
  opacity: 1;
  transform: translateY(-50%);
}

#fp-nav.fp-right {
  right: 17px;
}

#fp-nav.fp-left {
  left: 17px;
}

/* 导航圆点 */
#fp-nav ul li a span {
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background: #333333;
}

/* 激活状态 */
#fp-nav ul li a.active span {
  width: 12px;
  height: 12px;
}

/* Hover状态 */
#fp-nav ul li:hover a span {
  width: 10px;
  height: 10px;
}
```

### 工具提示

```css
#fp-nav ul li .fp-tooltip {
  position: absolute;
  top: -2px;
  color: #FFFFFF;
  font-size: 14px;
  opacity: 0;
  transition: opacity 0.2s ease-in;
}

#fp-nav ul li:hover .fp-tooltip {
  opacity: 1;
}
```

### 箭头控制

```css
.fp-controlArrow {
  position: absolute;
  z-index: 4;
  top: 50%;
  cursor: pointer;
  margin-top: -38px;
}

.fp-prev {
  left: 15px;
}

.fp-next {
  right: 15px;
}
```

### 特殊类

```css
.fp-auto-height          /* 自动高度 */
.fp-scrollable           /* 可滚动 */
.fp-responsive           /* 响应式 */
.fp-notransition         /* 禁用过渡 */
.fp-is-overflow          /* 内容溢出 */
```

### 滚动条样式（Mac）

```css
.fp-scroll-mac .fp-overflow::-webkit-scrollbar {
  background-color: transparent;
  width: 9px;
}

.fp-scroll-mac .fp-overflow::-webkit-scrollbar-thumb {
  background-color: rgba(0, 0, 0, 0.4);
  border-radius: 16px;
  border: 4px solid transparent;
}
```

---

## 通用设计规范

### 弹窗系统共同特点

**层级规范**：
```css
z-index: 1000  /* 视频弹窗 */
z-index: 1000  /* 图片弹窗 */
z-index: 999   /* 简历弹窗 */
```

**遮罩样式**：
```css
background: rgba(0, 0, 0, 0.7);  /* 视频/图片 */
background: rgba(0, 0, 0, 0.7);  /* 简历 */
background: rgba(0, 0, 0, 0.5);  /* iframe视频 */
```

**关闭按钮规范**：
- 尺寸：40x40px
- 形状：圆形（border-radius: 50%）
- 位置：top: 85%, left: 50%
- 默认：白色背景
- Hover：主题色背景（#005CE6）
- 动画：transition: 0.4s

**居中方式**：
```css
/* 绝对居中 */
position: fixed;
left: 50%;
top: 50%;
transform: translate(-50%, -50%);
```

### 响应式断点

```css
@media (max-width: 1580px) { /* 笔记本 */ }
@media (max-width: 991px)  { /* 平板 */ }
@media (max-width: 767px)  { /* 手机 */ }
```

### 过渡动画

```css
transition: 0.4s;          /* 按钮、小元素 */
transition: 0.3s ease-out; /* 轮播切换 */
transition: 0.2s ease-in;  /* 提示显示 */
transition: 0.1s ease-in-out; /* 微交互 */
```

---

## 使用建议

### 1. 插件选择

**轮播需求**：
- 简单banner → Swiper基础模式
- 产品展示 → Swiper + 缩略图
- 全屏切换 → FullPage

**动画需求**：
- 页面加载 → Animate.css
- 滚动触发 → WOW.js + Animate.css
- 复杂动画 → 自定义CSS动画

**弹窗需求**：
- 视频展示 → #hi-video-pop
- 第三方视频 → #hi-iframe-video
- 图片查看 → #hi-img-pop
- 表单提交 → #hi-resume-pop

### 2. 性能优化

**Animate.css优化**：
```css
/* 只引入需要的动画 */
@import 'animate/fadeIn.css';
@import 'animate/fadeOut.css';
```

**Swiper优化**：
- 使用 `lazy loading` 延迟加载图片
- 设置 `slidesPerView: 'auto'` 按需加载
- 禁用不需要的模块

**FullPage优化**：
- 设置 `lazyLoading: true`
- 使用 `scrollOverflow: false` 如果不需要内部滚动
- 移动端考虑使用 `responsiveWidth` 禁用

### 3. 兼容性考虑

**浏览器兼容**：
- IE9+：需要polyfill (Swiper v4)
- 移动端：添加 `-webkit-` 前缀
- Safari：注意 `transform` 和 `transition`

**触摸优化**：
```css
-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
-ms-touch-action: pan-y;
touch-action: pan-y;
```

### 4. 主题定制

**修改主题色**：
```css
:root {
  --color: #YOUR_COLOR; /* 替换主题色 */
}
```

**影响范围**：
- 弹窗hover状态
- 简历表单按钮
- Swiper默认分页器
- FullPage导航点

---

## 快速集成指南

### 基础HTML模板

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- 引入插件CSS -->
  <link rel="stylesheet" href="plugins.css">
</head>
<body>

  <!-- 视频弹窗 -->
  <div id="hi-video-pop">
    <div class="hi-close"></div>
    <div class="hi-video-box">
      <div class="hi-video-wrap">
        <video src="" controls></video>
      </div>
    </div>
  </div>

  <!-- 图片弹窗 -->
  <div id="hi-img-pop">
    <div class="hi-close"></div>
    <img src="" alt="">
  </div>

  <!-- 引入插件JS -->
  <script src="swiper.min.js"></script>
  <script src="wow.min.js"></script>
  <script src="fullpage.min.js"></script>

  <script>
    // 初始化WOW
    new WOW().init();

    // 初始化Swiper
    var swiper = new Swiper('.swiper-container', {
      // 配置项
    });

    // 初始化FullPage
    new fullpage('#fullpage', {
      // 配置项
    });
  </script>
</body>
</html>
```

---

## 常见问题

### Q: 如何更改弹窗背景透明度？
```css
#hi-video-pop {
  background: rgba(0, 0, 0, 0.9); /* 调整第4个值 */
}
```

### Q: 如何禁用Animate.css的某些动画？
```css
.animated.fadeIn {
  animation: none !important;
}
```

### Q: Swiper分页器位置如何调整？
```css
.swiper-pagination {
  bottom: 20px; /* 调整位置 */
}
```

### Q: FullPage如何在移动端禁用？
```javascript
new fullpage('#fullpage', {
  responsiveWidth: 768, // 小于768px禁用
});
```

---

## 版本信息

| 插件 | 版本 | 官网 |
|------|------|------|
| Animate.css | 3.7.2 | https://animate.style/ |
| Swiper | 4.5.0 | https://www.swiper.com.cn |
| FullPage | 4.0.22 | https://alvarotrigo.com/fullPage/ |

---

## 许可协议

- **Animate.css**: MIT License
- **Swiper**: MIT License
- **FullPage**: GPLv3（开源）/ Commercial License（商业）

---

**使用本插件集合时，请根据具体需求选择合适的插件，避免引入不必要的代码以保持性能。**
