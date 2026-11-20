# 四色圣诞树 · 网页版

由 [ZekangLi-Zico/Christmas-Tree](https://github.com/ZekangLi-Zico/Christmas-Tree)（Pygame 版）移植成纯网页版：
单个 HTML 内嵌 WebGL 点精灵渲染，50000 颗树粒子 + 地面光环 + 顶部爱心 + 星空雪花，无需联网、无依赖、无外链资源。

原版右下角的署名水印文字**已移除**。

---

## 文件

| 文件 | 说明 |
| --- | --- |
| `index.html` | 总入口（四色卡片 + 手机分享版入口） |
| **`xmas-all.html`** | **合并版：一个文件包含四套配色，点右下角色点实时切换**（推荐分享用） |
| `xmas-pink.html` | 粉色单色版（键盘 1-4 可跳转切换） |
| `xmas-gold.html` | 金色单色版 |
| `xmas-green.html` | 绿色单色版 |
| `xmas-blue.html` | 蓝色单色版 |
| `preview/` | 效果预览图（`all.jpg` 四色拼图、`mobile.jpg` 手机竖屏、`qr.png` 扫码卡片） |
| `_build/` | 构建源码（`template.html` + `build.py`），改完执行 `python build.py` 重新生成 |

## 怎么用

**电脑上**：双击 `index.html`，点任意卡片进入；页面内按 `1`-`4` 切换配色、`F` 全屏、`空格` 暂停。

**发给朋友 / 手机上**：只要发 **`xmas-all.html`** 这一个文件（约 21 KB）。
对方在手机上收到后选择「用其他应用打开」→ 浏览器，即可看到圣诞树，点右下角四个色点切换配色。

**扫二维码**：`preview/qr.png` 是一张可直接转发的扫码卡片。

## 说明

- 所有配色、粒子参数、运动方式均按原版 `tree.py` 复刻；仅水印被去除，四套色调是在原版粉白基调上派生的。
- `zoom` 会根据屏幕比例自适应：横屏树占满高度，竖屏自动放大填满手机屏。
- WebGL 不可用时自动降级到 Canvas2D（粒子数降到 34%）。
