# Yolanda Yin's Homepage — 个人网站

> 深圳大学南特金融科技学院金融科技与风险控制硕士（2025.09–2027.06）个人主页。
> CFA 持证 · PMP · 腾讯云 AI 工程师认证 · CQF 考生。

**GitHub Pages 正式链接**：<https://yinhy2008.github.io>

---

## 一、项目说明

本项目是「金融 AI Agent 暑假集训 · 模块三下午实验课」的基础作业（满分 100 分），按照规范化 AI 开发流程 **Vibe → Spec → Harness → GitHub → GitHub Pages → TA-Claw** 完成，目标是建立一个**可公开访问的静态个人主页**，完整呈现五个基础区块（Hero / About / Skills / Projects / Contact），内容真实、桌面与手机均可读。

---

## 二、所用模板

- **主题**：Jekyll + Minimal Mistakes 主题（MIT License）
- **教师模板源仓库**：<https://github.com/jwentong/jwentong.github.io>
- **本仓库**（fork 后改为个人内容）：<https://github.com/yinhy2008/yinhy2008.github.io>
- **部署方式**：GitHub Pages，从 `master` 分支根目录部署，无需本地 Ruby 环境

---

## 三、五区块导航

| 区块 | 入口 | 负责文件 |
| --- | --- | --- |
| Hero | 首页头部 | `index.md` |
| About | 导航栏 About | `AboutMe.md` |
| Skills | 导航栏 Skills | `skills.md` |
| Projects | 首页 Recent Projects 区块 | `index.md` |
| Publications | 导航栏 Publications | `Publication.markdown` |
| Contact | 导航栏 Contact | `contact.md` |

导航栏配置在 `_data/navigation.yml`，五入口 + GitHub 链接。

---

## 四、主要修改内容（相对教师模板）

1. **`_config.yml`**
   - `locale` 改为 `zh-CN`
   - `title` / `subtitle` / `description` / `name` / `repository` 全部替换为本人信息
   - `author` 区块替换为 `Yolanda Yin`，bio 为「金融科技与风险控制硕士 · CFA · PMP」
   - `author.links` 与 `footer.links` 仅保留 GitHub 链接，删除原模板作者的全部社交链接
   - 删除 `avatar` 字段（不公开个人照片）
   - `minimal_mistakes_skin` 保持 `aqua`
2. **`index.md`**
   - Hero 区块替换为本人姓名、定位副标题、一句话简介
   - 增加两个行动入口按钮：「查看 Projects」「联系 Contact」
   - Biography / Work Experience / Recent Projects / What's New / Selected Publication 全部替换为本人真实信息
   - Recent Projects 区块共 4 个项目卡片（VAE 期权定价 / LendingClub 信贷违约 / ERP-CRM 业务实施 / 金融 AI Agent 集训成果）
3. **`AboutMe.md`**：重写 About、Education、Work Experience、Certifications、Research Interests、Service 六段，全部为本人真实背景
4. **`skills.md`**（新建）：四类技能——金融与认证 / 编程与数据科学 / 业务系统与项目管理 / 语言能力，外加「学习中」段
5. **`contact.md`**（新建）：GitHub 链接为主联系方式，明确声明不公开邮箱 / 手机号 / 身份证 / 邀请码等敏感信息，所有联系通过 GitHub Issues 引导
6. **`Publication.markdown`**：替换为本人真实论文（MASS 2011 / AIMSEC 2011，均为第二作者）+ 在研课题
7. **`_data/navigation.yml`**：导航条改为 Home / About / Skills / Publications / Contact / GitHub

---

## 五、隐私说明

本仓库与网站**不包含**以下任何信息：

- 手机号、电子邮箱、身份证号、住址
- 课程邀请码、作业代码、Vibe 邀请码
- `.env`、API Key、Token、密码
- 依赖目录、构建产物、大型原始视频

所有联系通过 GitHub Issues 进行。

---

## 六、本地预览与使用说明

本项目完全在 GitHub Pages 服务端构建，**无需本地 Ruby 环境**。

如需本地预览：

```bash
# 需已安装 Ruby + Bundler
bundle install
bundle exec jekyll serve
# 打开 http://127.0.0.1:4000
```

如仅查看线上效果，直接访问：<https://yinhy2008.github.io>

---

## 七、目录结构

```
yinhy2008.github.io/
├─ _config.yml              # 站点配置
├─ _data/navigation.yml     # 导航栏
├─ index.md                 # 首页（Hero + About + Projects + What's New + Publication）
├─ AboutMe.md               # About 区块
├─ skills.md                # Skills 区块（新建）
├─ contact.md               # Contact 区块（新建）
├─ Publication.markdown     # Publications 区块
├─ README.md                # 本文件
├─ docs/                    # 规格文件
│  ├─ prd.md
│  ├─ design.md
│  └─ checklist.md
├─ report/
│  └─ final-report.md       # 最终报告
└─ screenshots/             # 验收截图
   ├─ homepage-desktop.png
   ├─ homepage-mobile.png
   ├─ github-pages.png
   └─ checklist.png
```

---

## 八、License

主题模板遵循 MIT License（Minimal Mistakes）。本仓库中本人撰写的文档与内容（`docs/`、`report/`、`README.md` 及各 `.md` 页面正文）版权归尹红艳所有，仅用于课程作业展示。
