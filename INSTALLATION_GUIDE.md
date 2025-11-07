# Black Friday Banner Installation Guide

## 📦 包含文件

1. **black-friday-banner.liquid** - 主页宽屏Banner（带倒计时）
2. **black-friday-collection-banner.liquid** - Collections页面简化Banner

---

## 🚀 安装步骤

### 方法一：通过Shopify管理后台上传（推荐）

#### 1. 上传Section文件

1. 登录您的Shopify管理后台
2. 进入 **Online Store** → **Themes**
3. 点击当前主题的 **Actions** → **Edit code**
4. 在左侧文件列表中找到 **Sections** 文件夹
5. 点击 **Add a new section**
6. 分别创建以下两个文件：
   - 复制 `black-friday-banner.liquid` 的内容，命名为 `black-friday-banner`
   - 复制 `black-friday-collection-banner.liquid` 的内容，命名为 `black-friday-collection-banner`
7. 点击 **Save** 保存

#### 2. 添加到主页

1. 返回 **Online Store** → **Themes**
2. 点击 **Customize** 进入主题编辑器
3. 选择 **Home** 页面
4. 点击顶部的 **Add section**
5. 在 **Custom** 分类下找到 **Black Friday Banner**
6. 将其拖到页面最顶部（Header下方）
7. 点击 **Save** 发布

#### 3. 添加到Collections页面

1. 在主题编辑器中，切换到 **Collections** → **Default collection**
2. 点击 **Add section**
3. 选择 **Black Friday Collection Banner**
4. 拖到合适位置（建议在产品列表上方）
5. 点击 **Save**

---

## ⚙️ 配置选项

### 主页Banner设置项

在主题编辑器中点击Banner Section可以看到以下设置：

| 设置项 | 默认值 | 说明 |
|--------|--------|------|
| Enable Banner | ✅ Checked | 开启/关闭Banner |
| Main Title | BLACK FRIDAY SALE | 主标题 |
| Subtitle | Up to 20% OFF | 优惠信息 |
| Dealer Note | Exclusive offer for... | 经销商提示文字 |
| Start Date | 2025-11-07 | 活动开始日期 |
| End Date | 2025-12-01 | 活动结束日期（倒计时截止） |
| Button Link | https://de.lokithorshop.com/... | 跳转链接 |
| Button Text | Order Now | 按钮文字 |
| Primary Color | #ac1d23 | 主色调 |
| Secondary Color | #a9abb2 | 辅助色 |

### Collection Banner设置项

| 设置项 | 默认值 | 说明 |
|--------|--------|------|
| Enable Banner | ✅ Checked | 开启/关闭Banner |
| Banner Title | BLACK FRIDAY SALE | 标题 |
| Banner Subtitle | Up to 20% OFF | 副标题 |
| Banner Note | For Dealers Only | 简短提示 |
| Start Date | 2025-11-07 | 活动开始日期 |
| End Date | 2025-12-01 | 活动结束日期 |
| Primary Color | #ac1d23 | 主色调 |
| Secondary Color | #a9abb2 | 辅助色 |

---

## 📱 功能特性

### ✨ 主页宽屏Banner
- ⚡ 闪电动画图标
- ⏱️ 实时倒计时（天/时/分/秒）
- 🎯 专业工具风格渐变背景
- 📱 完全响应式设计
- ❌ 可关闭按钮（刷新后再显示）
- 🔗 CTA按钮带悬停动画
- 📅 自动在活动期间显示/隐藏

### 🎨 Collection页面Banner
- 简洁的条形Banner设计
- ⏱️ 紧凑型倒计时
- 📱 移动端自适应
- ❌ 可关闭功能
- 🏷️ "For Dealers Only"标签

---

## 🎯 设计亮点

### 专业B2B风格
- 工业级渐变背景（红色系）
- 金色强调色（#FFD700）
- Roboto专业字体
- 微妙的网格纹理背景
- 阴影和悬停效果

### 移动端优化
- 断点：968px, 640px, 480px
- 字体和间距自动调整
- 倒计时在小屏幕上紧凑显示
- 图标在移动端隐藏以节省空间

---

## 🔧 高级定制

### 修改颜色
在主题编辑器中直接调整：
- **Primary Color**：主背景渐变色
- **Secondary Color**：边框颜色

### 修改文案
所有文字都可在主题编辑器中直接修改，支持多语言。

### 修改动画
如需调整动画效果，编辑代码中的CSS：
```css
/* 闪电图标脉冲动画 */
@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.8; transform: scale(1.05); }
}

/* Collection页面图标发光动画 */
@keyframes glow {
  0%, 100% { filter: drop-shadow(0 0 3px #FFD700); }
  50% { filter: drop-shadow(0 0 8px #FFD700); }
}
```

---

## 📋 检查清单

安装完成后，请检查：

- [ ] 两个Section文件已成功上传
- [ ] 主页Banner显示在页面顶部
- [ ] Collection页面Banner显示正常
- [ ] 倒计时正常运行
- [ ] 按钮链接正确（跳转到黑五促销页）
- [ ] 移动端显示正常（测试不同设备）
- [ ] 关闭按钮工作正常
- [ ] 活动日期设置正确
- [ ] 颜色和文字符合品牌要求

---

## 🛠️ 故障排除

### Banner不显示？
1. 检查 "Enable Banner" 是否勾选
2. 确认当前日期在活动日期范围内
3. 检查浏览器控制台是否有JavaScript错误
4. 清除浏览器缓存

### 倒计时不工作？
1. 检查日期格式是否正确（YYYY-MM-DD）
2. 确保结束日期晚于当前日期
3. 查看浏览器控制台错误信息

### 移动端显示异常？
1. 清除移动设备缓存
2. 检查主题CSS是否与Banner冲突
3. 使用浏览器开发者工具测试响应式断点

---

## 📞 技术支持

如有问题，请检查：
1. Shopify主题是否为2.0版本（支持Section everywhere）
2. 浏览器是否支持现代CSS和JavaScript
3. 主题是否有冲突的CSS样式

---

## 📄 许可证

此代码使用开源字体 **Roboto**（Apache License 2.0），可安全用于商业项目。

---

**祝黑五促销活动成功！** 🎉
