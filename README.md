# web-ui-autotest

一个给 Codex 使用的 Web UI 自动化测试 skill。  
A Web UI automation testing skill for Codex.

## Covers | 支持内容

- UI 自动化测试框架骨架生成
- 基于页面结构的测试用例生成
- 首次实践复盘记录

- UI automation framework scaffolding
- Test case generation from page structure
- First-practice review recording

## Install | 安装

下载或克隆本仓库后，直接把仓库目录作为 skill 使用即可。  
Download or clone this repository, then use the repository directory directly as the skill root.

## Use | 使用示例

### 1. Framework

```text
Use $web-ui-autotest to generate a Web UI automation framework skeleton.
Keep the stack fixed to Python + Playwright for Python + Pytest + POM + Allure.
```

```text
使用 $web-ui-autotest 生成 Web UI 自动化测试框架骨架。
技术栈固定为 Python + Playwright for Python + Pytest + POM + Allure。
```

### 2. Test Cases

```text
Use $web-ui-autotest to inspect the page structure first, then generate structured test cases.
```

```text
使用 $web-ui-autotest 先识别页面结构，再生成结构化测试用例。
```

### 3. First Practice Review

```text
Use $web-ui-autotest to record the first real execution and summarize issues and suggested rule updates.
```

```text
使用 $web-ui-autotest 记录首次真实实践，并总结问题点和建议回写内容。
```

## Structure | 结构

```text
web-ui-autotest/
├─ SKILL.md
├─ agents/openai.yaml
└─ references/
   ├─ framework-generation-spec.md
   ├─ framework-generation-execution-template.md
   ├─ test-case-instruction-set.md
   └─ first-practice-review-template.md
```

## References | 文档映射

- `framework-generation-spec.md`: 框架骨架生成规范 / framework scaffolding rules
- `framework-generation-execution-template.md`: 框架生成调用模板 / framework execution template
- `test-case-instruction-set.md`: 测试用例规则 / test case instruction set
- `first-practice-review-template.md`: 首次实践复盘模板 / first-practice review template
