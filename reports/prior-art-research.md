# Prior-Art Research

- Researched at: 2026-08-30
- Route: agent-reach GitHub route / gh CLI
- Queries: "First Principles Thinking" filename:SKILL.md; first-principles filename:SKILL.md; first principles agent skill
- Authentication: GitHub account available for read-only search
- Stop condition: stop after 3 sufficiently close, reviewable candidates
- Local environment: npx 10.9.8 is available

## Shortlist

### 1. mindfold-ai/Trellis — first-principles-thinking

- Repository: https://github.com/mindfold-ai/Trellis
- File: .agents/skills/first-principles-thinking/SKILL.md
- Observed at search time: 14,317 Stars; repository updated 2026-08-30; repository license reports AGPL-3.0 while the Skill file declares MIT, so reuse licensing is not treated as settled.
- Useful ideas: identify the problem essence, challenge assumptions, reason upward from ground truths, and end with a smallest test.
- Rejected as a direct replacement: mandatory 6 phases, fixed minimum counts, progress artifacts, Trellis file writes and long templates are heavier than this personal explicit-call Skill needs.

### 2. cursor/plugins — principle-redesign-from-first-principles

- Repository: https://github.com/cursor/plugins
- File: pstack/skills/principle-redesign-from-first-principles/SKILL.md
- Observed at search time: 6,225 Stars; repository updated 2026-08-30; no repository license was returned by gh.
- Useful idea: treat a new requirement as foundational and ask what would be designed from scratch, instead of bolting it onto the current solution.
- Rejected as a direct replacement: it is intentionally limited to integrating requirements into an existing software design and does not cover personal decisions, task necessity or concept boundaries.

### 3. guia-matthieu/clawfu-skills — first-principles

- Repository: https://github.com/guia-matthieu/clawfu-skills
- File: skills/strategy/first-principles/SKILL.md
- Observed at search time: 145 Stars; repository updated 2026-08-12; MIT license.
- Useful ideas: separate assumptions from fundamentals, rebuild from minimum requirements, and finish with a first experiment.
- Rejected as a direct replacement: the Skill is long, template-heavy, marketing-oriented and often frames constraints as physics versus convention, which does not transfer cleanly to relationships, learning, software governance or personal choices.

## Keep / Adapt / Reject / Invent

- **keep**：保留显式调用、跨领域、一次一问、事实与假设分离、条件式双向钢人和证据边界。
- **adapt**：吸收三个候选共同支持的“拿掉当前方案 → 从最低需求向上重建 → 最小验证”，但不复制固定阶段、文件产物或模板数量。
- **reject**：不采用强制三条公理、五条假设、固定六阶段、全程进度表、默认文件写入和把所有问题还原为物理规律。
- **invent**：结合用户近期使用场景，加入有界成熟方案搜索、非保守默认、低频高后果例外、最新要求优先、直接相关 Skill 影响范围和与 $suming 的时机边界。

## Evidence boundary

- 以上候选内容和仓库元数据均在 2026-08-30 通过 gh 只读取得。
- 搜索达到 3 个足够接近的候选后按停止条件结束，没有继续追逐理论最优。
- 旧报告中“当前环境无法解析 npx”的说法已经过期；本次实测 npx 10.9.8 可用。
- 没有安装、复制或执行候选 Skill。
- provider-backed 输出对比、跨宿主调用稳定性和人工盲测仍属于 missing evidence。
