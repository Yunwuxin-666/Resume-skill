# 简历.skill

> *像严厉面试官一样审稿，像咨询顾问一样重构，最后输出一份能投递的 A4 简历。*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-Compatible-green)](https://agentskills.io)
[![Codex](https://img.shields.io/badge/Codex-Skill-blue)](Resume-skill/SKILL.md)
[![Templates](https://img.shields.io/badge/Templates-3%20Families-black)](#三类模板)

**简历.skill** 是一套中文简历优化与 A4 HTML 简历生成规则。它不是只做润色，而是先用严厉面试官视角审稿，再按目标岗位重排经历、补强项目、强化量化指标，最后套入可打印的一页或两页 HTML 简历模板。

```bash
npx skills add Yunwuxin-666/Resume-skill
```

---

## 它解决什么

很多简历的问题不是“不够好看”，而是：

- 经历写得像职责清单，看不出候选人到底做了什么
- 项目没有背景、方法、结果，面试官追问两层就断
- 指标和成果缺少因果链，像编出来的
- 岗位重点不清，AI、产品、设计、工程表达混在一起
- 版式不是太空，就是太挤，无法稳定输出 A4

简历.skill 把这些问题拆成三件事：

1. **审稿**：指出虚、弱、空、不可追问的内容
2. **重写**：按岗位重组工作经历、项目经历和技能结构
3. **排版**：按四级优先级输出 A4 HTML 简历

---

## 可产出的内容

根据用户上传的简历、粘贴的经历、目标岗位，或完全从零虚构的候选人信息，可以生成：

- **个人信息栏**：姓名、电话、邮箱、求职岗位、头像区域
- **教育经历**：学校、专业、学历、起止时间，支持本科 / 硕士 / 博士多段展示
- **个人总结**：围绕目标岗位提炼候选人定位、核心能力和可追问亮点
- **工作经历**：按时间倒序重写公司、岗位、部门、地点、职责、方法、工具和结果
- **项目经历**：使用“项目简介 / 项目细节 / 项目成果”结构，强化业务背景、技术动作和量化指标
- **专业技能**：按岗位归纳工具链、技术栈、方法论和交付能力
- **荣誉奖项**：展示奖学金、竞赛、认证、语言能力、作品集、论文或开源成果

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

- AI 设计师 / AIGC 视觉设计师简历
- AI 产品经理 / 大模型应用产品经理简历
- 运营、内容、市场、品牌类简历
- 需要正式投递、阅读密度适中、强调经历结构的单页简历

模板文件：

- `Resume-skill/templates/resume-template-01-moxian-classic.html`
- `Resume-skill/templates/resume-template-01-moxian-classic-center.html`
- `Resume-skill/templates/resume-template-02-moxian-classic-right.html`

### 2. 运营简洁

适合运营、内容、品牌、电商、教育和增长类岗位，表达更偏业务结果和执行动作。

适合产出：

- 内容运营 / 用户运营 / 活动运营简历
- 小红书运营 / 新媒体运营 / 电商运营简历
- 品牌营销 / 增长运营 / 课程运营简历
- 强调活动策划、内容增长、转化指标、渠道执行的简历

模板文件：

- `Resume-skill/templates/resume-template-02-ziteng-ops.html`
- `Resume-skill/templates/resume-template-03-ziteng-ops-center.html`
- `Resume-skill/templates/resume-template-04-ziteng-ops-right.html`

### 3. 工程专业

适合工程、算法、AI 工程、半导体、研发和技术岗位，表达更强调技术栈、项目细节和指标。

适合产出：

- 算法工程师 / 机器学习工程师 / 推荐算法工程师简历
- AI 图像工程师 / ComfyUI 工作流工程师简历
- 后端、数据、工程研发、半导体工艺类简历
- 强调模型、系统、实验、性能、良率、准确率、A/B 测试等技术指标的简历

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
