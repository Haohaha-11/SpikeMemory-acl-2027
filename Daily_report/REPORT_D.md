没有基线在任何已运行设置上超过 SpikeMem（归一化 EM；E1 的 10 档及 E5/E6）。

# REPORT_D（2026-09-25，full-rerun-D-20260925）

## 0. 摘要

- E0–E12 已在新仓库独立完成；新 reader 缓存仅保存本轮重新生成的 Qwen3-8B 输出。
- 阶段 B 35 格严格 EM 对账 33/35 通过。失败格子：diag=.3 SpikeMem 偏差 0.002689；clean bm25_k8 偏差 0.005575。
- 用户确认在报告明确标注偏差后继续 E5–E12；本轮没有为追旧稿调参。

## 1. 环境、代码和偏离

- env/ENV.md、env/model_weights.sha256、docs/PROVENANCE.md、docs/PARAMS.md 记录环境、权重和代码来源。
- 服务器启动曾中断 RAG 推理；237,920 条已写入的逐题记录通过 JSON 校验后接续，缓存始终只追加。新进程调用数与缓存总条目分开记录。

## 2. 结果

- RESULTS.md 汇总 Table 1–4、Figure 2、附录 A–D、E10/E12；figures/fig3_rho_scan.pdf 已渲染并检查。
- 验证：E1 图方法 145,020 条逐题行，RAG 290,040 条，E3 21,753 条；E10 候选/输入/输出差异总计 0。
- results.json 给出 19,875 条新结果数字的实验、文件、JSON 指针、命令和样本量；paper_numbers.json 清点现稿 213 处数字，PAPER_DIFFERENCES.md 直接对比 74 处实验数字。

## 3. 闸门与核查

- diag=.3 SpikeMem 偏差来自 18 题 MD5 平局改变候选及 7 题相同 prompt 的新 reader 输出，详见 reports/E1_DIAG3_AUDIT.json 与 prompt 核对文件。
- clean BM25 k8 的 4,336/4,834 个输入候选因 MD5 平局变化，严格 EM 净增加 26/4,834；相同 prompt 的新 reader 输出净增加 1/4,834。详见 reports/E1_BM25_AUDIT.json。
- reports/VALIDATION.json 记录样本量、结果文件结构、有限数值和 E10 等价性校验。

## 4. 异常与可疑之处

- 现稿 paper/main.tex 未修改。E3 的 FP=.3 top-2 读出及 FN=.3 屏蔽/ top-2 相对 SpikeMem 的方向或平局发生变化；见 reports/PAPER_DIFFERENCES.md。
- E9 更新注入未触及的比例 0.3633、该子集文本入口准确率 0.6891，与旧稿 0.626 和 1.000 的口径/入口不同。原屏蔽式噪声恒等式脚本未找到。
- 旧 comparisons 注解从未自增，不作为效率计数；E4 使用实际边访问与每设置独立 CPU 计时。
- 现稿逐级能力分解除全图 soft 外没有在本轮 E0–E12 独立重跑；保留为历史说法，不能作为新证据。

## 5. 产物路径

- results/E0–E12/、RESULTS.md、results.json、paper_numbers.json、reports/REPORT_A.md–REPORT_D.md。
- figures/fig3_rho_scan.pdf；打包结果见 /202608/202608/haojiang/projects_spike/SpikeMem_results_2026-09-25.tgz。
- 四个旧文件夹的只读备份见 /202608/202608/haojiang/backup/SpikeMem_legacy_2026-09-25.tar.gz。
