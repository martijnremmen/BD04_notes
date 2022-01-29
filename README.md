# Latex template voor studie Zuyd

## Requirements
 * `texlive` Voor het algemene pakket (pdflatex)
 * `texlive-lang-european` Voor de nederlandse taal (voor babel)
 * `texlive-bibtex-extra` Voor biblatex
 * `biber` Ook voor biblatex

## Compilen project

1. `pdflatex --shell-escape main.tex`
2. *Optioneel voor bibliografie* `biber main`
3. *Optioneel voor bibliografie* `pdflatex main`
