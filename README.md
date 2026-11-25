# OSPAIC LaTeX Template

A LaTeX template for papers submitted to **Oxford Studies in Philosophy of AI
and Computing** (OSPAIC). 

This template is an independent file for authors preparing a submission. It is
not affiliated with OSPAIC, its editors, or Oxford University Press. Check the
call for papers for the official requirements.

## Files
| File | Purpose |
| --- | --- |
| `main.tex` | The manuscript template. |
| `references.bib` | Example bibliography (biblatex `authoryear`, Biber). |
| `orcid.pdf` | ORCID iD mark used in the author block. |
| `main.pdf` | Compiled preview of the example text. |
| `LICENSE` | CC0 1.0. |

## Building
```sh
latexmk -pdf main.tex     # build (runs pdflatex and biber as needed)
latexmk -c                # remove build artefacts
```

Requires a recent TeX Live (2023 or later; tested with 2026) or Overleaf.
Preamble packages: `newtxtext`/`newtxmath`, `biblatex` + `biber`, `csquotes`,
`cleveref`, `booktabs`, `graphicx` (all in a standard full installation).

References use biblatex's author–date style, adjusted to Harvard form:
`(1950) 'Title'. Journal, 59(236), pp. 433–460.` Cite with `\textcite{key}` in
the sentence or `\parencite{key}` in brackets, and print the list with
`\printbibliography`. Harvard has several variants; the adjustments are the
commented lines at the top of the preamble.

## Blind review
Submissions are blind reviewed. Set the switch at the top of `main.tex`:

```latex
\blindreviewtrue    % anonymous version: no author block, no PDF author
\blindreviewfalse   % named version, for a preprint or the camera-ready
```

The anonymous version prints a discreet line where the author block would be.

## What the example text shows
Delete the example content and replace it with your paper. The examples cover
the basic elements common to a philosophy paper:

- a display quotation with a source;
- sections and subsections, with `lipsum` filler;
- a figure and a `booktabs` table;
- numbered propositions, with and without a title;
- definitions of two kinds: a concept (`Consciousness`) and a formal notion
  (`Realisation`), in a distinct style;
- a footnote, `cleveref` cross-references, and author–date citations;
- a display equation;
- the reference list.

Typography: Times (New TX), 12 pt, one-inch margins. `babel` is set to
`american`; change the option to `british` if you prefer.

## License
CC0 1.0 Universal: public domain dedication. Use it, change it, redistribute it,
commercially or otherwise, with no permission and no credit required. See
`LICENSE`. The ORCID iD mark in `orcid.pdf` is ORCID's own asset and remains
subject to ORCID's brand guidelines.

---
<https://ospaic.org/call-for-papers/> · <https://ospaic.org/policies/>
