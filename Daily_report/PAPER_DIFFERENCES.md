# 现稿与重跑差异

主指标是归一化 EM；严格 EM 用于旧稿对账。paper/main.tex 未修改。

| 来源 | 数字 | 旧值 | 新严格 EM | 新归一化 EM | 四位一致 | 新证据 |
|---|---|---:|---:|---:|---|---|
| Table 1 | clean SpikeMem | 0.6856 | 0.6856 | 0.6856 | True | results/E1/graph_summary.json |
| Table 1 | clean TKG_hard | 0.6856 | 0.6856 | 0.6856 | True | results/E1/graph_summary.json |
| Table 1 | clean TKG_soft | 0.6243 | 0.6241 | 0.6241 | False | results/E1/graph_summary.json |
| Table 1 delta | clean SpikeMem minus TKG_hard | 0.0000 | 0.0000 | 0.0000 | True | results/E1/graph_summary.json |
| Table 1 delta | clean SpikeMem minus TKG_soft | 0.0612 | 0.0614 | 0.0614 | False | results/E1/graph_summary.json |
| Table 1 | FP=.1 SpikeMem | 0.6756 | 0.6754 | 0.6754 | False | results/E1/graph_summary.json |
| Table 1 | FP=.1 TKG_hard | 0.6347 | 0.6347 | 0.6347 | True | results/E1/graph_summary.json |
| Table 1 | FP=.1 TKG_soft | 0.6055 | 0.6059 | 0.6059 | False | results/E1/graph_summary.json |
| Table 1 delta | FP=.1 SpikeMem minus TKG_hard | 0.0410 | 0.0408 | 0.0408 | False | results/E1/graph_summary.json |
| Table 1 delta | FP=.1 SpikeMem minus TKG_soft | 0.0701 | 0.0695 | 0.0695 | False | results/E1/graph_summary.json |
| Table 1 | FP=.2 SpikeMem | 0.6663 | 0.6659 | 0.6659 | False | results/E1/graph_summary.json |
| Table 1 | FP=.2 TKG_hard | 0.5925 | 0.5925 | 0.5925 | True | results/E1/graph_summary.json |
| Table 1 | FP=.2 TKG_soft | 0.5904 | 0.5910 | 0.5910 | False | results/E1/graph_summary.json |
| Table 1 delta | FP=.2 SpikeMem minus TKG_hard | 0.0739 | 0.0734 | 0.0734 | False | results/E1/graph_summary.json |
| Table 1 delta | FP=.2 SpikeMem minus TKG_soft | 0.0759 | 0.0749 | 0.0749 | False | results/E1/graph_summary.json |
| Table 1 | FP=.3 SpikeMem | 0.6566 | 0.6558 | 0.6558 | False | results/E1/graph_summary.json |
| Table 1 | FP=.3 TKG_hard | 0.5445 | 0.5445 | 0.5445 | True | results/E1/graph_summary.json |
| Table 1 | FP=.3 TKG_soft | 0.5770 | 0.5772 | 0.5772 | False | results/E1/graph_summary.json |
| Table 1 delta | FP=.3 SpikeMem minus TKG_hard | 0.1121 | 0.1113 | 0.1113 | False | results/E1/graph_summary.json |
| Table 1 delta | FP=.3 SpikeMem minus TKG_soft | 0.0796 | 0.0786 | 0.0786 | False | results/E1/graph_summary.json |
| Table 1 | FN=.1 SpikeMem | 0.6769 | 0.6767 | 0.6767 | False | results/E1/graph_summary.json |
| Table 1 | FN=.1 TKG_hard | 0.6756 | 0.6754 | 0.6754 | False | results/E1/graph_summary.json |
| Table 1 | FN=.1 TKG_soft | 0.6229 | 0.6227 | 0.6227 | False | results/E1/graph_summary.json |
| Table 1 delta | FN=.1 SpikeMem minus TKG_hard | 0.0012 | 0.0012 | 0.0012 | True | results/E1/graph_summary.json |
| Table 1 delta | FN=.1 SpikeMem minus TKG_soft | 0.0540 | 0.0540 | 0.0540 | True | results/E1/graph_summary.json |
| Table 1 | FN=.2 SpikeMem | 0.6709 | 0.6703 | 0.6703 | False | results/E1/graph_summary.json |
| Table 1 | FN=.2 TKG_hard | 0.6663 | 0.6659 | 0.6659 | False | results/E1/graph_summary.json |
| Table 1 | FN=.2 TKG_soft | 0.6202 | 0.6200 | 0.6200 | False | results/E1/graph_summary.json |
| Table 1 delta | FN=.2 SpikeMem minus TKG_hard | 0.0046 | 0.0043 | 0.0043 | False | results/E1/graph_summary.json |
| Table 1 delta | FN=.2 SpikeMem minus TKG_soft | 0.0507 | 0.0503 | 0.0503 | False | results/E1/graph_summary.json |
| Table 1 | FN=.3 SpikeMem | 0.6651 | 0.6640 | 0.6640 | False | results/E1/graph_summary.json |
| Table 1 | FN=.3 TKG_hard | 0.6566 | 0.6558 | 0.6558 | False | results/E1/graph_summary.json |
| Table 1 | FN=.3 TKG_soft | 0.6171 | 0.6167 | 0.6167 | False | results/E1/graph_summary.json |
| Table 1 delta | FN=.3 SpikeMem minus TKG_hard | 0.0085 | 0.0083 | 0.0083 | False | results/E1/graph_summary.json |
| Table 1 delta | FN=.3 SpikeMem minus TKG_soft | 0.0480 | 0.0474 | 0.0474 | False | results/E1/graph_summary.json |
| Table 1 | diag=.1 SpikeMem | 0.6696 | 0.6680 | 0.6680 | False | results/E1/graph_summary.json |
| Table 1 | diag=.1 TKG_hard | 0.6309 | 0.6307 | 0.6307 | False | results/E1/graph_summary.json |
| Table 1 | diag=.1 TKG_soft | 0.6057 | 0.6057 | 0.6057 | True | results/E1/graph_summary.json |
| Table 1 delta | diag=.1 SpikeMem minus TKG_hard | 0.0387 | 0.0372 | 0.0372 | False | results/E1/graph_summary.json |
| Table 1 delta | diag=.1 SpikeMem minus TKG_soft | 0.0639 | 0.0623 | 0.0623 | False | results/E1/graph_summary.json |
| Table 1 | diag=.2 SpikeMem | 0.6560 | 0.6541 | 0.6541 | False | results/E1/graph_summary.json |
| Table 1 | diag=.2 TKG_hard | 0.5662 | 0.5658 | 0.5658 | False | results/E1/graph_summary.json |
| Table 1 | diag=.2 TKG_soft | 0.5896 | 0.5890 | 0.5890 | False | results/E1/graph_summary.json |
| Table 1 delta | diag=.2 SpikeMem minus TKG_hard | 0.0898 | 0.0883 | 0.0883 | False | results/E1/graph_summary.json |
| Table 1 delta | diag=.2 SpikeMem minus TKG_soft | 0.0664 | 0.0652 | 0.0652 | False | results/E1/graph_summary.json |
| Table 1 | diag=.3 SpikeMem | 0.6380 | 0.6353 | 0.6353 | False | results/E1/graph_summary.json |
| Table 1 | diag=.3 TKG_hard | 0.5002 | 0.4996 | 0.4996 | False | results/E1/graph_summary.json |
| Table 1 | diag=.3 TKG_soft | 0.5577 | 0.5573 | 0.5573 | False | results/E1/graph_summary.json |
| Table 1 delta | diag=.3 SpikeMem minus TKG_hard | 0.1378 | 0.1357 | 0.1357 | False | results/E1/graph_summary.json |
| Table 1 delta | diag=.3 SpikeMem minus TKG_soft | 0.0803 | 0.0780 | 0.0780 | False | results/E1/graph_summary.json |
| METHOD RAG | dense k8 clean | 0.2503 | 0.2501 | 0.2633 | False | results/E1/rag_summary.json |
| METHOD RAG | bm25 k8 clean | 0.2286 | 0.2342 | 0.2472 | False | results/E1/rag_summary.json |
| METHOD RAG | recency_dedup k8 clean | 0.2913 | 0.2923 | 0.3070 | False | results/E1/rag_summary.json |
| METHOD baseline | Iterative clean | 0.2503 | 0.2503 | 0.2503 | True | results/E1/graph_summary.json |
| METHOD baseline | PPR clean | 0.0074 | 0.0087 | 0.0190 | False | results/E1/graph_summary.json |
| METHOD E3 | clean no_arbitration | 0.2503 | 0.2503 | 0.2503 | True | results/E3/summary.json |
| METHOD E3 | FP=.3 no_arbitration | 0.2503 | 0.2503 | 0.2503 | True | results/E3/summary.json |
| METHOD E3 | FN=.3 no_arbitration | 0.2503 | 0.2503 | 0.2503 | True | results/E3/summary.json |
| METHOD E3 | clean hard_masking | 0.6856 | 0.6856 | 0.6856 | True | results/E3/summary.json |
| METHOD E3 | FP=.3 hard_masking | 0.5445 | 0.5445 | 0.5445 | True | results/E3/summary.json |
| METHOD E3 | FN=.3 hard_masking | 0.6645 | 0.6640 | 0.6640 | False | results/E3/summary.json |
| METHOD E3 | clean top2_readout | 0.6856 | 0.6856 | 0.6856 | True | results/E3/summary.json |
| METHOD E3 | FP=.3 top2_readout | 0.6560 | 0.6558 | 0.6558 | False | results/E3/summary.json |
| METHOD E3 | FN=.3 top2_readout | 0.6645 | 0.6640 | 0.6640 | False | results/E3/summary.json |
| E6 historical FP=.3 | SpikeMem EM | 0.9537 | 0.9519 | 0.9519 | False | results/E6/summary.json |
| E6 historical FP=.3 | TKG_soft_full EM | 0.9012 | 0.8988 | 0.8988 | False | results/E6/summary.json |
| E6 Table 4 | singleton EM | 1.0000 | 1.0000 | 1.0000 | True | results/E6/summary.json |
| E6 Table 4 | same_answer_pair EM | 1.0000 | 1.0000 | 1.0000 | True | results/E6/summary.json |
| E6 Table 4 | original_distractor_pair EM | 0.8776 | 0.8761 | 0.8761 | False | results/E6/summary.json |
| E6 Table 4 | attractive_wrong_pair EM | 0.8673 | 0.8630 | 0.8630 | False | results/E6/summary.json |
| Figure 2 caption | 0.0 seed@1 | 0.7225 | 0.7225 | 0.7225 | True | results/E5/summary.json |
| Figure 2 caption | 0.75 seed@1 | 0.7000 | 0.7000 | 0.7000 | True | results/E5/summary.json |
| E7 paper narrative | two-chain decisions | 14292.0000 | 14293.0000 | 14293.0000 | False | results/E7/summary.json |
| E7 paper narrative | order flips | 4314.0000 | 4365.0000 | 4365.0000 | False | results/E7/summary.json |

## 结论方向或平局改变

- FP=.3 top2_readout
- FN=.3 hard_masking
- FN=.3 top2_readout

## 不可直接对比的历史数字

- E7 的旧裁决数混合多种入口；本轮只统计 E1 文本入口，口径不同。
- 论文逐级能力分解仅全图 soft 对应本轮 E6；其余三段没有在 E0–E12 中独立重跑。
- 旧 PPR edge relaxations 与本轮 E4 的实测边访问计数口径不同。
- E9 原屏蔽式噪声恒等式脚本若未找到，旧预测/实测值不作为新证据。
