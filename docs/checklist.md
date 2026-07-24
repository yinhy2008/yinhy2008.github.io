# 验收清单（Checklist）— 个人网站

> 项目：yinhy2008.github.io · 版本：v1.0 · 2026-07-24  
> 用途：提交前逐项打勾，确保 G1–G6 六项硬性门槛全部通过

---

## G1 — 作品可访问 ✅

- [ ] GitHub Pages 链接 `https://yinhy2008.github.io` 在**无痕窗口**可打开
- [ ] 链接无 404 / 500 / 主题渲染失败
- [ ] 桌面端 Chrome、Edge、Safari 至少 2 个浏览器能正常访问
- [ ] 移动端 Safari / Chrome 模拟器（或真机）布局正常
- [ ] README.md 中已记录 Pages 链接
- [ ] 报告 `report/final-report.md` 中已记录 Pages 链接
- [ ] **截图证据**：`screenshots/github-pages.png`（Pages 设置截图）

---

## G2 — 内容属于本人 ✅

### 2.1 五区块完整性
- [ ] **Hero** 区块：本人姓名"尹红艳 / Yolanda" + 定位副标题 + 行动按钮
- [ ] **About** 区块：本人教育背景、职业经历摘要、研究兴趣
- [ ] **Skills** 区块：本人真实技能（CFA/PMP/Python/ERP/语言）
- [ ] **Projects** 区块：本人研究项目 + 工作产出 + 课程作业 + 论文
- [ ] **Contact** 区块：本人 GitHub 链接 + （可选）学术邮箱

### 2.2 内容真实性
- [ ] 没有任何占位符：`TODO`、`Lorem ipsum`、`占位`、`示例`、`Template`
- [ ] 没有任何教师模板原内容残留：jwentong / Jingwen Tong / 童景文
- [ ] 所有项目描述为本人真实经历或研究
- [ ] 论文条目为本人真实发表（MASS 2011 / AIMSEC 2011）

---

## G3 — 规格文件完整 ✅

- [ ] `docs/prd.md` 存在且内容完整
- [ ] `docs/design.md` 存在且内容完整
- [ ] `docs/checklist.md` 存在（即本文档）
- [ ] 三份文件均能在 GitHub 仓库内直接预览
- [ ] PRD 中五区块描述与网站实际呈现一致
- [ ] Design 中文件修改清单与实际 diff 一致

---

## G4 — 过程可追溯 ✅

- [ ] 仓库 Commits 列表中至少 **3 次有意义的 Commit**
- [ ] Commit 1：初始化（Fork 模板 + 创建 docs/）
- [ ] Commit 2：内容替换（修改 _config.yml / index.md / AboutMe.md / Publication.markdown）
- [ ] Commit 3：新建 Skills/Contact 页面 + README + 报告
- [ ] （可选）Commit 4：截图入仓 + 报告润色
- [ ] 每条 Commit 信息描述清晰，格式如 `docs: add PRD/Design/Checklist` / `content: replace with real personal info`
- [ ] 没有"一次性大提交"（避免一个 commit 推 100+ 文件）

---

## G5 — 证据可复核 ✅

### 5.1 报告完整性
- [ ] `report/final-report.md` 存在
- [ ] 报告包含六部分：项目背景 / 开发流程 / 五区块说明 / Harness 验证 / 反思与改进 / 提交证据
- [ ] 报告内含 Pages 链接、仓库链接、Commit 链接

### 5.2 截图完整性（至少 4 张）
- [ ] `screenshots/homepage-desktop.png`（桌面端首页全景）
- [ ] `screenshots/homepage-mobile.png`（移动端首页全景）
- [ ] `screenshots/github-pages.png`（GitHub Pages 设置界面，显示部署成功）
- [ ] `screenshots/checklist.png`（本文档全部打勾截图）

### 5.3 可选增强截图
- [ ] `screenshots/about-block.png`
- [ ] `screenshots/skills-block.png`
- [ ] `screenshots/projects-block.png`
- [ ] `screenshots/contact-block.png`
- [ ] `screenshots/commits-history.png`

---

## G6 — 平台确已收件 ✅

- [ ] 登录 Vibe / 课程平台
- [ ] 进入对应课程 → 模块三作业提交入口
- [ ] **第一次预览**：填入 Pages 链接 + 仓库链接 + 报告路径，检查自动校验
- [ ] **二次确认**：手动核对每项必填字段（项目代码、邀请码、链接）
- [ ] **看到 "Submitted successfully" 或等效的成功回执**
- [ ] 截图保存提交回执：`screenshots/ta-claw-submission.png`
- [ ] 提交邀请码和作业代码**不写入任何公开文件**（PRD/Design/Checklist/README/网站本身均不出现）

---

## 隐私红线专项检查 🔒

提交前必须用 grep / 搜索工具对仓库所有 `.md` `.html` `.yml` 文件做敏感词扫描：

- [ ] **无手机号**：搜 `\b1[3-9]\d{9}\b` 结果为空
- [ ] **无身份证号**：搜 `\b\d{17}[\dXx]\b` 结果为空
- [ ] **无住址门牌**：搜 `号 | 路 | 街 | 室 | Building | Street | Road` 结果为空（除非已确认是公开信息）
- [ ] **无课程邀请码 / 作业代码**：搜 `Vibe` `邀请码` `Invitation` `Class Code` 结果为空
- [ ] **无 .env / 密钥 / Token**：搜 `API_KEY` `SECRET` `TOKEN` `password` 结果为空
- [ ] **无银行账号**：搜 `银行卡` `银行账号` `Bank Account` 结果为空
- [ ] **无家庭成员姓名**（非必要不放）
- [ ] **学术邮箱确认不公开**：网站任何位置均无邮箱地址，Contact 区块只放 GitHub 链接

---

## 100 分评分量规自评

| 维度 | 满分 | 自评目标 | 说明 |
| --- | --- | --- | --- |
| Vibe 与 Spec | 25 | 22+ | PRD/Design/Checklist 具体一致可验证 |
| 网站内容与体验 | 20 | 18+ | 五区块齐全，内容真实，桌面手机可读 |
| GitHub 可追溯 | 15 | 14+ | 结构合理，≥ 3 次有意义 Commit |
| Harness 与报告 | 15 | 14+ | 验证证据完整，问题修复反思清楚 |
| GitHub Pages | 15 | 14+ | 正式链接稳定可访问 |
| TA-Claw 提交 | 10 | 10 | 正确项目/报告/截图/会话/成功回执 |
| **基础合计** | **100** | **92+** | |

---

## 最终签字

- 提交者：尹红艳（Yolanda）
- 提交日期：____ 年 ____ 月 ____ 日
- Commit SHA 末四位：________
- Pages 链接验证：✅ / ❌
- 隐私红线检查：✅ / ❌
- TA-Claw 回执：✅ / ❌
