# Paper: Multi-Behaviour Evaluation of 30 Small Open LLMs

Build: `latexmk -pdf main.tex` (or pdflatex → bibtex → pdflatex ×2).

```
main.tex                  preamble, macros, section includes
references.bib            bibliography (entries marked VERIFY need checking)
sections/00_abstract.tex  … 10_appendix.tex
tables/                   30-row result tables (skeletons full of \TBD)
figures/                  put your plots here
```

## Filling in results
- `\TBD` marks every value still to be measured (it renders as a red **TBD**). Run `grep -rn '\\TBD' .` to list them.
- `\begin{observation}[...]` boxes in `sections/06_results.tex` are where you write observations. The grey guiding questions inside each box (`\questions{...}`) can be deleted once you've written your text.
- `\figplaceholder{...}` marks a planned figure. Replace it with `\includegraphics[width=\linewidth]{figures/<file>.pdf}`.
- `\guide{...}` is a grey writing note. Switch `\showguidancetrue` to `\showguidancefalse` in `main.tex` to hide all notes and questions for a clean build.

## Before submission
- Verify the model licences and GGUF sizes in Table 3 (`sections/03_models.tex`).
- Fix the two bib entries with `[Author list to verify]` (SyPS, Refusal–Compliance Tradeoff).
- Re-check the evidence map (Table 1) against new arXiv papers.
