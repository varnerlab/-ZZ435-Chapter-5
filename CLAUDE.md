# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a LaTeX manuscript for a NeurIPS 2026 submission (currently set to `preprint` mode). The paper presents a computational framework for multistep metabolic pathway design using deep learning-based retrobiosynthesis. Authors: Peter Zhiping Zhang and Jeffrey D. Varner (Cornell University). The content originates from Chapter 5 of P.Z.'s Ph.D. thesis.

## Build Commands

Compile the manuscript (requires LaTeX distribution with `minted` package support):
```bash
cd paper && pdflatex -shell-escape chapter5.tex && bibtex chapter5 && pdflatex -shell-escape chapter5.tex && pdflatex -shell-escape chapter5.tex
```

The `-shell-escape` flag is required because the paper uses the `minted` package for code highlighting (which calls Pygments externally).

## Repository Structure

- `paper/chapter5.tex` — Main manuscript source
- `paper/Reference.bib` — BibTeX bibliography
- `paper/neurips_2026.sty` — NeurIPS 2026 style file
- `paper/checklist.tex` — NeurIPS paper checklist (included from main tex)
- `paper/blank_template.tex` — Clean NeurIPS template for reference
- `paper/Figures/RouteDesign/` — All figures (PDF/PNG), covering neural network architectures, retrosynthesis workflows, pathway diagrams, and ML performance plots

## Key LaTeX Details

- Style: `neurips_2026` package, currently using `[preprint]` option. Switch to `[main, final]` for camera-ready.
- Notable packages: `minted` (code blocks, requires Pygments), `algorithm`/`algpseudocode` (pseudocode), `amsmath`, `booktabs`, `graphicx`
- Bibliography: `plain` style via `natbib` (loaded by neurips style)
