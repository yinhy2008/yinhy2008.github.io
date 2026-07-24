# 最终报告 — 个人网站规范化 AI 开发

> 项目：yinhy2008.github.io
> 作者：尹红艳（Yolanda）
> 提交日期：2026-07-24
> 模板：Jekyll + Minimal Mistakes 主题（forked from jwentong/jwentong.github.io，MIT License）

---

## 一、项目背景与定位

本项目是「金融 AI Agent 暑假集训 · 模块三下午实验课」基础作业（满分 100 分），要求在规范化 AI 开发流程 **Vibe → Spec → Harness → GitHub → GitHub Pages → TA-Claw** 下完成一个综合个人简介型静态网站，发布到 GitHub Pages 并通过 TA-Claw 提交。

我的定位是建立一个**面向招聘方 / 学术同行 / 课程教师**的公开个人主页，集中呈现：

- 深圳大学南特金融科技学院金融科技与风险控制硕士在读（2025.09–2027.06）的学术身份
- CFA 持证、PMP、腾讯云 AI 工程师认证、CQF 考生的专业资质
- 两个硕士研究方向：VAE 期权定价与希腊字母预测、LendingClub 信贷违约预测
- 10 年以上金融与地产科技行业经验（家族办公室渠道经理 + 万科/明源 ERP 业务分析）
- 已发表的国际会议论文（MASS 2011 / AIMSEC 2011）

---

## 二、开发流程（Vibe → Spec → Harness → GitHub → Pages → TA-Claw）

### 2.1 Vibe 阶段

在 Vibe 会话中明确：

- 目标访问者：招聘方 HR、学术同行、课程教师
- 希望访问者记住的：金融科技 + 风控 + 真实项目经历
- 本期必须包含：五区块（Hero / About / Skills / Projects / Contact）
- 本期明确不做：登录、数据库、支付、评论、访客追踪
- 隐私红线：不公开手机号、邮箱、身份证、住址、邀请码、作业代码

### 2.2 Spec 阶段

完成三份规格文件，均存放于 `docs/` 目录，可在 GitHub 仓库内直接预览：

- `docs/prd.md`：产品需求文档——目标用户画像、5 区块信息架构、8 条验收标准（AC1–AC8）、范围边界与变更控制
- `docs/design.md`：设计说明——模板选型理由、页面结构与路由、视觉设计（配色/字体/布局）、文件修改清单、内容来源与隐私设计、风险与回滚
- `docs/checklist.md`：验收清单——逐项对照 G1–G6 六项硬性门槛 + 隐私红线专项扫描 + 100 分评分量规自评

### 2.3 Harness 阶段

采用证据驱动的验收方式：

- 每一项验收都要求可看见、可点击或可复现
- 桌面端与移动端均通过浏览器实际访问验证
- GitHub Pages 部署成功状态截图留存
- 提交前对全部 `.md` / `.yml` 文件做敏感词正则扫描（手机号、身份证、邮箱、邀请码、API_KEY 等）

### 2.4 GitHub 与 Pages 阶段

- Fork 教师模板 `jwentong/jwentong.github.io` → `yinhy2008/yinhy2008.github.io`（Public）
- 在 `master` 分支根目录部署 GitHub Pages
- 完成至少 3 次有意义的 Commit（详见第四部分）
- Pages 自动构建约 1–2 分钟，部署完成后用无痕窗口验证访问

### 2.5 TA-Claw 阶段

在 Vibe / 课程平台（vibe.planlabopc.com）完成：

1. 第一次预览：填入 Pages 链接 + 仓库链接 + 报告路径
2. 二次确认：手动核对每项必填字段
3. 看到「Submitted successfully」成功回执并截图

---

## 三、五区块说明

### 3.1 Hero（首页头部）

- 称呼：尹红艳（Yolanda）
- 定位副标题：金融科技与风险控制硕士 · CFA 持证
- 一句话简介：深圳大学南特金融科技学院，金融科技与风险控制专业（2025.09–2027.06）
- 行动入口按钮：「查看 Projects」（锚点跳转）、「联系 Contact」（跳转 contact 页）

### 3.2 About

文件 `AboutMe.md`，包含六段：

- About Me：个人简介 + 两个硕士研究方向概述
- Education：硕士（深圳大学南特金融科技学院）+ 本科（河海大学信息管理与信息系统，GPA 4.03/5.0）
- Work Experience：4 段真实工作经历（松石家族办公室 / 万科万翼科技 / 御邦医通 / 明源软件）
- Certifications：CFA / PMP / 腾讯云 AI 工程师 / CQF（考生）
- Research Interests：生成式 AI 金融工程应用 / 信贷风控 ML / 量化金融 Greeks 与 XVA / AI Agent 金融决策
- Service：金融 AI Agent 暑假集训参与、CFA/CQF 社区

### 3.3 Skills

文件 `skills.md`，四类技能 + 学习中：

- 金融与认证：CFA / CQF / PMP / 腾讯云 AI
- 编程与数据科学：Python（pandas/numpy/sklearn/XGBoost/TensorFlow/QuantLib/SHAP）/ SQL / Jupyter+VSCode+Git
- 业务系统与项目管理：ERP 实施（明源/SAP）/ CRM（万科/明源）/ PMBOK+敏捷+瀑布
- 语言能力：中文母语 / 英文工作语言（CFA 全英文考试通过）
- 学习中：RNN/LSTM/Transformer、强化学习、Hugging Face、PyPortfolioOpt

### 3.4 Projects

首页 `index.md` 的 Recent Projects 区块，4 个项目卡片：

1. VAE 生成模型用于期权定价与希腊字母预测（硕士在研课题）
2. LendingClub 信贷违约预测模型（硕士课程项目，XGBoost + SHAP，AUC 0.92）
3. ERP / CRM 业务系统实施案例（工作产出，万科 + 明源）
4. 金融 AI Agent 暑假集训实验成果（模块一至模块三）

首页同时呈现 What's New（4 条时间线）与 Selected Publication（2 篇国际会议论文）。

### 3.5 Contact

文件 `contact.md`：

- 主联系方式：GitHub（<https://github.com/yinhy2008>）+ 本仓库 Issue
- 学术交流：列出学院、专业、两个研究主题；如需邮件交流通过 GitHub Issues 留言
- 隐私声明：明确不公开手机号、邮箱、身份证、住址、邀请码、作业代码
- 网站信息：部署平台、访问地址、技术栈、源码许可

---

## 四、Git 提交记录

仓库 <https://github.com/yinhy2008/yinhy2008.github.io>，`master` 分支，至少 3 次有意义 Commit：

| 顺序 | Commit 信息 | 内容 |
| --- | --- | --- |
| 1 | `docs: add PRD, Design, and Checklist` | 初始化规格文件 `docs/prd.md` `design.md` `checklist.md` |
| 2 | `content: replace with real personal info and add skills/contact pages` | 修改 `_config.yml` / `index.md` / `AboutMe.md` / `Publication.markdown` / `navigation.yml`，新建 `skills.md` `contact.md` |
| 3 | `docs: add README, final report, and screenshots` | 新建 `README.md`、`report/final-report.md`、`screenshots/` 4 张关键截图 |

每次 Commit 均围绕一个独立可验证的目标，避免一次性大提交。

---

## 五、Harness 验证结果

### 5.1 G1 作品可访问

- ✅ Pages 链接 <https://yinhy2008.github.io> 在无痕窗口可打开
- ✅ 桌面端 Chrome / Edge / Safari 均正常
- ✅ 移动端 Safari / Chrome 模拟器布局正常
- ✅ 截图证据：`screenshots/github-pages.png`（Pages 部署成功状态）

### 5.2 G2 内容属于本人

- ✅ 五区块齐全（Hero / About / Skills / Projects / Contact）
- ✅ 无占位符：扫描 `TODO` `Lorem ipsum` `占位` `示例` `Template` 结果为空
- ✅ 无教师模板原内容残留：扫描 `jwentong` `Jingwen Tong` `童景文` 结果为空
- ✅ 项目描述均为本人真实经历或研究

### 5.3 G3 规格文件完整

- ✅ `docs/prd.md` / `docs/design.md` / `docs/checklist.md` 均存在且非空
- ✅ PRD 五区块描述与网站实际呈现一致
- ✅ Design 文件修改清单与实际 diff 一致

### 5.4 G4 过程可追溯

- ✅ 仓库 Commits 列表至少 3 次有意义 Commit
- ✅ 没有"一次性大提交"

### 5.5 G5 证据可复核

- ✅ `report/final-report.md` 存在并覆盖六部分
- ✅ `screenshots/` 至少 4 张关键证据：
  - `homepage-desktop.png`（桌面端首页）
  - `homepage-mobile.png`（移动端首页）
  - `github-pages.png`（Pages 部署成功）
  - `checklist.png`（验收清单完成）

### 5.6 G6 平台确已收件

- ⏳ 待在 TA-Claw 完成预览 → 二次确认 → 「Submitted successfully」回执截图

### 5.7 隐私红线专项扫描

提交前已对全部 `.md` `.yml` 文件执行正则扫描：

- ✅ 无手机号：`\b1[3-9]\d{9}\b` 结果为空
- ✅ 无身份证号：`\b\d{17}[\dXx]\b` 结果为空
- ✅ 无邮箱明文：扫描 `163.com` `@` + 邮箱格式结果为空（仅 `contact.md` 中"电子邮箱"中文词出现，非实际地址）
- ✅ 无课程邀请码 / 作业代码
- ✅ 无 `.env` / API_KEY / TOKEN / password
- ✅ 无银行账号

---

## 六、AI 参与与个人判断

### 6.1 AI 参与部分

- 阅读 docx 作业说明、解析模板结构
- 起草 `docs/prd.md` `docs/design.md` `docs/checklist.md` 三份规格文件
- 起草 `index.md` / `AboutMe.md` / `skills.md` / `contact.md` / `Publication.markdown` 的内容
- 修改 `_config.yml`（删除 avatar、替换站点信息）
- 起草 `README.md` 与本报告
- 执行敏感词正则扫描

### 6.2 本人最终决策

- ✅ 网站定位：综合个人简介型，面向招聘 + 学术 + 课程三类访问者
- ✅ 模板选择：使用教师指定的 Minimal Mistakes，不切换框架
- ✅ 内容真实性：所有项目、工作经历、论文均为本人真实情况，无虚构
- ✅ 隐私边界：不公开邮箱、手机号、身份证、住址、邀请码；2023.05–2025.04 个人生活段不放入网站
- ✅ 头像处理：不公开个人照片，使用主题默认占位
- ✅ 配色：保持主题 `aqua` skin，不做额外样式定制
- ✅ 部署：完全在 GitHub Pages 服务端构建，不本地编译

---

## 七、问题与后续计划

### 7.1 已知问题

- 头像位置使用主题默认占位（首字母组合），未来如需可上传本人裁剪的正方形头像到 `assets/images/bio-photo.jpg` 并在 `_config.yml` 恢复 `avatar` 字段
- 项目卡片中的 GitHub 链接目前统一指向个人主页 <https://github.com/yinhy2008>，待各项目仓库建立后可分别替换为独立仓库链接

### 7.2 后续计划

- 建立 VAE 期权定价、LendingClub 信贷违约两个独立 GitHub 仓库，并在 Projects 卡片中替换为直链
- 在 Publications 页面补充硕士期间正式发表的论文（如有）
- 考虑在 About 页加入学术简历 PDF 下载（脱敏版本）
- 完成加分作业 OpenClaw 双角色聊天 APP（金融顾问 vs 谨慎客户）

---

## 八、提交证据汇总

| 证据 | 位置 |
| --- | --- |
| Pages 链接 | <https://yinhy2008.github.io> |
| 仓库链接 | <https://github.com/yinhy2008/yinhy2008.github.io> |
| PRD | `docs/prd.md` |
| Design | `docs/design.md` |
| Checklist | `docs/checklist.md` |
| 本报告 | `report/final-report.md` |
| 桌面端截图 | `screenshots/homepage-desktop.png` |
| 移动端截图 | `screenshots/homepage-mobile.png` |
| Pages 部署截图 | `screenshots/github-pages.png` |
| Checklist 截图 | `screenshots/checklist.png` |
| TA-Claw 回执截图 | `screenshots/ta-claw-submission.png`（待提交后补） |

---

> 本报告覆盖项目定位、模板选择、主要修改、AI 参与、个人判断、验证结果、Pages 链接、问题与后续计划，未复制整段聊天记录。
