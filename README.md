# 第一性原理

`$suming-first-principles` 是一个仅手动调用的 Agent Skill。它把任务、方案或概念拆回真实痛点和基本事实，拿掉现成方案，推导最低需求，再重建可验证的选择。

当前版本：0.3.1

## 核心流程

~~~text
真实痛点 → 基本事实 → 拿掉现成方案 → 最低需求 → 重建方案 → 最小验证
~~~

建设类问题只有在最低需求明确后，才检查本地和历史决定、官方原生能力、已安装插件或服务、GitHub 与真实案例。找到 1—3 个足够接近的候选后停止，并在直接复用、最小改造和确有必要才自建之间判断。

保持现状不是默认答案。Skill 会同时考虑行动价值、探索价值、机会成本、失败代价和可逆性：低成本选择直接给最小试验，高成本且难回退的选择才升级反方检验或双向钢人。

## 你可以直接这样说

~~~text
$suming-first-principles 帮我判断，这两个学习 Skill 是否应该融合。
~~~

~~~text
$suming-first-principles 这个工具最近没用过，是否应该卸载？
~~~

~~~text
$suming-first-principles 拆解“工作流自动化”的本质、成立条件和边界。
~~~

## 输出

任务或方案默认只给真实目标、底层事实与约束、关键假设、当前判断和最小验证。候选方案比较和双向钢人只在实际触发时出现，不机械填满固定模板。

概念类继续输出一句话本质、成立条件、不适用边界和直观例子。分析请求默认只读、不自动监控；用户已授权实施时，收敛分析后由主代理继续执行与验证，不把退出本 Skill 当作结束任务。0.3.1 同时明确复用充分证据、尊重显式全量审阅范围。

## 边界

- 普通教学使用 $suming-learn-explain。
- 模糊产品或 MVP 访谈使用 $suming-product-discovery。
- 长对话整理按用户要求直接处理当前上下文。
- 今天是否做、是否跑偏和优先级安排交给 $suming。
- 单纯搜索、摘要、翻译和路径已明确的执行任务不调用本 Skill。

## 验证

仓库维护者可以使用兼容的 `validate_skill.py` 和随包测试材料进行验证：

~~~bash
python3 /path/to/validate_skill.py .
npx skills add try-suming/suming-first-principles --list
~~~

现有报告覆盖结构、触发边界和输出案例；真实模型输出改善及跨宿主稳定性仍属于 missing evidence。

## 安装

~~~bash
npx skills add try-suming/suming-first-principles
~~~

### 前置条件

- [ ] 使用支持 Agent Skills 的宿主。
- [ ] 通过上述命令安装时，已安装 Node.js 与 `npx`。
- [ ] 已理解本 Skill 默认只分析；外部搜索和实际执行仍受宿主权限与用户授权约束。

## Troubleshooting

- 找不到 Skill：确认目录存在后刷新或重新打开 Codex。
- 没有自动调用：这是设计行为，必须明确调用 $suming-first-principles 或要求使用第一性原理。
- 回答总在劝退：检查是否同时比较了行动、探索、缩小试验和保持现状。
- 搜索越来越长：找到 1—3 个有效候选后应停止。
- 一直提问：每轮最多一个关键问题，得到关键答案后必须收敛。

## 致谢

Upstream inspiration: suming-meta-skill: reusable skill packaging, trigger boundaries, and evidence-bound validation

## License

MIT
