# SpikeMem system paper (大创结题稿)

This is the ACL 2027 writing workspace. Import the repository root into
Overleaf and keep `main.tex` as the main document. `Daily_report/` stores the
human/AI coordination notes and audit reports; it is intentionally kept in the
GitHub repository so the writing history remains reviewable.

Build: `pdflatex main && bibtex main && pdflatex main && pdflatex main` (ACL style, `[preprint]`).
Current build: 7 pages, 0 overfull boxes, 0 undefined references, 0 TODOs.

Every number in main.tex comes from the frozen evaluation artifacts that paper_numbers.json maps
(R0 replay_summary.json for Table 1; g7/g8/g10 summaries for §6 and the appendices;
phase7_entry_ppr_2417.json for PPR). No number from R1 (dense/BM25/recency RAG, iterative,
ablation switches, efficiency) is used, because R1 results were not delivered.

Claim rules:
1. The matched event queue is not a baseline, but the implementation note in §3 and the matching
   Limitations sentence stay.
2. Adding R1 baselines later: add columns to Table 1 and delete the Limitations sentence saying
   RAG/iterative memories are not included. Do not write "beats every baseline" unless all ten rows
   support it.
3. Table 3 is the read-out ablation (343-question slice); do not present it as full-dev.
