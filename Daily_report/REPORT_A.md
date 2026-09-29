# REPORT_A (2026-09-25, full-rerun-A-20260925)

## 0. 摘要

阶段 A 的新仓库、来源清单、独立环境、统一评分和追加式 reader 缓存已建立；41 题哈希抽样在 clean 与 FP=.3 完整跑通三种方法。

## 1. 环境、代码、模型和偏离

- 新仓库：`/202608/202608/haojiang/projects_spike/SpikeMem`，用户明确指定；HANDOFF 中的旧直接子路径已被覆盖。
- 四个旧目录已完整压缩并校验，备份与 SHA256 位于 `/202608/202608/haojiang/backup/`。
- Python 3.12.3、NumPy 1.26.4、Torch 2.8.0a0+5228986c39.nv25.6、CUDA 12.9、Transformers 4.57.1；见 `env/ENV.md`。
- 模型逐文件 SHA256 见 `env/model_weights.sha256`；源码逐文件来源见 `docs/PROVENANCE.md`（56 项）。
- 旧目录核实结果见 `docs/LEGACY_MAP.md`；冻结参数见 `docs/PARAMS.md`。
- 旧代码仅在新副本修改 package import、数据/输出路径，另为 METHOD §4 传递答案别名并新建评分和缓存层。源码差异逐项记录在 `docs/PROVENANCE.md`。
- 新数据构图、新 bge 向量和 Qwen 生成均独立完成；未读取旧冻结 reader 输出或旧 reader 缓存。

## 2. 结果

- E0：n=2417、事实数=11322、seed@1=0.685561；K=2/3/4 分别 1252/760/405；注入桥接槽位 1964，gold 较新写入比例 1.000。

| 设置 | 方法 | n 题 | 归一化 EM | 严格 EM | reader 逻辑调用 |
|---|---|---:|---:|---:|---:|
| clean | SpikeMem | 41 | 0.7561 | 0.7561 | 0 |
| clean | TKG_soft | 41 | 0.6707 | 0.6707 | 20 |
| clean | Dense_k8 | 41 | 0.2195 | 0.1585 | 82 |
| FP=.3 | SpikeMem | 41 | 0.6829 | 0.6829 | 6 |
| FP=.3 | TKG_soft | 41 | 0.6220 | 0.6220 | 18 |
| FP=.3 | Dense_k8 | 41 | 0.2195 | 0.1585 | 82 |

- reader：252 次逻辑调用，128 个独特 prompt 实际生成，124 次批内复用；全部实际生成使用 batch 8、左填充。

## 3. 闸门与核查

- 原代码 `src/spikemem/bench/common.py:82` 的 `Prediction.correct` 直接使用 `self.answer == q.answer`。原两链裁决在 `src/spikemem/experiments/g7_order_balanced.py:108-111` 对正序和反序分别做原始字符串相等判断；新 runner 统一调用 `src/spikemem/scoring.py`。
- 复制后的原方法测试和新评分测试共 23 项通过。
- E0 的 11,322 与 seed@1≈0.6856 均与 METHOD 预期相符。

## 4. 异常与可疑之处

- Dense_k8 的 41 题严格 EM 为 0.1585，归一化 EM 为 0.2195；确认两种评分不可混用。
- 首次缓存汇总漏计同一批次中的重复 prompt；已修正为 252=128+124，不影响生成输出与 EM。

## 5. 产物路径

- `results/E0/{config.json,per_query.jsonl,summary.json}`
- `results/smoke/{per_query.jsonl,summary.json}`
- `cache/reader/outputs.jsonl`（追加式；不纳入 Git）
- `docs/{LEGACY_MAP.md,PROVENANCE.md,PARAMS.md}` 和 `env/{ENV.md,requirements.lock,model_weights.sha256}`
