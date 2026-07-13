# Uploading this to Overleaf

## Fastest route (recommended)
1. Zip the whole `Project Report` folder (so it contains `main.tex`, `references.bib`, and the `sections/` folder).
2. In Overleaf: **New Project → Upload Project** → drop the zip.
3. Overleaf creates the project already populated. Set the compiler to **pdfLaTeX** (Menu → Settings) — it's the default, so usually nothing to change.
4. Hit **Recompile**. You should get a titled PDF with all sections as headings and TODO placeholders inside.

## Folder structure
```
Project Report/
├── main.tex              # document class, title, abstract, \input order, bibliography
├── references.bib        # add citations here (paste BibTeX from Scholar/arXiv/ACL)
└── sections/
    ├── 01_introduction.tex
    ├── 02_background.tex
    ├── 03_system.tex
    ├── 04_implementation.tex
    ├── 05_evaluation.tex
    ├── 06_discussion.tex
    └── 07_conclusion.tex
```

## How to work in it
- Each section is its own file — edit them independently, they get pulled into `main.tex` via `\input{}`.
- Every section has commented notes (`%`) explaining what goes there, plus `TODO` markers where prose is needed. Search "TODO" to find every open spot.
- Write the **abstract last** (noted in `main.tex`).

## Retargeting later (arXiv / workshop / conference)
When you pick a venue, usually you only swap the `\documentclass{...}` line in `main.tex` for the venue's template class and adjust a couple of packages. The `sections/` content carries over unchanged. Ping me when you know the venue and I'll do the conversion.

## Syncing edits back to this folder
If you later want me editing alongside you, the clean path is Overleaf's **Git** integration (paid Overleaf plan): clone the project into this folder, I edit here, you push/pull. For now the upload route above is one-way (here → Overleaf).
