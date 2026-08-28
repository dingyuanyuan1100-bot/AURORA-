# AURORA 极光汽车 · 品牌科技网站

> 一个充满未来感的虚构汽车品牌官网，蓝色渐变视觉体系，丰富的交互动画与多页面体验。

![AURORA](https://aka.doubaocdn.com/s/PyC1OCJ6g3)

## 项目简介

**AURORA（极光汽车）** 是一个虚构的未来智能出行品牌，创立于 2042 年，定位为「以极光之名，重新定义速度」。本项目是该品牌的官方网站，采用单文件原生前端实现，包含 5 个独立页面与全套交互动效。

## 功能特性

### 多页面结构（Hash 路由）

| 页面 | 路由 | 内容 |
|------|------|------|
| 首页 | `#/home` | Hero 主视觉、核心数据、旗舰车型预告、技术亮点、车型预览、品牌理念 |
| 车型 | `#/models` | 4 款车型详情卡、分类筛选、全参数对比表 |
| 技术 | `#/tech` | 全固态能量舱、全息智舱 OS、LUMEN Drive 智驾、智驾等级演进 |
| 品牌 | `#/about` | 品牌故事、三大价值观、2042–2050 大事记时间线 |
| 预约 | `#/contact` | 试驾预约表单、联系信息、FAQ 手风琴 |

### 交互动画

- **点击爆裂粒子** — 全站任意点击位置迸发蓝青色光爆（Canvas 粒子物理 + 发光）
- **打字机轮播** — Hero 区标语循环打字 + 光标闪烁
- **滚动视差** — Hero 背景随滚动位移，营造纵深
- **落地窗 Reveal** — 区块滚动进入时从下方/侧向整块滑入（IntersectionObserver，延迟交错）
- **极光滚动进度条** — 顶部流光进度条，随页面滚动填充
- **数字滚动计数** — 数据指标进入视口时从 0 递增到目标值
- **3D 卡片倾斜** — 车型卡 / 预告卡跟随鼠标做透视旋转
- **鼠标跟随光晕** — 柔和青色径向光跟随光标
- **导航吸顶模糊** — 滚动后导航栏毛玻璃化
- **车型筛选 / FAQ 折叠 / 表单提交动效 / 返回顶部**

### 视觉体系

- 深蓝夜空底 `#04070f` + 品牌青蓝渐变 `#1a6bff → #37d6ff`
- 玻璃拟态卡片（backdrop-filter）+ 发光描边
- Orbitron 科技展示字体 + Noto Sans SC 正文字体
- 9 张 AI 生成的统一风格概念车视觉素材

## 技术栈

- **HTML5** — 语义化结构，单文件自包含
- **CSS3** — 自定义属性（CSS Variables）、Grid / Flex、动画与过渡、响应式媒体查询
- **原生 JavaScript（ES6+）** — 无框架、无构建工具
- **Canvas 2D** — 点击粒子爆裂效果
- **IntersectionObserver** — 滚动触发动画
- **Hash Router** — 页内多视图切换

## 快速开始

无需安装任何依赖，直接用浏览器打开即可：

```bash
# 克隆仓库
git clone https://github.com/dingyuanyuan1100-bot/AURORA-.git

# 进入目录
cd AURORA-

# 直接用浏览器打开
# Windows:
start index.html
# macOS:
open index.html
# Linux:
xdg-open index.html
```

或者启动一个本地静态服务器：

```bash
# Python 3
python -m http.server 8080

# 然后访问 http://localhost:8080
```

## 项目结构

```
AURORA-/
├── index.html    # 网站主文件（HTML + CSS + JS 全部内联）
├── README.md     # 项目说明
└── LICENSE       # 开源协议
```

## 浏览器兼容

支持所有现代浏览器（Chrome / Edge / Firefox / Safari 最新版）。动画遵循 `prefers-reduced-motion` 系统设置，用户开启「减少动态效果」时自动关闭动画。

## 部署

本项目为纯静态网站，可部署到任意静态托管服务：

- **GitHub Pages** — 仓库 Settings → Pages → 选择 `main` 分支根目录
- **Vercel / Netlify** — 直接导入仓库，零配置部署
- **Nginx / Apache** — 将 `index.html` 放入站点根目录

## 许可证

MIT License — 详见 [LICENSE](LICENSE)。

---

> 本项目为虚构品牌演示网站，所有车型、参数、品牌故事均为虚构，仅用于前端设计与交互展示。
