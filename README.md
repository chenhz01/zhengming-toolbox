# zhengming-toolbox

> A toolbox of **55 purpose-built, score-first-designed AI-engineering tools**, each targeting a niche where no direct equivalent existed (verified by pre-construction anchor searches as of 2026-10-12). Pure standard-library Python, CLI-first, self-tested.

## Why score-first?

Every tool was reverse-designed against a quality rubric (novelty vs. existing anchors, test depth >= 40 cases, measured evidence) **before** construction — predicted scores matched actual audits 55/55 across two rounds. See the methodology note at the bottom.

## Flagships (no direct equivalent found — true zero-anchor niches)

- [instruction-dsl-lint](https://github.com/chenhz01/instruction-dsl-lint) — AI 指令模板的 DSL 规范+校验器
- [json-output-salvage](https://github.com/chenhz01/json-output-salvage) — LLM 输出 JSON 抢修器
- [md-table-lint](https://github.com/chenhz01/md-table-lint) — Markdown 表格校验器
- [focus-data-aggregator](https://github.com/chenhz01/focus-data-aggregator) — 专注数据聚合规范
- [vector-meta-schema](https://github.com/chenhz01/vector-meta-schema) — 向量库元数据规范
- [complexity-budget-gate](https://github.com/chenhz01/complexity-budget-gate) — 复杂度预算闸
- [timezone-safety-check](https://github.com/chenhz01/timezone-safety-check) — 时区安全检查器
- [dead-code-quantifier](https://github.com/chenhz01/dead-code-quantifier) — 死代码量化器

## Score-first batch 1 (R12, live)

- [schema-clamp](https://github.com/chenhz01/schema-clamp) — Validate & auto-repair LLM JSON output against a JSON-Schema subset, with violation paths and fix suggestions.
- [invariant-guard-gen](https://github.com/chenhz01/invariant-guard-gen) — Turn docstring invariants into property-based checkers for AI-generated code.
- [model-origin-ledger](https://github.com/chenhz01/model-origin-ledger) — Tamper-evident hash-chain ledger for AI model/dataset provenance with license-conflict audits.
- [x402-receipt-reconciler](https://github.com/chenhz01/x402-receipt-reconciler) — Exactly-once reconciliation for x402 agent payments: duplicate detection, amount mismatch, timeout reports.
- [nl2sql-schema-drift](https://github.com/chenhz01/nl2sql-schema-drift) — Detect drift between semantic-layer definitions and real database schemas before NL2SQL queries break.

## The 50-tool catalog (R13 batch)


### AI Instruction & Prompt Engineering (8)

- [instruction-dsl-lint](https://github.com/chenhz01/instruction-dsl-lint) — AI 指令模板的 DSL 规范+校验器
- [prompt-regression-harness](https://github.com/chenhz01/prompt-regression-harness) — 记录提示词→期望断言的回归测试架
- [prompt-version-diff](https://github.com/chenhz01/prompt-version-diff) — 两版提示词的结构化 diff（指令段/示例段/约束段分级 + 语义风险标注）
- [prompt-template-merge](https://github.com/chenhz01/prompt-template-merge) — 提示词模板继承合并器
- [token-budget-clamp](https://github.com/chenhz01/token-budget-clamp) — 提示词 token 预算钳
- [context-pack-planner](https://github.com/chenhz01/context-pack-planner) — 上下文窗口打包规划器
- [llm-cache-key-spec](https://github.com/chenhz01/llm-cache-key-spec) — LLM 缓存键规范
- [fewshot-picker-bench](https://github.com/chenhz01/fewshot-picker-bench) — few-shot 样例选择基准

### Agent & LLM Governance (9)

- [agent-audit-trail](https://github.com/chenhz01/agent-audit-trail) — Agent 行为审计轨迹规范
- [tool-call-replay](https://github.com/chenhz01/tool-call-replay) — Agent 工具调用录制重放器
- [model-capability-matrix](https://github.com/chenhz01/model-capability-matrix) — 模型能力矩阵规范
- [model-arbitration-spec](https://github.com/chenhz01/model-arbitration-spec) — 多模型仲裁协议
- [embedding-drift-watch](https://github.com/chenhz01/embedding-drift-watch) — 嵌入漂移监测规范
- [vector-meta-schema](https://github.com/chenhz01/vector-meta-schema) — 向量库元数据规范
- [llm-gateway-spec](https://github.com/chenhz01/llm-gateway-spec) — LLM 网关接口规范
- [system-prompt-audit](https://github.com/chenhz01/system-prompt-audit) — 系统提示词静态审计器
- [rag-chunk-bench](https://github.com/chenhz01/rag-chunk-bench) — RAG 分块策略基准

### Code Engineering & Quality (10)

- [json-output-salvage](https://github.com/chenhz01/json-output-salvage) — LLM 输出 JSON 抢修器
- [dead-code-quantifier](https://github.com/chenhz01/dead-code-quantifier) — 死代码量化器
- [complexity-budget-gate](https://github.com/chenhz01/complexity-budget-gate) — 复杂度预算闸
- [comment-drift-check](https://github.com/chenhz01/comment-drift-check) — 注释漂移检测
- [deprecated-api-scan](https://github.com/chenhz01/deprecated-api-scan) — 弃用 API 使用扫描
- [doc-rot-detector](https://github.com/chenhz01/doc-rot-detector) — 文档腐化检测器
- [readme-quality-score](https://github.com/chenhz01/readme-quality-score) — README 质量评分器
- [changelog-semantic-lint](https://github.com/chenhz01/changelog-semantic-lint) — CHANGELOG 语义校验
- [api-contract-drift](https://github.com/chenhz01/api-contract-drift) — API 契约漂移检测
- [schema-evolution-grader](https://github.com/chenhz01/schema-evolution-grader) — Schema 演进兼容性分级

### Security & Compliance (7)

- [log-redaction-spec](https://github.com/chenhz01/log-redaction-spec) — 日志脱敏规范
- [secret-rotation-check](https://github.com/chenhz01/secret-rotation-check) — 密钥轮换检查器
- [retention-policy-check](https://github.com/chenhz01/retention-policy-check) — 数据保留策略校验器
- [ai-commit-disclosure](https://github.com/chenhz01/ai-commit-disclosure) — AI 提交披露检查器
- [lockfile-audit-diff](https://github.com/chenhz01/lockfile-audit-diff) — 锁文件审计
- [money-precision-check](https://github.com/chenhz01/money-precision-check) — 金额精度检查器
- [unit-confusion-check](https://github.com/chenhz01/unit-confusion-check) — 单位混淆检查

### Data & Consistency (8)

- [csv-dialect-fingerprint](https://github.com/chenhz01/csv-dialect-fingerprint) — CSV 方言指纹
- [md-table-lint](https://github.com/chenhz01/md-table-lint) — Markdown 表格校验器
- [event-replay-verifier](https://github.com/chenhz01/event-replay-verifier) — 事件溯源重放校验器
- [idempotency-key-spec](https://github.com/chenhz01/idempotency-key-spec) — 幂等键规范
- [timezone-safety-check](https://github.com/chenhz01/timezone-safety-check) — 时区安全检查器
- [calendar-conflict-check](https://github.com/chenhz01/calendar-conflict-check) — 日历冲突检测
- [claim-verification-chain](https://github.com/chenhz01/claim-verification-chain) — 断言校验链
- [lock-contract-test](https://github.com/chenhz01/lock-contract-test) — 分布式锁契约测试

### Process & Collaboration (8)

- [git-history-hygiene](https://github.com/chenhz01/git-history-hygiene) — Git 历史卫生审计
- [todo-expiry-ledger](https://github.com/chenhz01/todo-expiry-ledger) — TODO 期限账本
- [self-heal-runbook](https://github.com/chenhz01/self-heal-runbook) — 自愈运行手册规范
- [deploy-checklist-code](https://github.com/chenhz01/deploy-checklist-code) — 部署清单即代码
- [quota-aware-scheduler](https://github.com/chenhz01/quota-aware-scheduler) — 配额感知调度器规范
- [meeting-notes-to-tasks](https://github.com/chenhz01/meeting-notes-to-tasks) — 会议纪要→任务转换规范
- [email-triage-spec](https://github.com/chenhz01/email-triage-spec) — 邮件分诊规范
- [focus-data-aggregator](https://github.com/chenhz01/focus-data-aggregator) — 专注数据聚合规范

## Earlier releases

52 additional utility tools were released on 2026-10-10/11 (Rounds R10-R11): defensive security scanners, MCP cleanroom acceptance harnesses, and developer workflow tools — see the [repositories list](https://github.com/chenhz01?tab=repositories).

## Roadmap

- CI on every repo (self-test runs on each push) — rolling out with this release

- Feedback-driven selection: 30-day star/issue data feeds the next round's niche choices

- Iteration tiers: repos with traction get v0.2 feature depth; zero-signal niches get SEO tuning or archival review


## Methodology: reverse score-first design

1. Pre-construction anchor search (per niche, multiple queries) — no direct equivalent, or mechanism-inverted positioning vs. weak anchors

2. Predicted score committed to a design contract before any code

3. Construction under hard gates: >= 40 self-test cases (functional / exception / extreme-edge), two iteration rounds with changelog evidence

4. Independent master audit re-runs every self-test; predicted vs. actual scores reconciled (55/55 match so far)


## License

All tools MIT — © zhengming contributors. Contact: hcac4735@agent.qq.com
