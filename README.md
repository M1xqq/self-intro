# 马一先 · 自我介绍网页

用于地瓜机器人黑客松报名的单页个人介绍。原生 HTML / CSS / JS，无框架、无外部依赖，双击即可打开。

## 链接

| 用途 | 地址 |
|---|---|
| 网页在线地址 | https://m1xqq.github.io/self-intro/ |
| 代码仓库 | https://github.com/M1xqq/self-intro |

## 目录结构

```
self-intro/
├── index.html     # 自我介绍网页（单页，含响应式布局与打印样式）
└── README.md      # 本说明
```

## 本地预览

直接双击 `index.html`，或在本目录执行：

```bash
python -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 提交与部署

### GitHub 仓库与 Pages

仓库在 <https://github.com/M1xqq/self-intro>，分支 `main`。根目录的 `index.html` 通过 GitHub Pages 直接托管，在线地址见上表。日常更新：

```bash
git add -A && git commit -m "说明" && git push
```

推送后 Pages 会自动重新构建，稍等片刻刷新即可看到新版本。

### 同步到 Gitee（可选）

Gitee 账号 `hzjhzjhzjhzj` 的 SSH 密钥已配置。如需在 Gitee 也留一份镜像：

1. 在 <https://gitee.com/projects/new> 新建空仓库 `self-intro`，不要勾选「使用 Readme 文件初始化这个仓库」，复制仓库 SSH 地址。
2. 为两个平台各留一个远端：

```bash
git remote add gitee git@gitee.com:hzjhzjhzjhzj/self-intro.git
git push -u gitee main
```

之后 `git push` 推 GitHub，`git push gitee main` 推 Gitee。Gitee 仓库可在「服务 → Gitee Pages」开启静态托管（需完成实名认证）。

## 常用命令速查

| 目的 | 命令 |
|---|---|
| 查看改动 | `git status` |
| 提交改动 | `git add -A && git commit -m "说明"` |
| 推送到 GitHub | `git push` |
| 推送到 Gitee | `git push gitee main` |
| 拉取更新 | `git pull` |
| 查看远程地址 | `git remote -v` |

## 技术说明

- 原生 HTML + CSS + 少量原生 JS，无 CDN、无构建步骤，离线可用
- 响应式栅格，手机端可直接阅读；附打印样式，便于导出 PDF 或截图放进报名材料
- 网页内容按报名需要整理，只保留必要的公开信息

---

马一先（M1xqq）· 上海工程技术大学电子信息类 · 2026
