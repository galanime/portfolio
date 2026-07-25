# 张恒玮 · Personal Portfolio

面向实习 / 秋招展示的静态单页作品集，主线定位为 AI 应用工程、Agent 工作流与 Python 全栈产品化。页面只放适合公开的项目链接；仍在脱敏或不适合公开的项目会标注状态，不伪装成可访问仓库。

## 当前展示重点

- **LifeHelper**：全栈 Agent 工程原型，覆盖 FastAPI 后端、React 前端、工具调用、任务编排、Trace、评估与会话回放。
- **Short Video Studio Lite**：公开视频工作流 Demo，用 mock providers 保留工程结构并隔离真实商业 / provider 配置。
- **灰虎题库小程序**：微信原生小程序学习产品原型，展示移动端页面组织、题库流程和本地数据演示能力；当前按“待脱敏公开 / 面试可讲”处理。

页面默认不展示私人邮箱、手机号、真实密钥、客户资料、私有 provider 信息或未确认公开的 GitHub 链接。

## 公开状态

| 项目 | 展示状态 | 说明 |
| --- | --- | --- |
| LifeHelper | Public | 可作为 AI Agent / FastAPI / React 主项目展示 |
| Short Video Studio Lite | Public | 可作为公开视频工作流与 mock provider 公开版展示 |
| 灰虎题库小程序 | 待脱敏公开 | 本地 README 已按 mock 小程序原型整理，公开前需确认远端已同步清理版 |
| HUIHU Xiaohongshu Ops Agent | 只面试讲 | 涉及端侧自动化、账号/设备状态和平台操作边界，不公开源码 |
| job-hunt-kb | 私有 | 含真实求职材料，只可做 sample candidate 脱敏版后展示 |

## 文件结构

```text
personal-portfolio/
├── index.html      # 页面结构（中文内容，公开项目链接）
├── style.css       # 暗色极简样式
└── README.md       # 本文件
```

## 本地预览

```powershell
py -m http.server 8000
# 浏览器打开 http://localhost:8000
```

也可以使用 Node 静态服务器：

```bash
npx serve .
```

## 部署到 Vercel

1. 将 `portfolio_exports/personal-portfolio/` 作为独立静态站点仓库推到 GitHub，推荐仓库名 `personal-portfolio` 或 `portfolio`。
2. 登录 Vercel，选择 `Add New...` → `Project`。
3. Import 对应 GitHub 仓库。
4. Framework Preset 选择 **Other**。
5. Deploy 后把生成的 `*.vercel.app` 域名写回页面 footer。

## 发布前检查

- [ ] `index.html` 中所有 GitHub 链接均指向已确认公开的 `https://github.com/galanime/...` 仓库。
- [ ] Private / 待脱敏项目没有被写成公开可点击仓库链接。
- [ ] 如需放简历 PDF，已提供公开版 `resume.pdf`，且不含不想公开的信息。
- [ ] footer 中 Portfolio 域名已替换为真实 Vercel 或 GitHub Pages 域名。
- [ ] 公开项目 README 与页面描述一致，且没有开发日志、内部恢复记录、求职话术或不该出现的 AI 辅助过程痕迹。
- [ ] 未出现手机号、私人邮箱、真实 API Key、Cookie、Token、私有部署地址、客户 / 商家资料或真实平台账号信息。
- [ ] 灰虎题库小程序公开前已同步脱敏版 README，并复查 AppID、支付、订单、题库版权和演示账号边界。

## 风格说明

- 暗色极简单页，纯原生 HTML / CSS，无构建依赖。
- 桌面端左侧 sticky sidebar + 右侧主内容；移动端单列自适应。
- HTML 语义化：`header`、`nav`、`main`、`section`、`article`、`footer`。

## 许可

本页面仅作为个人求职作品集入口，公开发布前请按上方清单复查项目链接和隐私边界。
