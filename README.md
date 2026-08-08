<div align="center">

# 💣 MINESWEEPER X

### 暗夜矿场 · 神经突触

一款用纯 JavaScript 打造的现代化扫雷游戏，告别 Win98 灰色时代。

![License](https://img.shields.io/badge/License-MIT-FFB627?style=for-the-badge)
![Tech](https://img.shields.io/badge/纯原生-JavaScript_+_CSS-00D4FF?style=for-the-badge)
![Difficulty](https://img.shields.io/badge/难度-4种模式-00FF9D?style=for-the-badge)
![Dependencies](https://img.shields.io/badge/依赖-零运行时依赖-FF3860?style=for-the-badge)

</div>

---

## 📑 目录

- [✨ 特性概览](#-特性概览)
- [🎮 游戏模式](#-游戏模式)
- [🚀 快速开始](#-快速开始)
- [🎯 操作说明](#-操作说明)
- [🎨 设计理念](#-设计理念)
- [🏗️ 项目结构](#️-项目结构)
- [🛠️ 技术栈](#-技术栈)
- [🔧 核心算法](#-核心算法)
- [📱 浏览器支持](#-浏览器支持)
- [🤝 贡献指南](#-贡献指南)
- [📝 开发计划](#-开发计划)
- [📄 许可证](#-许可证)
- [🙏 致谢](#-致谢)

---

## ✨ 特性概览

| 类别 | 功能 |
|:---:|:---|
| 🎮 经典玩法 | 完整还原传统扫雷的核心机制：左键揭开 / 右键标记 / 双击展开 |
| 🎨 现代视觉 | 暗夜矿场主题，霓虹质感，金属凸起格子，告别 Win98 灰色 |
| ⚡ 零依赖 | 纯 HTML + CSS + JavaScript，无任何运行时框架或库 |
| 📱 响应式 | 完美适配桌面、平板、移动设备，格子尺寸自动计算 |
| 🏆 本地存档 | 自动保存最佳成绩、游戏统计、连胜记录至 `localStorage` |
| 💡 智能提示 | 内置安全格提示系统，优先推荐有数字相邻的格子 |
| ⌨️ 全键盘支持 | `R` 重开 / `H` 提示 / `1-3` 切换难度 / `ESC` 关闭模态 |
| 🎯 四种难度 | 初级 9×9 / 中级 16×16 / 高级 30×16 / 自定义任意规模 |
| 🔒 首点保护 | 第一次点击保证安全，且周围 8 格均无雷 |
| 🖱️ Chord 操作 | 双击数字格，若周围旗数与数字相等，自动揭开剩余格 |
| 🎭 表情反馈 | 笑脸按钮根据游戏状态切换表情：微笑 / 惊讶 / 庆祝 / 哭脸 |
| 🎉 视觉特效 | 背景粒子流动、胜利彩纸飘落、踩雷屏幕震动 |

---

## 🎮 游戏模式

| 难度 | 规模 | 雷数 | 适合人群 | 估计耗时 |
|:---:|:---:|:---:|:---:|:---:|
| 🌱 初级 | 9 × 9 | 10 | 新手入门 | 1–3 min |
| 🔥 中级 | 16 × 16 | 40 | 进阶挑战 | 5–10 min |
| 💀 高级 | 30 × 16 | 99 | 高手对决 | 15–30 min |
| 🎛️ 自定义 | 任意 | 任意 | 自由发挥 | 自定义 |

---

## 🚀 快速开始

### 方式一：直接下载运行

```bash
# 克隆仓库
git clone  https://aventardo7777.github.io/minesweeper-x/

# 进入项目目录
cd minesweeper-x
```

直接在浏览器中打开 `index.html` 即可开始游戏。

### 方式二：使用本地服务器（推荐）

```bash
# 使用 Python
python -m http.server 8000

# 或使用 Node.js（需先安装 http-server）
npx http-server -p 8000
```

然后访问 [http://localhost:8000](http://localhost:8000)

### 方式三：在线体验

访问 GitHub Pages 部署版本：[Demo Link](https://Aventardo7777.github.io/minesweeper-x/)

---

## 🎯 操作说明

### 鼠标操作

| 操作 | 效果 |
|:---|:---|
| **左键点击** | 揭开格子 |
| **右键点击** | 标记 / 取消旗子 |
| **双击数字格** | 若周围旗数 = 数字，自动揭开剩余格 |

### 键盘快捷键

| 按键 | 功能 |
|:---:|:---|
| `R` | 重新开始当前难度 |
| `H` | 获取提示（+10 秒惩罚） |
| `1` | 切换到初级难度 |
| `2` | 切换到中级难度 |
| `3` | 切换到高级难度 |
| `ESC` | 关闭胜利模态框 |

### 游戏规则

1. **目标** —— 揭开所有非雷格子即可获胜。
2. **数字含义** —— 数字 N 表示周围 8 格中有 N 颗雷。
3. **空白展开** —— 揭开数字为 0 的格子时，自动展开周围所有空白区域。
4. **旗子标记** —— 右键标记可疑格子，避免误触。
5. **Chord 操作** —— 双击已揭开的数字格，若周围旗数 = 数字，自动揭开剩余未标记格。
6. **首点保护** —— 第一次点击保证安全，且周围 8 格也无雷。

---

## 🎨 设计理念

### 配色方案

| 颜色 | 用途 | HEX | 色块 |
|:---:|:---:|:---:|:---:|
| 🟡 琥珀金 | 主色调（旗子、强调） | `#FFB627` | ![](https://img.shields.io/badge/-FFB627-FFB627) |
| 🟢 翡翠绿 | 安全 / 胜利 | `#00FF9D` | ![](https://img.shields.io/badge/-00FF9D-00FF9D) |
| 🔴 警示红 | 危险 / 失败 / 计数器 | `#FF3860` | ![](https://img.shields.io/badge/-FF3860-FF3860) |
| 🔵 信息青 | 提示 / 进度 | `#00D4FF` | ![](https://img.shields.io/badge/-00D4FF-00D4FF) |
| ⚫ 深炭蓝 | 背景基色 | `#0A0E1A` | ![](https://img.shields.io/badge/-0A0E1A-0A0E1A) |

### 数字配色

经典扫雷的 8 种数字颜色，调整为暗色背景下的高对比版本：

| 数字 | 颜色 | 含义 |
|:---:|:---:|:---|
| 1 | 亮蓝 `#4DABF7` | 周围 1 雷 |
| 2 | 亮绿 `#51CF66` | 周围 2 雷 |
| 3 | 亮红 `#FF6B6B` | 周围 3 雷 |
| 4 | 紫色 `#CC5DE8` | 周围 4 雷 |
| 5 | 橙色 `#FF922B` | 周围 5 雷 |
| 6 | 青色 `#22D3EE` | 周围 6 雷 |
| 7 | 粉色 `#F783AC` | 周围 7 雷 |
| 8 | 白色 `#E8EEF5` | 周围 8 雷 |

### 字体系统

- **Orbitron** — 科技感标题字体，用于 Logo 与小标题
- **Space Grotesk** — 现代正文字体，用于界面文本
- **JetBrains Mono** — 等宽字体，用于数字与计时器

### 视觉细节

- **金属凸起格子** — 未揭开格子使用渐变 + 内阴影模拟金属凸起
- **凹陷已揭开** — 揭开格子使用反向阴影模拟凹陷
- **霓虹发光** — 数字、旗子、雷均有彩色光晕
- **微动画** — 揭开缩放动画、旗子放置旋转、爆炸放大
- **背景粒子** — 60 个流动粒子 + 距离连线，营造科技氛围

---

## 🏗️ 项目结构

```
minesweeper-x/
├── index.html              # 主页面（含 CSS 与 JS，单文件部署）
├── README.md               # 项目文档（本文件）
├── LICENSE                 # MIT 许可证
├── CONTRIBUTING.md         # 贡献指南
├── .gitignore              # Git 忽略规则
└── docs/
    ├── screenshot.png      # 游戏截图
    └── demo.gif            # 演示动图
```

---

## 🛠️ 技术栈

| 技术 | 用途 | 选择理由 |
|:---:|:---|:---|
| **HTML5** | 语义化结构 | 原生支持，无依赖 |
| **CSS3** | 样式与动画 | Grid 布局、自定义属性、Keyframes |
| **JavaScript ES6+** | 游戏逻辑 | Class、Arrow Function、Template Literal |
| **Tailwind CSS (CDN)** | 工具类样式 | 快速布局，零构建 |
| **Font Awesome 6** | 图标库 | 完整的图标生态 |
| **Google Fonts** | 字体服务 | Orbitron / Space Grotesk / JetBrains Mono |
| **localStorage** | 数据持久化 | 无需后端，自动保存进度 |
| **Canvas API** | 背景粒子 | 原生绘制，性能优秀 |
| **Web Animations API** | 胜利粒子 | 流畅的 JS 动画 |

---

## 🔧 核心算法

### 1. 首点保护算法

```javascript
placeMines(safeRow, safeCol) {
  // 计算首点周围 8 格作为安全区
  const safeCells = new Set();
  for (let dr = -1; dr <= 1; dr++) {
    for (let dc = -1; dc <= 1; dc++) {
      const r = safeRow + dr;
      const c = safeCol + dc;
      if (this.inBounds(r, c)) {
        safeCells.add(`${r},${c}`);
      }
    }
  }
  // 随机布雷时跳过安全区
  while (minesPlaced < totalMines) {
    const r = Math.floor(Math.random() * rows);
    const c = Math.floor(Math.random() * cols);
    if (!safeCells.has(`${r},${c}`) && !board[r][c].isMine) {
      board[r][c].isMine = true;
      minesPlaced++;
    }
  }
}
```

### 2. BFS 自动展开

当揭开一个空白格（周围雷数为 0）时，使用广度优先搜索自动揭开相邻的所有空白区域：

```javascript
reveal(row, col) {
  const queue = [[row, col]];
  const visited = new Set();

  while (queue.length > 0) {
    const [r, c] = queue.shift();
    const key = `${r},${c}`;
    if (visited.has(key)) continue;
    visited.add(key);

    const cell = board[r][c];
    cell.revealed = true;

    if (cell.adjacentMines === 0) {
      for (let dr = -1; dr <= 1; dr++) {
        for (let dc = -1; dc <= 1; dc++) {
          const nr = r + dr;
          const nc = c + dc;
          if (this.inBounds(nr, nc) && !board[nr][nc].revealed) {
            queue.push([nr, nc]);
          }
        }
      }
    }
  }
}
```

### 3. Chord 操作

双击已揭开的数字格 N，检测周围已标记旗数。若旗数 = N，则自动揭开周围所有未标记且未揭开的格子：

```javascript
chord(row, col) {
  const cell = board[row][col];
  if (!cell.revealed || cell.adjacentMines === 0) return;

  let flagCount = 0;
  const toReveal = [];

  for (let dr = -1; dr <= 1; dr++) {
    for (let dc = -1; dc <= 1; dc++) {
      const nr = row + dr;
      const nc = col + dc;
      if (this.inBounds(nr, nc)) {
        const neighbor = board[nr][nc];
        if (neighbor.flagged) flagCount++;
        else if (!neighbor.revealed) toReveal.push([nr, nc]);
      }
    }
  }

  if (flagCount === cell.adjacentMines) {
    toReveal.forEach(([r, c]) => this.reveal(r, c));
  }
}
```

### 4. 胜利判定

```javascript
if (cellsRevealed === rows * cols - totalMines) {
  // 所有非雷格已揭开 → 胜利
  this.win();
}
```

---

## 📱 浏览器支持

| 浏览器 | 最低版本 | 状态 |
|:---:|:---:|:---:|
| Chrome | 88+ | ✅ 完全支持 |
| Firefox | 85+ | ✅ 完全支持 |
| Safari | 14+ | ✅ 完全支持 |
| Edge | 88+ | ✅ 完全支持 |
| Opera | 74+ | ✅ 完全支持 |
| IE | — | ❌ 不支持 |

> 使用了 ES6+ 语法、CSS Grid、Web Animations API，不支持 IE。

---

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！请遵循以下流程。

### 提交 Issue

1. 在 [Issues](https://github.com/yourname/minesweeper-x/issues) 页面搜索是否已有相同问题
2. 若无，点击 **New Issue** 创建新问题
3. 详细描述问题、复现步骤、期望行为、实际行为
4. 附上截图或控制台错误信息

### 提交 Pull Request

```bash
# 1. Fork 本仓库

# 2. 克隆你的 Fork
git clone https://github.com/yourname/minesweeper-x.git

# 3. 创建特性分支
git checkout -b feature/amazing-feature

# 4. 进行修改并提交
git add .
git commit -m "feat: add amazing feature"

# 5. 推送到你的 Fork
git push origin feature/amazing-feature

# 6. 在 GitHub 上创建 Pull Request
```

### 提交规范

| 前缀 | 说明 |
|:---:|:---|
| `feat:` | 新功能 |
| `fix:` | 修复 Bug |
| `docs:` | 文档更新 |
| `style:` | 代码格式（不影响功能） |
| `refactor:` | 重构 |
| `perf:` | 性能优化 |
| `test:` | 测试相关 |
| `chore:` | 构建 / 工具变动 |

---

## 📝 开发计划

### ✅ 已完成

- [x] 核心扫雷游戏逻辑
- [x] 4 种难度系统（含自定义）
- [x] 首点保护
- [x] BFS 自动展开
- [x] Chord 双击操作
- [x] 本地存档（最佳成绩、统计）
- [x] 智能提示功能
- [x] 键盘快捷键
- [x] 暗夜矿场视觉主题
- [x] 背景粒子动画
- [x] 胜利彩纸特效
- [x] 踩雷震动 + 红屏
- [x] 响应式布局
- [x] Toast 通知系统

### 🔜 计划中

- [ ] 多人对战模式
- [ ] 在线排行榜
- [ ] 自定义主题切换
- [ ] 移动端长按手势优化
- [ ] 音效系统
- [ ] 撤销操作
- [ ] 回放系统
- [ ] 多语言支持
- [ ] PWA 离线模式

---

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

```
MIT License

Copyright (c) 2024 Minesweeper X

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 致谢

- 灵感来源于经典 Windows 扫雷游戏（Robert Donner, 1989）
- 感谢 [Tailwind CSS](https://tailwindcss.com/) 提供的优秀工具
- 感谢 [Font Awesome](https://fontawesome.com/) 提供的图标库
- 感谢 [Google Fonts](https://fonts.google.com/) 提供的字体服务
- 感谢所有为开源社区贡献力量的人

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Aventardo7777/minesweeper-x&type=Date)](https://star-history.com/#Aventardo7777/minesweeper-x&Date)

---

<div align="center">

**如果这个项目对你有帮助，请给一个 ⭐ Star！**

Made with ❤️ by [Aventardo7777](https://github.com/Aventardo7777)

---

*Last updated: 2024*

</div>
