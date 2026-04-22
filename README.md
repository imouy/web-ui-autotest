# web-ui-autotest

一个面向 Codex 的单一 skill，用于统一承载 Web UI 自动化测试框架骨架生成、基于页面结构的测试用例生成，以及首次实践复盘记录。  
A single Codex skill that unifies Web UI automation framework scaffolding, page-structure-based test case generation, and first-practice review recording.

## What This Skill Covers | 这个 Skill 能做什么

### 1. UI automation framework scaffolding | UI 自动化框架骨架生成

- Generate a standardized Web UI automation framework skeleton.
- Keep the stack fixed to Python, Playwright for Python, Pytest, POM, and Allure.
- Preserve clear layering for `config`, `data`, `pages`, `tests`, `utils`, `reports`, and `artifacts`.

- 生成标准化的 Web UI 自动化测试框架骨架。
- 固定技术栈为 Python、Playwright for Python、Pytest、POM、Allure。
- 保持 `config`、`data`、`pages`、`tests`、`utils`、`reports`、`artifacts` 等层次清晰。

### 2. Test case generation from page structure | 基于页面结构的测试用例生成

- Identify visible page structure before generating test cases.
- Map element types to predefined test-point categories.
- Output structured test cases with complete template fields.

- 在生成测试用例前先识别页面可见结构。
- 将元素类型映射到预定义测试点类别。
- 输出带完整模板字段的结构化测试用例。

### 3. First-practice review recording | 首次实践复盘记录

- Record the first real project execution of the framework-generation workflow.
- Capture inputs, outputs, gaps, ambiguities, and next-round fixes.
- Support rule write-back for future refinement.

- 记录框架生成规范的首次真实项目实践过程。
- 沉淀输入、输出、问题点、歧义点与下一轮修订项。
- 为后续规则回写和迭代提供依据。

## What This Skill Does Not Change | 这个 Skill 不改什么

- It does not rewrite the original rule logic.
- It does not switch the defined framework-generation stack.
- It does not fabricate business details when input is incomplete.
- It does not merge unrelated tasks into a single vague workflow.

- 不改写原始规则逻辑。
- 不切换框架生成任务中已定义的技术栈。
- 输入不足时不伪造业务细节。
- 不把边界不同的任务混成一个模糊流程。

## Repository Structure | 仓库结构

```text
web-ui-autotest/
├─ SKILL.md
├─ README.md
├─ agents/
│  └─ openai.yaml
└─ references/
   ├─ framework-generation-spec.md
   ├─ framework-generation-execution-template.md
   ├─ test-case-instruction-set.md
   └─ first-practice-review-template.md
```

- `SKILL.md`
  Main entry for task routing and operating rules.
- `agents/openai.yaml`
  UI-facing metadata for the skill.
- `references/framework-generation-spec.md`
  Source-of-truth rules for UI automation framework scaffolding.
- `references/framework-generation-execution-template.md`
  Invocation template, input template, output receipt, and acceptance guide for framework generation.
- `references/test-case-instruction-set.md`
  Source-of-truth rules for page recognition and structured test case generation.
- `references/first-practice-review-template.md`
  Template for recording the first real execution and feeding issues back into the rule set.

- `SKILL.md`
  任务分流与执行原则入口。
- `agents/openai.yaml`
  skill 的界面元数据配置。
- `references/framework-generation-spec.md`
  UI 自动化测试框架骨架生成的真源规范。
- `references/framework-generation-execution-template.md`
  框架生成任务的调用模板、输入模板、输出回执与验收说明。
- `references/test-case-instruction-set.md`
  页面识别与结构化测试用例生成的真源规则。
- `references/first-practice-review-template.md`
  首次真实执行后的复盘记录模板与规则回写依据。

## Installation | 安装方式

### Option 1. Use as a local skill directory | 方式一：作为本地 skill 目录使用

Clone or download this repository, then place the `web-ui-autotest` folder under your local Codex skills directory.

克隆或下载本仓库后，将 `web-ui-autotest` 目录放入本地 Codex skills 目录中使用。

### Option 2. Keep the repository as the skill root | 方式二：直接将仓库作为 skill 根目录

Because the repository root already matches the skill structure, it can be used directly as a distributable skill package.

由于仓库根目录本身就是完整 skill 结构，因此可以直接作为可分发的 skill 包使用。

## Usage Examples | 调用示例

### Example 1. Framework scaffolding | 示例 1：框架骨架生成

```text
Use $web-ui-autotest to generate a Web UI automation framework skeleton for a CRM system.
Stack must stay Python + Playwright for Python + Pytest + POM + Allure.
If input is missing, keep placeholders instead of inventing business details.
```

```text
使用 $web-ui-autotest 为一个 CRM 系统生成 Web UI 自动化测试框架骨架。
技术栈必须固定为 Python + Playwright for Python + Pytest + POM + Allure。
如果输入不足，请保留占位，不要伪造业务细节。
```

### Example 2. Test case generation | 示例 2：测试用例生成

```text
Use $web-ui-autotest to inspect the visible page structure first, then generate structured test cases.
Do not skip page recognition, and keep each case traceable to the instruction set.
```

```text
使用 $web-ui-autotest 先识别页面可见结构，再生成结构化测试用例。
不要跳过页面识别，并确保每条用例都能映射回指令集来源。
```

### Example 3. First-practice review | 示例 3：首次实践复盘

```text
Use $web-ui-autotest to record the first real execution of the framework-generation workflow.
Summarize inputs, actual outputs, issues, ambiguities, and suggested rule updates.
```

```text
使用 $web-ui-autotest 记录框架生成流程的首次真实实践。
请整理输入、实际输出、问题点、歧义点以及建议回写到规则中的内容。
```

## Reference Mapping | 文档映射关系

| Reference file | Purpose | 中文用途 |
| --- | --- | --- |
| `references/framework-generation-spec.md` | Defines the fixed structure, responsibilities, technical stack, and acceptance checks for framework scaffolding. | 定义框架骨架生成的固定结构、职责边界、技术栈与合格标准。 |
| `references/framework-generation-execution-template.md` | Defines how the framework-generation workflow should be invoked, what inputs should be provided, and how outputs should be reported. | 定义框架生成任务的调用方式、输入项与输出回执格式。 |
| `references/test-case-instruction-set.md` | Defines page recognition rules and structured test case generation rules. | 定义页面识别规则与结构化测试用例生成规则。 |
| `references/first-practice-review-template.md` | Defines how to record the first real-world practice and feed discoveries back into the rule set. | 定义首次实践的记录方式，以及如何将发现回写进规则体系。 |

## Design Principles | 设计原则

- Single skill entry, multiple task routes.
- Original reference documents remain the source of truth.
- `SKILL.md` handles routing and operating discipline, not rule replacement.
- `README.md` explains navigation and usage, not rule substitution.

- 单一 skill 入口，多任务分流。
- 原始 reference 文档保持真源地位。
- `SKILL.md` 负责路由与执行约束，不替代规则正文。
- `README.md` 负责导航与使用说明，不替代规则正文。
