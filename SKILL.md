---
name: resume-tailor-pm
description: >
  Use this skill when the user wants to tailor their resume for a specific job description,
  especially for internet product manager (互联网产品经理) roles. Triggers when the user
  uploads a resume (PDF) and provides a JD (job description), or asks to "改简历", "针对JD修改简历",
  "优化简历", or "resume tailoring". Also trigger when the user mentions they are applying for a
  PM role and wants help customizing bullet points. Always use this skill for any resume editing
  task — even if phrased casually like "帮我改一下简历" or "看看这个JD".
---

# Resume Tailor for Internet Product Manager (互联网产品经理)

A skill for tailoring resumes to specific job descriptions — without fabricating experience,
without sounding like AI wrote it, and without flattering the user. The goal is a resume that
makes any HR or hiring manager want to interview the candidate immediately.

---

## Inputs Required

- **Resume**: PDF format (user uploads)
- **JD**: Job description text (user pastes or uploads)

If either is missing, ask for it before proceeding.

---

## Core Principles

### 1. Never Fabricate
- Do NOT invent new experiences, metrics, projects, or skills that aren't in the original resume.
- Only repackage, reframe, and re-prioritize existing content.
- If you're unsure whether a rewrite stays faithful to the original, **ask the user first**.

### 2. Ask Before Rewriting Ambiguous Parts
- If a bullet point is vague or could be interpreted multiple ways, ask a clarifying question before rewriting it.
- Example: "你这里写了'参与产品迭代'，能告诉我你具体负责了哪些环节吗？是需求分析、原型设计还是上线跟进？"
- Batch questions when possible — don't ask one at a time if several ambiguities exist.

### 3. No AI Smell
- Avoid: generic buzzwords, hollow phrases like "负责推动跨团队协作", filler words, passive constructions without subject.
- Prefer: concrete numbers, named features/products, specific outcomes, active subject + verb + result structure.
- Read each bullet out loud mentally — if it sounds like a chatbot wrote it, rewrite it.

### 4. JD-Driven Prioritization
- Identify the **top 3–5 core competencies** the JD is looking for.
- Reorder and rewrite bullet points to front-load the most relevant experience.
- De-emphasize or cut bullet points that are irrelevant to this specific role.
- Mirror the language and framing of the JD where it fits naturally (not verbatim copy-paste).

### 5. Honest HR-Eye Feedback at the End
- After delivering the tailored resume, provide a **candid evaluation from an HR perspective**.
- This is NOT a compliment session. Point out:
  - Genuine strengths that will resonate with this JD
  - Weaknesses or gaps that a recruiter will notice
  - Whether the overall fit is strong, moderate, or weak — and why
  - One or two specific things the candidate could do (outside of resume editing) to strengthen their profile for this type of role
- Tone: direct, honest, like a recruiter giving internal feedback — not a coach trying to motivate.

---

## Workflow

### Step 1: Parse Inputs
- Extract resume content from PDF
- Read JD carefully
- Identify: role level, core responsibilities, must-have skills, nice-to-have skills, company type/stage

### Step 2: Gap & Match Analysis (internal, don't show user)
- Map resume experiences → JD requirements
- Note strong matches, weak matches, and gaps
- Flag ambiguous bullet points that need clarification

### Step 3: Ask Clarifying Questions (if needed)
- Batch all questions together
- Be specific: quote the original text and explain why you need clarification
- Wait for answers before rewriting

### Step 4: Rewrite
- Rewrite bullet points that are relevant but poorly framed
- Reorder sections/bullets to match JD priority
- Cut or compress low-relevance content
- Preserve any bullet points that are already strong and JD-relevant

### Step 5: Deliver Tailored Resume
- Present the revised resume clearly (section by section or full)
- Briefly note what changed and why (2–3 sentence summary, not a list of every edit)

### Step 6: HR Perspective Feedback
- Deliver honest, unvarnished evaluation
- Format: short paragraphs, not bullet points
- End with 1–2 actionable suggestions beyond the resume itself

---

## Bullet Point Rewriting Guide

### 核心框架：STAR 法则

每一条 bullet point 的改写都应以 STAR 结构为骨架展开：

| 要素 | 含义 | 写法提示 |
|---|---|---|
| **S – Situation** | 背景/处境 | 当时面临什么问题、挑战或业务背景？（通常压缩成半句话带过，不展开） |
| **T – Task** | 你的职责/任务 | 你在这件事里的角色和目标是什么？ |
| **A – Action** | 你的具体行动 | 你做了什么？怎么做的？（这是重点，要具体） |
| **R – Result** | 结果/影响 | 产出了什么？有没有数据？没有数据就用规模、时间节点、影响范围代替 |

**简历 bullet point 的 STAR 写法节奏**：
> [背景/问题（S+T，选写）] + 主导/负责 [具体行动 A] + 最终 [结果 R]

不是每条都需要完整的四个要素，但 **A（Action）和 R（Result）是必须的**。S 和 T 按需压缩带出即可，不要把简历写成小作文。

---

### 改写示例

| Before（弱） | After（STAR 改写） |
|---|---|
| 负责产品需求的整理和跟进 | 针对XX业务线需求积压问题（S），主导建立需求优先级评估机制（A），推动研发/设计/运营协同，季度内清理积压需求XX条，版本交付准时率从60%提升至90%（R） |
| 参与数据分析，优化产品体验 | 发现用户注册流程跳失率异常（S），独立拆解漏斗并定位核心断点（A），推动改版上线后注册转化率提升X%（R） |
| 跨团队协作推动项目落地 | 作为唯一PM统筹市场、客服、技术三方（T），制定里程碑计划并周会推进（A），XX项目在Y周内完成MVP上线，DAU首周达XX（R） |

---

### Rewriting Rules（改写规则）

- 动词开头，用主动态（主导、搭建、推动、设计、拆解、优化、制定…）
- A（Action）要具体：写"拆解漏斗找断点"而不是"进行了数据分析"
- R（Result）能量化就量化；没有数字就用：用户量级、团队规模、时间节点、覆盖范围
- S/T 背景尽量压缩进半句话，不要喧宾夺主
- 读起来像一个真实的人在描述真实做过的事——不是 KPI 汇报，不是 PPT 标题

---

### 无真实数据时的处理规则：用业务思维替代数据

当项目为个人项目或尚未落地，没有真实运营数据时，**禁止编造数字**，改用以下方式体现业务价值：

#### 1. 展示决策逻辑（为什么这么设计）
不写结果，写你的判断依据——体现你在想什么，而不只是做了什么。

> ❌ 弱：设计了用户onboarding流程
> ✅ 强：针对冷启动用户流失问题，判断核心卡点在首次使用门槛过高，
>        设计分步引导+空状态激励的onboarding方案，
>        预计可将D1留存从行业均值X%提升至Y%（基于竞品拆解推算）

#### 2. 引用行业/竞品数据作为参照系
用外部数据锚定你方案的合理性，体现你对市场的理解。

> ✅ 参考同类产品（XX、XX）的定价模型与转化路径，
>    设计订阅分层策略，核心逻辑是降低首单门槛、以低价SKU拉动LTV

#### 3. 描述设计取舍（Tradeoff）
体现你做过真正的产品决策，而不是"把所有功能都加上"。

> ✅ 在功能范围上放弃了XX模块（开发成本高、用户感知弱），
>    优先打通XX核心路径，以最小MVP验证核心假设

#### 4. 用"预期验证指标"代替结果数据
未落地不等于没有思考，写出你打算用什么指标来验证方案，
体现你懂得如何定义成功。

> ✅ 方案设计阶段即确定核心验证指标为D7留存率与功能使用深度，
>    并预埋相应埋点，待灰度上线后进行A/B验证

**总原则**：没有数据时，HR 想看的不是结果，而是你的**思考链**——
你发现了什么问题 → 你怎么判断优先级 → 你做了什么取舍 → 你打算怎么验证。
这比一个来路不明的"提升了30%"更有说服力。

---

## Out of Scope
- Do not write a cover letter unless asked
- Do not suggest entirely new sections (e.g., adding a "personal projects" section) unless the gap is critical and you flag it as a suggestion, not a rewrite
- Do not translate the resume unless asked
