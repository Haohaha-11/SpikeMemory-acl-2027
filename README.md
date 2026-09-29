# SpikeMem system paper (大创结题稿)

Build: `pdflatex main && bibtex main && pdflatex main && pdflatex main` (ACL style, `[preprint]`).
Current build: 9 pages, 0 overfull boxes, 0 undefined references, 0 TODOs.

All numbers come from the full from-scratch rerun in the SpikeMem repository (commit 8564d84;
RESULTS.md, results/E0-E12; normalized EM for every method). Figures 2 and 3 were redrawn from E5 and
E7. The self-check in Appendix B was computed from results/E0 and results/E1 per-query files.

Claim rules:
1. The matched event queue is not a baseline, but the implementation note in §3 and the matching
   Limitations sentence stay.
2. "Most accurate in every setting" is supported by all ten rows of Table 1 (normalized EM).
3. Table 4 is the read-out intervention on a 343-question slice with historical entry; do not present
   it as full-dev.
