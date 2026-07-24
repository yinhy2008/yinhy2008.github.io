# 设计说明（Design）— 个人网站

> 项目：yinhy2008.github.io · 版本：v1.0 · 2026-07-24

---

## 1. 模板选型

### 1.1 选型结果
**Jekyll + Minimal Mistakes 主题**（forked from jwentong/jwentong.github.io，MIT License）

### 1.2 选型理由
- 教师统一要求：作业要求"使用教师提供的统一模板"
- 模板成熟：Minimal Mistakes 在 GitHub 上是 12k+ stars 的主流 Jekyll 主题
- 五区块适配：模板天然支持多页面布局（Hero、About、Publication 已存在，Skills/Contact 需新建）
- 响应式内置：桌面双栏 / 移动单栏自适应，零代码适配
- 文档完善：官方文档齐全，中文社区资料丰富

### 1.3 复杂度权衡
- 劣势：依赖 Ruby/Bundler/Sass，本地预览需 `bundle exec jekyll serve`（约 200MB 依赖）
- 应对策略：**完全不在本地编译**，所有预览通过 GitHub Pages 在线渲染验证（节省环境配置时间）
- 作业说明明确："复杂模板不会自动加分"，但本模板为教师指定，不扣分

---

## 2. 页面结构与路由

```
yinhy2008.github.io/
├─ _config.yml          站点配置（标题、作者、社交链接、导航）
├─ index.md             首页（Hero + About + Projects 摘要）
├─ AboutMe.md           About 区块（保持原文件名以保留模板引用）
├─ skills.md            Skills 区块（新建）
├─ contact.md           Contact 区块（新建）
├─ Publication.markdown Publications 区块（保留为研究/论文展示）
├─ _data/navigation.yml 导航栏配置
├─ assets/              图片、CSS、JS
└─ docs/                PRD / Design / Checklist（GitHub 上可见）
```

### 2.1 导航栏（Header Nav）
- Home（首页）
- About（关于我）
- Skills（技能）
- Projects（项目）— 在 AboutMe.md 内通过锚点
- Publications（论文/成果）
- Contact（联系）

---

## 3. 视觉设计

### 3.1 配色
- 主题默认配色（Minimal Mistakes 的 `default` skin）
- 主色：深蓝灰（专业、学术感）
- 辅色：链接蓝 `#2f7dd8`（主题默认）
- 不做主题皮肤切换，保持极简

### 3.2 字体
- 标题：Helvetica Neue（主题默认）
- 正文：Helvetica / Arial fallback
- 中文：浏览器默认中文字体栈（macOS PingFang / Windows Microsoft YaHei）

### 3.3 布局
- 桌面端（≥ 1024px）：左侧固定导航 + 右侧内容，最大宽度 1280px
- 移动端（≤ 414px）：单栏堆叠，导航折叠为汉堡菜单

### 3.4 内容呈现
- 区块之间用水平分割线（hr 标签）分隔，视觉清晰
- 项目条目用列表 + 加粗项目名 + 缩进描述
- 论文条目保留模板原格式（题目 + 会议名 + 年份）

---

## 4. 文件修改清单

| 文件 | 操作 | 关键内容 |
| --- | --- | --- |
| `_config.yml` | 修改 | site.title / site.author / site.description / author 区块（name/bio/email）/ social 区块 |
| `index.md` | 修改 | Hero 区块（姓名、定位副标题、按钮）；About 段落；Projects 摘要 |
| `AboutMe.md` | 重写 | 真实教育背景、职业经历、研究方向 |
| `skills.md` | 新建 | 四类技能（金融证书 / 编程工具 / 业务系统 / 语言） |
| `contact.md` | 新建 | GitHub 链接、联系说明（通过 Issues 引导交流，不公开邮箱） |
| `Publication.markdown` | 修改 | 替换为本人论文（MASS 2011 / AIMSEC 2011） |
| `_data/navigation.yml` | 修改 | 增加 Skills、Contact 入口 |
| `README.md` | 重写 | 项目说明、五区块导航、隐私声明、Commit 历史 |

---

## 5. 内容来源与隐私设计

### 5.1 真实信息源
- 简历：`/模块三/尹红艳中文个人简历.docx`
- 课程：深圳大学南特金融科技学院培养方案（来自 memory）

### 5.2 隐私保护设计（Privacy by Design）
- 在 PRD 与本文档中已显式列出**禁放字段**清单
- 提交前用正则扫描敏感关键词（手机号、身份证号、邀请码等）
- 邮箱地址采用 `mailto:` 链接 + 反爬虫文本（不在页面以明文形式完整暴露，若用户选择不公开则完全不放）

### 5.3 内容审核流程
- 每份规格文件（PRD/Design/Checklist）由用户本人最终确认
- 网站所有正文在 PR 描述中粘贴预览，用户确认后再合并

---

## 6. 技术约束

- **不引入额外插件**（除 Minimal Mistakes 自带外）
- **不修改主题核心样式**（`_sass/` 下文件不动）
- **不引入外部 JS 框架**（无 React/Vue，保持纯静态）
- **图片本地化**：头像暂用默认或省略，论文截图不外链

---

## 7. 部署方案

1. 所有内容修改在 GitHub 网页端直接完成（用 Web Editor 或上传文件）
2. GitHub Pages 默认从 master 分支根目录部署
3. 访问地址：`https://yinhy2008.github.io`（无需等待，自动构建约 1–2 分钟）
4. 部署完成后用无痕窗口验证访问

---

## 8. 风险与回滚

| 风险 | 影响 | 回滚方式 |
| --- | --- | --- |
| 主题模板渲染失败 | 页面 404 | Sync fork 回到教师原版 |
| 个别内容不符合隐私红线 | 个人信息泄露 | 立即 git revert 上一 Commit |
| GitHub Pages 构建失败 | 部署不可用 | 查看 Actions 日志，修复后重 push |
