<p align="center">
  <strong>简体中文</strong> · <a href="./README_EN.md">English</a>
</p>

<h1 align="center">第一性原理</h1>

<p align="center">从真实痛点和基本事实重建可验证方案，而不是被现成做法牵着走。</p>

<p align="center">
  <a href="https://github.com/shilefumaoqu/suming-first-principles/releases"><img alt="GitHub Release" src="https://img.shields.io/github/v/release/shilefumaoqu/suming-first-principles?display_name=tag&sort=semver"></a>
  <a href="https://github.com/shilefumaoqu/suming-first-principles/commits/main"><img alt="Last commit" src="https://img.shields.io/github/last-commit/shilefumaoqu/suming-first-principles?style=flat-square"></a>
  <a href="./LICENSE"><img alt="License" src="https://img.shields.io/github/license/shilefumaoqu/suming-first-principles?style=flat-square"></a>
</p>

<p align="center">
  <a href="#效果示例">效果示例</a> · <a href="#安装">安装</a> ·
  <a href="#核心流程">核心流程</a> · <a href="#边界">边界</a>
</p>

![第一性原理六步推导流程](docs/assets/first-principles-flow.svg)

```bash
npx skills add shilefumaoqu/suming-first-principles
```

当前版本：0.3.5

## 效果示例

你问：

```text
$suming-first-principles 这两个学习 Skill 要不要融合？
```

它不会因为功能相似就直接建议合并，而会先检查：

- 两者解决的是不是同一个真实问题；
- 用户在什么场景下难以选择；
- 合并会不会让触发范围变模糊、上下文变重；
- 保留两个入口、调整命名或明确边界，是否已经能解决痛点。

最终交付的是“保留、合并、缩小或换方案”的明确判断、成立条件和最小验证，而不是一份抽象方法论。

## 30 秒理解

这个 Skill 不负责机械套用“第一性原理模板”。它先确认真正要解决的问题，区分事实、约束、决定、假设和未知；暂时拿掉当前方案，推导最低需求，再判断应该复用、改造还是重新构建。

建设类问题只有在最低需求明确后，才检查本地能力、官方方案、已安装工具、GitHub 与真实案例。找到 1—3 个足够接近的候选后停止，不为了寻找理论最优无限搜索。

## 你可以直接这样说

```text
$suming-first-principles 帮我判断，这两个学习 Skill 是否应该融合。
```

```text
$suming-first-principles 这个工具最近没用过，是否应该卸载？
```

```text
$suming-first-principles 拆解“工作流自动化”的本质、成立条件和边界。
```

## 使用前后有什么不同

| 原问题 | 使用后得到 |
|---|---|
| “这两个 Skill 要不要合并？” | 检查职责冲突、真实使用障碍和合并代价，再判断保留、调整边界或合并 |
| “这个工具很少用，要不要卸载？” | 同时检查不可替代性、低频高后果价值和重新安装成本，不只看使用次数 |
| “GitHub 有没有更好的方案？” | 先推导最低需求，再比较少量接近候选，判断直接复用、最小改造或确有必要才自建 |

## 核心流程

```text
真实痛点 → 基本事实 → 拿掉现成方案 → 最低需求 → 重建方案 → 最小验证
```

保持现状不是默认答案。Skill 会同时考虑行动价值、探索价值、机会成本、失败代价和可逆性：低成本选择直接给最小试验，高成本且难回退的选择才升级反方检验或双向钢人。

## 输出

任务或方案通常给出：真实目标、底层事实与约束、关键假设、当前判断和最小验证。候选方案比较和双向钢人只在实际触发时出现，不机械填满固定模板。

## 安装

```bash
npx skills add shilefumaoqu/suming-first-principles
npx skills add shilefumaoqu/suming-first-principles --list
python3 /path/to/validate_skill.py .
```

### 前置条件

- [ ] 使用支持 Agent Skills 的宿主。
- [ ] 通过上述命令安装时，已安装 Node.js 与 `npx`。
- [ ] 已理解本 Skill 默认只分析；外部搜索和实际执行仍受宿主权限与当前任务授权约束。

## 边界

- 普通教学使用 `$suming-learn-explain`。
- 模糊产品或 MVP 访谈使用 `$suming-product-discovery`。
- 今天是否做、是否偏离主线和优先级安排交给 `$suming`。
- 单纯搜索、摘要、翻译和路径已经明确的执行任务不调用本 Skill。
- 分析请求默认只读；用户已经授权实施时，主代理收敛判断后继续执行和验证。

## 已验证与尚未证明

已验证：包结构、显式触发边界、公开文档、发布流程和干净安装。

尚未证明：真实模型输出一定优于普通分析、所有 Agent Skills 宿主中的行为完全一致，以及长期使用带来的固定效率提升。

## Troubleshooting

| 问题 | 原因 | 解决 |
|---|---|---|
| 找不到 Skill | 安装目录或宿主扫描状态不一致 | 核对安装目录后刷新或重新打开宿主 |
| 没有自动调用 | 这是显式调用 Skill | 明确调用 `$suming-first-principles` 或要求使用第一性原理 |
| 回答总在劝退 | 只看到了风险，没有比较行动和探索价值 | 同时检查行动、探索、缩小试验与保持现状 |
| 搜索越来越长 | 没有执行候选停止条件 | 找到 1—3 个有效候选后停止 |
| 一直提问 | 没有在关键答案后收敛 | 每轮最多问一个会改变结论的问题，随后给出判断 |

## 致谢

Upstream inspiration: suming-meta-skill: reusable skill packaging, trigger boundaries, and evidence-bound validation

## License

MIT
