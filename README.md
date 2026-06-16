# Fabric Smart Warehouse — Documentation

LaTeX sources for the technical report and the presentation of the **Fabric Smart Warehouse** project, developed for the *Cloud Native Applications* course (MSc), Harokopio University of Athens.

This repository contains only the documentation (LaTeX). The application source code lives in a separate repository.

## Links

- **Application source code:** https://github.com/drososkats/fabric-smart-warehouse
- **Report (PDF):** [`report/report.pdf`](report/report.pdf)
- **Presentation (PDF):** [`presentation/presentation.pdf`](presentation/presentation.pdf)

> The PDFs are generated from the LaTeX sources below. See **Building** for compiler details.

## Repository structure

```
.
├── report/                 # Technical design document
│   ├── report.tex          # Main document  (compile with pdfLaTeX)
│   ├── commands.tex        # Custom macros and shared commands
│   ├── chapters/           # Report chapters (\input from report.tex)
│   ├── figures/            # Images and diagrams
│   └── bib/                # Bibliography (.bib references)
│
└── presentation/           # Εxam presentation (Beamer)
    ├── presentation.tex    # Main document  (compile with XeLaTeX)
    ├── custom.tex          # Theme, colors and custom commands
    ├── chapters/           # Presentation sections
    ├── figures/            # Images and diagrams
    └── bib/                # Bibliography (.bib references)
```

## Building

This project can be edited and compiled either on **Overleaf** or **locally**, and is kept in sync through the Overleaf ↔ GitHub integration.

| Document | Main file | Compiler |
|---|---|---|
| Report | `report/report.tex` | pdfLaTeX |
| Presentation | `presentation/presentation.tex` | XeLaTeX |

**On Overleaf**
1. Open the project.
2. From *Menu*, set the **Main document** to the file you want to build.
3. Set the matching **Compiler** (pdfLaTeX for the report, XeLaTeX for the presentation).
4. Recompile.

**Locally** (TeX Live / MiKTeX installed)

```bash
# Report
cd report
pdflatex report.tex && biber report && pdflatex report.tex && pdflatex report.tex

# Presentation
cd presentation
xelatex presentation.tex && biber presentation && xelatex presentation.tex && xelatex presentation.tex
```

## Sync workflow (Overleaf ↔ GitHub ↔ local)

This repository is linked to an Overleaf project. To avoid merge conflicts, follow one simple rule: **work on one side at a time**, and sync before switching.

- **Overleaf:** *Menu → GitHub → Pull* before editing, *Push* when done.
- **Local / VS Code:** `git pull` before editing, then `git add . && git commit && git push` when done.

## Course

- **Course:** Cloud Native Applications (Spring 2026)
- **Institution:** Harokopio University of Athens — Dept. of Informatics and Telematics
- **Author:** Drosos Katsigarakis — `ais25123`
