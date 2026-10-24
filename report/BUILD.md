# Build the LaTeX report

In Overleaf, choose New Project → Upload Project, upload the repository ZIP, select `report/main.tex` as the main document, and use pdfLaTeX. Include any retained outer folder in the main-document path.

Alternatively, upload only `main.tex` and its `figures/` folder from this directory. No TRNSYS files are needed for typesetting.

For local TeX Live or MiKTeX, open a terminal in this folder and run `pdflatex -interaction=nonstopmode -halt-on-error main.tex` twice. The second pass updates the contents and bookmarks. All packages and Latin Modern fonts are standard; no custom fonts, `.bib`, `.cls`, or `.sty` files are required.

The compiled PDF includes the historical report and a separate editorial appendix. Compiling it does not execute the simulation.
