# Creation Handoff

> 2026-09-20 本地维护 0.3.4：英文 README 改用独立英文 SVG，中文版继续使用中文图；运行逻辑与显式调用策略保持不变。本次尚未发布远端版本。

> 2026-09-07 本地维护 0.3.1：分析收敛后继续已授权实施，核查范围尊重明确请求；以下历史候选研究不等于新版本效果对比。

## 1. Result

- Skill：suming-first-principles 0.3.0
- 职责：显式调用后，从真实痛点和基本事实推导最低需求，拿掉现成方案后重建可验证选择。
- 系统级安装目录：`~/.codex/skills/suming-first-principles`
- 发布状态：本地系统级版本已更新；未发布到 GitHub 或 Skill 市场。
- 结构：沿用原包，不新增 references、脚本、状态文件或其他 Skill。

## 2. Core redesign

- 主流程收敛为“真实痛点 → 基本事实 → 拿掉现成方案 → 最低需求 → 重建方案 → 最小验证”。
- 建设类问题改为先推导需求，再检查本地、官方、已安装能力、GitHub 和真实案例；找到 1—3 个有效候选后停止。
- 保持现状不再是默认优先项，同时比较行动、探索、缩小试验、替代方案、机会成本和失败代价。
- 低成本可逆选择直接给最小试验；高成本且真实可争议的选择才使用双向钢人。
- 最近使用频率和公开热度都只作为线索，不单独决定保留、删除或采用。
- 长对话采用后来明确确认的新要求；其他 Skill 影响只检查直接关系。
- 是否值得做由本 Skill 判断；今天是否做、是否偏离主线和优先级交给 $suming。
- 用户要求开始执行时立即收敛并退出分析，不继续访谈。

## 3. Prior-art review

通过 agent-reach 的 GitHub 路由只读检查了 3 个候选：

- mindfold-ai/Trellis：方法完整但固定阶段、数量门槛、文件写入和项目集成过重；
- cursor/plugins：从零重建设计的原则清楚，但只适用于已有软件设计变更；
- guia-matthieu/clawfu-skills：包含原子拆解和最小试验，但模板过长且偏物理与成本场景。

结论：不直接复用；只吸收三个候选共同支持的“去掉现成方案、向上重建、最小验证”。本机 npx 10.9.8 已确认可用，旧报告中的 npx 缺失结论已修正。

## 4. Verification

- 标准 quick_validate.py：通过，Skill is valid；
- 包结构 validate_skill.py：通过，0 failures、0 warnings；
- trigger_eval.py：通过，28/28，0 false positive、0 false negative；
- export_skill_ir.py：通过，名称和版本与 manifest 对齐；
- 静态输出契约：14 个场景，覆盖需求先于搜索、低频能力判断、直接关联影响、最新约束、风险适配、$suming 边界和执行交接；
- 主 SKILL.md：200 行，短于升级前的 252 行；
- JSON、YAML、UTF-8 和完整回读：通过。

## 5. Evidence limits

- provider-backed 输出对比尚未执行；
- 没有保存无 Skill 基线，也没有进行独立人工盲测；
- 跨宿主显式调用稳定性仍为 missing evidence；
- 本次未安装、执行或复制任何公开候选 Skill。
