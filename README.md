# aierlaite的博客

基于开源主题 [astro-koharu](https://github.com/cosZone/astro-koharu)（萌系 / 二次元 / 粉蓝配色的 Astro 博客主题）搭建的个人博客。

- 🌐 **在线访问**：<https://blog.aierlaite.dpdns.org>
- 🎵 歌单页：网易云歌单在线播放
- 📄 协议：AGPL-3.0（主题及本仓库修改版均遵循）

## 目录结构速查

| 路径 | 说明 |
| --- | --- |
| `src/content/blog/` | 文章（Markdown），`draft: true` 的文章不会发布 |
| `config/site.yaml` | 站点配置：标题、导航、友链、BGM 歌单等 |
| `src/pages/music.md` | 歌单页内容 |
| `dist/` | 构建产物（部署到服务器 Caddy 托管） |

## 本地开发

```bash
pnpm install
pnpm dev      # 本地预览 http://localhost:4321
pnpm build    # 构建到 dist/
```

环境要求：Node.js ≥ 22.20、pnpm ≥ 10（`corepack enable` 可自动启用）。

## 部署方式

静态构建，服务器端 Caddy 托管 + 自动 HTTPS（Let's Encrypt，Cloudflare 代理回源）。主题更新：

```bash
git fetch upstream && git merge upstream/main
```

## 致谢

- 主题作者：[@cosZone](https://github.com/cosZone)，喜欢这个主题欢迎去[原仓库](https://github.com/cosZone/astro-koharu)点个 star ⭐
- 主题完整文档见原仓库 [GETTING-STARTED](https://github.com/cosZone/astro-koharu/blob/main/GETTING-STARTED.md) 与[使用指南](https://github.com/cosZone/astro-koharu/blob/main/src/content/blog/tools/astro-koharu-guide.md)
