# ccr-latex

LaTeX template for [Computational Communication Research (CCR)](https://journal.computationalcommunication.org/), a peer-reviewed, open-access, community-owned journal publishing articles on computational methods in communication research, published by Amsterdam University Press and founded by the ICA Computational Methods Division.

Please see the [author guide](author_guide.md) for detailed instructions on how to prepare a manuscript for publication. 

## Using the template

### Overleaf (recommended)

1. [Download this repository as a ZIP](https://github.com/ccr-journal/ccr-latex/archive/refs/heads/main.zip)
2. In Overleaf, click **New Project → Upload Project** and select the downloaded ZIP
3. Open `main.tex` and begin editing

### Locally

```sh
git clone https://github.com/ccr-journal/ccr-latex.git
cd ccr-latex
latexmk -pdf main.tex
```

Requires a TeX Live distribution with `biblatex-apa`, `biber`, `erewhon`, and `noto`. The template defaults to `pdflatex`; use `latexmk -xelatex` instead if your manuscript contains non-Latin scripts (the class has an `\ifxetex` branch that loads `fontspec`, `unicode-math`, and `Erewhon-Math.otf`).

## Writing your article

- **`main.tex`** — preamble: title, authors, affiliations, abstract, keywords, bibliography, packages
- **`body.tex`** — article body (sections, figures, tables, citations)

### Anonymised peer review

CCR requires [anonymised manuscripts for peer review](https://journal.computationalcommunication.org/about/submissions). To produce an anonymised build — with author/affiliation info suppressed, line numbers enabled, and a draft watermark — use the `review` class option in `main.tex`:

```latex
\documentclass[review]{ccr}
```

Remove the option when preparing the final camera-ready version.

## Quarto authors

A parallel Quarto template lives at [ccr-journal/ccr-quarto](https://github.com/ccr-journal/ccr-quarto) and wraps the same `ccr.cls`. 


## Reporting issues

File template bugs and suggestions at [github.com/ccr-journal/ccr-latex/issues](https://github.com/ccr-journal/ccr-latex/issues), or contact the editorial team at <ccreditorialteam@gmail.com>.

## License

The template is dual-licensed:

- **Code** (`ccr.cls`) — [MIT License](./LICENSE)
- **Example content** (`main.tex`, `body.tex`, `bibliography.bib`, `aup_logo.pdf`) — [Creative Commons Attribution 4.0 International](./LICENSE)

Articles typeset with this template are released under CC BY 4.0 upon publication in CCR, independent of the template's own license terms.
