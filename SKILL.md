---
name: web-ui-autotest
description: Use when Codex needs one skill for Web UI 自动化测试工作: generate a Python + Playwright for Python + Pytest + POM + Allure framework skeleton, derive structured test cases from real page structure, or record the first practice review. Trigger on requests about UI automation scaffolds, page-structure-based test cases, or first-run retrospective templates without inventing missing business details.
---

# Web UI AutoTest

## Overview

Use this skill as the single entry point for the project's existing Web UI 自动化测试规则.
Keep the logic in the bundled reference documents intact. Do not relax constraints, switch stacks, or fabricate business details that the references do not allow.

## Task Routing

- When the user asks to generate a UI 自动化测试框架骨架, read:
  - [references/framework-generation-spec.md](references/framework-generation-spec.md)
  - [references/framework-generation-execution-template.md](references/framework-generation-execution-template.md)
- When the user asks to identify page structure and generate 测试用例, read:
  - [references/test-case-instruction-set.md](references/test-case-instruction-set.md)
- When the user asks to record or review the first real execution/practice, read:
  - [references/first-practice-review-template.md](references/first-practice-review-template.md)
- When the user asks for a combined task, load only the relevant reference files above and apply them together without rewriting their rules.

## Operating Rules

- Treat the reference documents as the source of truth.
- Preserve the original task boundaries:
  - framework generation is not the same task as business test case generation
  - first-practice review is not an execution prompt for framework generation
- Keep the framework-generation stack fixed when that workflow is selected:
  - Python
  - Playwright for Python
  - Pytest
  - POM
  - Allure
- When input is incomplete, keep placeholders, generic skeletons, or `待确认` markers instead of inventing business rules, hidden elements, backend validation, or permission details.
- When generating test cases, keep the template fields complete and keep each case traceable back to the corresponding rule set.
- When generating framework output, keep structure, layering, reporting, and evidence rules aligned with the references; do not silently simplify them.

## Reference Map

- [references/framework-generation-spec.md](references/framework-generation-spec.md)
  Primary rule set for generating the UI 自动化测试框架骨架.
- [references/framework-generation-execution-template.md](references/framework-generation-execution-template.md)
  Invocation template, input template, output receipt, and acceptance guidance for framework generation.
- [references/test-case-instruction-set.md](references/test-case-instruction-set.md)
  Page-structure recognition rules and structured test-case generation rules.
- [references/first-practice-review-template.md](references/first-practice-review-template.md)
  Retrospective template for the first real project run and rule write-back.

## Output Discipline

- Keep the original logic in the bundled references intact.
- Add only routing, selection, and task-scoping behavior in this `SKILL.md`.
- If a request exceeds what the references define, state the gap clearly instead of inventing new rules.
