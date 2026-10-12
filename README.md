# Short Cycle Bases - revised thesis talk

48 slides: 44 main slides plus 4 technical Appendix slides. The revision makes the main question and the three proof mechanisms understandable with only this presentation, while keeping the actual theorems and adapted TikZ figures from the thesis.

## Overleaf

1. Upload the entire ZIP archive as a new Overleaf project.
2. Set **Main file** to `main.tex` and **Compiler** to **XeLaTeX**.
3. Recompile. All figures are included as TikZ source; no external image dependencies.

## Files

- `main.tex` - all presentation content in Beamer.
- `figures/diagrams.tex` - editable gadgets, witness/leaf configurations, lifts, folding, and MST figures.
- `figures/spiral_frames.tex` - six exact editable diagrams of the 16x16 double-spiral construction.
- `REVIEW_NOTES.md` - standalone comprehension test, proof-theme summary, and figure-validation results.
- `latexmkrc` - configuration for XeLaTeX.

The source is in English; the full thesis serves as the reference for longer proofs. Rendered PDF and an optional image-based PowerPoint version are supplied separately.
