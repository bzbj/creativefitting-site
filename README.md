# CreativeFitting 井英科技 — 官网

井英科技（CreativeFitting）公司官网，纯静态站点，无任何构建步骤和运行时依赖。

## 站点结构

```
index.html      首页（单页：首屏 / AI 短剧 / Agent 系统 / 公司动态 / 关于我们）
p2026.html      新闻：完成新一轮融资，原 AWS 首席应用科学家加盟（2026.06）
p0409.html      新闻：温影 × 井英科技战略合作揭牌（2025.04）
p0123.html      新闻：海外热榜首次出现 AI 短剧的身影（2025.01）
p76.html        新闻：获百度 PreA+ 轮融资（2024.07）
p56.html        新闻：斩获全球 AI 电影马拉松大赛观众选择奖（2024.06）
p2023.html      新闻：获数百万美元 Pre-A 轮融资（2023.11）
assets/         全部图片资源
assets/fonts/   自托管 Web 字体（Noto Serif SC / Playfair Display / Space Grotesk）
```

## 部署说明

1. 将仓库全部文件原样放到任意 Web 服务器（Nginx / Caddy / Apache / 对象存储静态托管均可）的站点根目录或子目录下。
2. 确保目录默认文档为 `index.html`（各服务器默认配置即满足）。
3. 无需 Node / PHP / 数据库，无构建步骤。

### 资源完整性

- 所有图片、字体均已本地化（`assets/`），**不依赖任何外部资源**，可在无外网环境/内网部署。
- 仅有的三个外部链接为导航跳转：App Store、Google Play（Reel.AI 产品页）和工信部 ICP 备案查询，不影响页面渲染。

### 备案信息

页脚含 ICP 备案号：闽ICP备2023004627号-2。如部署到新域名请按实际备案情况更新 `index.html` 及各 `p*.html` 页脚。

## 技术说明

- 单文件页面：每个 HTML 内联了全部 CSS / JS，互相独立。
- 字体通过 `assets/fonts/fonts.css` 引入（按 unicode-range 分片的 woff2，浏览器只加载用到的分片）。
- 无 Cookie、无统计脚本、无第三方请求。
