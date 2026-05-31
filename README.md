# Resume Skill / 简历.skill

> *Review like a strict interviewer. Rewrite like a consultant. Export a polished A4 resume in Chinese, English, bilingual, or other localized formats.*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Compatible-green)](https://agentskills.io)
[![Codex](https://img.shields.io/badge/Codex-Skill-blue)](Resume-skill/SKILL.md)
[![Templates](https://img.shields.io/badge/Templates-3%20Families-black)](#三类模板)

**Resume Skill / 简历.skill** is a multilingual resume optimization and A4 HTML resume generation skill. It can work with Chinese, English, bilingual, and localized resume outputs. It does not simply polish wording; it reviews the resume like a strict interviewer, restructures experience for the target role, strengthens project evidence and measurable impact, then exports a printable one-page or two-page HTML resume.

```bash
npx skills add Yunwuxin-666/Resume-skill
```

---

## 它解决什么

很多简历的问题不是“不够好看”，而是：

- Experience reads like a responsibility list, not evidence of real contribution
- Projects lack context, methods, outcomes, and interview-ready depth
- Metrics are disconnected from actions and look unconvincing
- Role positioning is unclear across AI, product, design, engineering, operations, or business tracks
- Layout is either too empty or too dense, making A4 output unstable

简历.skill 把这些问题拆成三件事：

1. **审稿**：指出虚、弱、空、不可追问的内容
2. **重写**：按岗位重组工作经历、项目经历和技能结构
3. **排版**：按四级优先级输出 A4 HTML 简历

It also adapts tone and section labels by language and market context:

- Chinese resume: `个人总结`、`工作经历`、`项目经历`、`专业技能`
- English resume: `Summary`、`Experience`、`Projects`、`Skills`
- Bilingual resume: Chinese and English section labels or paired content blocks when requested
- Localized resume: adjust wording, dates, contact fields, and role naming for the target country or hiring context

---

## 可产出的内容

根据用户上传的简历、粘贴的经历、目标岗位，或完全从零虚构的候选人信息，可以生成中文、英文、双语或本地化版本：

- **Profile / 个人信息**：name, phone, email, target role, avatar area
- **Education / 教育经历**：school, major, degree, date range, multiple degree levels
- **Summary / 个人总结**：candidate positioning, core strengths, interview-ready highlights
- **Experience / 工作经历**：company, role, team, location, responsibilities, methods, tools, and outcomes
- **Projects / 项目经历**：project context, technical actions, business value, and measurable results
- **Skills / 专业技能**：toolchain, technical stack, methodology, delivery capability
- **Awards / 荣誉奖项**：scholarships, competitions, certificates, language ability, portfolio, papers, open-source work

---

## 四级排版优先级

输出时不随机决定页数和密度，而是按固定优先级走：

| 优先级 | 模式 | 适用场景 |
|---|---|---|
| 1 | `1-page loose` | 一页宽松铺满，默认第一版 |
| 2 | `1-page compact` | 内容较多，但仍适合压在一页 |
| 3 | `2-page loose` | 一页承载不了，改用两页宽松铺满 |
| 4 | `2-page compact` | 内容非常多，两页也需要提高密度 |

默认永远从 **一页宽松铺满** 开始。页面不够满时，优先补充岗位相关内容，而不是先压缩行距。只有内容放不下时，才进入紧凑或双页策略。

---

## 三类模板

项目内置 3 个模板家族，每个家族包含靠右头像、居中头像等变体。

### 1. 墨线经典

黑白、简洁、正式，是默认模板，适合大多数通用岗位。

适合产出：

- AI Designer / AIGC Visual Designer resumes
- AI Product Manager / LLM Application Product Manager resumes
- Operations, content, marketing, and brand resumes
- Formal one-page resumes that emphasize structured experience and readable density

模板文件：

- `Resume-skill/templates/resume-template-01-moxian-classic.html`
- `Resume-skill/templates/resume-template-01-moxian-classic-center.html`
- `Resume-skill/templates/resume-template-02-moxian-classic-right.html`

### 2. 运营简洁

适合运营、内容、品牌、电商、教育和增长类岗位，表达更偏业务结果和执行动作。

适合产出：

- Content operations / user operations / campaign operations resumes
- Social media operations / e-commerce operations resumes
- Brand marketing / growth / course operations resumes
- Resumes emphasizing campaigns, content growth, conversion metrics, and channel execution

模板文件：

- `Resume-skill/templates/resume-template-02-ziteng-ops.html`
- `Resume-skill/templates/resume-template-03-ziteng-ops-center.html`
- `Resume-skill/templates/resume-template-04-ziteng-ops-right.html`

### 3. 工程专业

适合工程、算法、AI 工程、半导体、研发和技术岗位，表达更强调技术栈、项目细节和指标。

适合产出：

- Algorithm Engineer / Machine Learning Engineer / Recommendation Engineer resumes
- AI Image Engineer / ComfyUI Workflow Engineer resumes
- Backend, data, R&D, semiconductor process, and technical resumes
- Resumes emphasizing models, systems, experiments, performance, yield, accuracy, and A/B testing

模板文件：

- `Resume-skill/templates/resume-template-03-lanbiao-engineering.html`
- `Resume-skill/templates/resume-template-05-lanbiao-engineering-center.html`
- `Resume-skill/templates/resume-template-06-lanbiao-engineering-right.html`

---

## 使用示例

```text
用我的简历优化成 AI 设计师岗位，一页宽松铺满。
```

```text
Create an English one-page resume for a machine learning engineer, using the centered-avatar template.
```

```text
输出一份中英双语简历，目标岗位是 AI Product Designer。
```

```text
从零生成一份算法工程师简历，用居中头像模板，一页。
```

```text
把这份项目经历改成能经得起面试追问的项目描述，并套工程专业模板。
```

```text
给我输出 6 个模板版本做对比。
```

---

## 仓库结构

```text
Resume-skill/
├── README.md
├── LICENSE
├── .gitignore
└── Resume-skill/
    ├── SKILL.md
    └── templates/
        ├── resume-template-01-moxian-classic.html
        ├── resume-template-01-moxian-classic-center.html
        ├── resume-template-02-moxian-classic-right.html
        ├── resume-template-02-ziteng-ops.html
        ├── resume-template-03-ziteng-ops-center.html
        ├── resume-template-04-ziteng-ops-right.html
        ├── resume-template-03-lanbiao-engineering.html
        ├── resume-template-05-lanbiao-engineering-center.html
        ├── resume-template-06-lanbiao-engineering-right.html
        └── resume-template-index.html
```

仓库只保留 Skill 本体和可复用模板，不保留测试生成的个人简历、PDF、截图预览等临时产物。

---

## 安装

### 方式一：skills CLI

```bash
npx skills add Yunwuxin-666/Resume-skill
```

### 方式二：手动安装

把 `Resume-skill/` 文件夹复制到你的 Codex skills 目录：

```text
~/.codex/skills/Resume-skill/
```

然后在 Codex 中直接请求“用简历 skill 优化简历”即可。

---

## License

MIT License © Yunwuxin-666
