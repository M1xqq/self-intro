# 马一先 · 个人介绍与作品

用于地瓜机器人黑客松报名的单页个人介绍。原生 HTML / CSS / JS，无框架、无构建步骤。

## 链接

| 用途 | 地址 |
|---|---|
| 网页在线地址 | https://m1xqq.github.io/self-intro/ |
| 代码仓库 | https://github.com/M1xqq/self-intro |

## 页面里可以直接点开体验的项目

评委不需要看代码，点标题或截图就能进到项目本身：

| 项目 | 直接体验 |
|---|---|
| SWEET少年的创想空间 | http://noel-psc.cn:8000 |
| 一纸千年 · 心纹研学 | https://m1xqq.github.io/self-intro/yizi/ |
| 上海奶隆工程技术大学.club | https://xn--fhqu4y0gz4eixee8i2xip5mcs1ads3d.club |

一纸千年原本是离线单文件课程，这里把它放到 `yizi/` 下，所以在线上也能直接上课。

「Arduino 机器车」是实物作品，没有可点的体验链接，页面上只放一张同类构型示意图（图源 Wikimedia Commons，CC BY-SA 3.0），图注里已注明是示意图。

## 目录结构

```
self-intro/
├── index.html            # 主页（单页，含响应式与打印样式）
├── assets/
│   └── gsap.min.js       # GSAP 3.13，本地引入，不依赖 CDN
├── shots/                # 项目配图（WebP，已压到约 93KB/张）
│   ├── camp.webp         # 创想空间首屏
│   ├── yizi.webp         # 一纸千年封面
│   ├── nailong.webp      # 奶龙网站首屏
│   └── robotcar.webp     # Arduino 机器车（示意图）
├── yizi/
│   └── index.html        # 一纸千年互动课（单文件，可在线体验）
└── README.md
```

## 本地预览

```bash
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

直接双击 `index.html` 也能看，但 `yizi/` 与截图建议用上面的本地服务器访问。

## 技术说明

- **首屏入场用纯 CSS `@keyframes`**：不依赖脚本、不依赖网络，任何情况下都能播完，不会出现空白首屏。
- **GSAP 本地引入**（`assets/gsap.min.js`），只用于「正在准备」区块的数字落位，属于非关键增强：脚本不加载时页面依然完整可读。
- **响应式**在 1440 / 1180 / 1024 / 860 / 768 / 390 六个宽度实测，均无横向溢出。
- 已适配 `prefers-reduced-motion`：开启减少动效时所有动画停止，内容直接呈现。
- 版式遵循 `design-taste-frontend`（taste-skill 2.5.1）的原则：一屏一区块、左右对齐、真实截图、hover 微动效、不做滚动渐显。
- 附打印样式，便于导出 PDF 或截图放进报名材料。

调试用参数：地址后加 `?still` 可跳过动效、直接看静态终态。

## 提交与部署

仓库在 <https://github.com/M1xqq/self-intro>，分支 `main`。根目录的 `index.html` 通过 GitHub Pages 直接托管。

```bash
git add -A && git commit -m "说明" && git push
```

推送后 Pages 会自动重新构建，稍等片刻刷新即可。

### 同步到 Gitee（可选）

Gitee 账号 `hzjhzjhzjhzj` 的 SSH 密钥已配置：

```bash
git remote add gitee git@gitee.com:hzjhzjhzjhzj/self-intro.git
git push -u gitee main
```

## 常用命令速查

| 目的 | 命令 |
|---|---|
| 查看改动 | `git status` |
| 提交改动 | `git add -A && git commit -m "说明"` |
| 推送到 GitHub | `git push` |
| 推送到 Gitee | `git push gitee main` |
| 拉取更新 | `git pull` |
| 查看远程地址 | `git remote -v` |

---

马一先（M1xqq）· 上海工程技术大学电子信息类 · 2026
