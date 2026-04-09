# Felipe R. Terrazas — CV LaTeX Project

A version-controlled LaTeX workspace for maintaining multiple tailored CV variants. Each CV is written in LaTeX, auto-compiled via VS Code on save, and outputs a clean PDF to the `output/` folder — keeping source, build artifacts, and final PDFs neatly separated.

A companion static website (`web/`) is included to showcase the professional profile online.

---

## Repository Structure

```
cv/
├── src/          # LaTeX source files (.tex) — one file per CV variant
├── output/       # Final PDFs only — the only folder you ever share
├── build/        # Intermediate LaTeX artifacts (.aux, .log, .synctex.gz, etc.)
├── web/          # Static personal website (HTML/CSS/JS)
│   ├── index.html
│   ├── styles.css
│   └── script.js
├── .vscode/
│   └── settings.json   # LaTeX Workshop configuration
├── .gitignore
└── README.md
```

> `build/` is listed in `.gitignore` and is never committed. Only `src/` and `output/` are tracked in version control.

---

## Prerequisites

| Tool | Purpose |
|---|---|
| [TeX Live](https://www.tug.org/texlive/) or [MiKTeX](https://miktex.org/) | LaTeX compiler (`pdflatex`) |
| [VS Code](https://code.visualstudio.com/) | Editor |
| [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) (VS Code extension) | Auto-build, PDF preview, SyncTeX |

Install the LaTeX Workshop extension in VS Code:

```
ext install James-Yu.latex-workshop
```

---

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/FelipeRamiresTerrazas/cv.git
   cd cv
   ```

2. **Open the workspace in VS Code**

   ```bash
   code .
   ```

3. **Open any `.tex` file in `src/`**

   LaTeX Workshop will auto-build on save. The PDF will be written to `output/` and intermediate files will go to `build/`.

4. **Preview the PDF**

   After saving, click the PDF preview icon in the top-right of the VS Code editor (or press `Ctrl+Alt+V`).

---

## How the Build Works

The `.vscode/settings.json` configures a two-step recipe:

1. **`pdflatex`** — compiles the `.tex` file, writing all artifacts to `build/`
2. **`copy-pdf`** — copies only the resulting `.pdf` to `output/`

This means `output/` stays clean — just the final PDFs, ready to attach or share.

Build is triggered automatically on every save (`"latex-workshop.latex.autoBuild.run": "onSave"`).

---

## CV Variants (`src/`)

| File | Role / Target |
|---|---|
| `cv_felipe_terrazas_data_analyst.tex` | General Data Analyst role |
| `cv_analytics_eng_lead.tex` | Analytics Engineering Lead |
| `cv_felipe_terrazas_ey_bi_senior.tex` | Senior Data & BI Analyst — EY FSO |
| `cv_felipe_terrazas_product_ops_deliveryhero.tex` | Product Operations |
| `pooja_hiremath_data_qa_cv.tex` | Data QA CV (third-party) |
| `cv_template.tex` | Blank template for new variants |

### Creating a New CV Variant

1. Duplicate `cv_template.tex` inside `src/` and rename it (e.g. `cv_<name>_<role>.tex`).
2. Edit the content.
3. Save — the PDF will be auto-generated in `output/`.

---

## CV Submission Log

To avoid confusion between multiple CV versions, keep a single tracking file at:

- `output/cv_usage_log.md`

This log links each generated PDF to the role/company where it was used.

Suggested minimum fields per entry:

- Date
- Output PDF filename
- Source `.tex` filename (if available)
- Company
- Role / Job posting
- Notes

Example:

| Date | Output PDF | Source TEX | Company | Role | Notes |
|---|---|---|---|---|---|
| 2026-04-09 | `cv_felipe_terrazas_data_specialist.pdf` | N/A | Delivery Hero | Data Specialist | Custom version used for Delivery Hero application |

Update this file whenever you send a CV. This gives you one place to audit where each version was used.

---

## Website (`web/`)

A lightweight static personal website is included for showcasing the professional profile online.

| File | Purpose |
|---|---|
| `index.html` | Main page (About, Experience, Skills, Contact sections) |
| `styles.css` | Responsive styling |
| `script.js` | Navigation toggle and small UI helpers |

### Preview locally

Just open `web/index.html` in any browser — no server needed.

### Deploy to GitHub Pages

1. Go to the repository **Settings → Pages**.
2. Set **Source** to `main` branch, folder `/web`.
3. Save — GitHub will publish the site at `https://feliperamiresterrazas.github.io/cv/`.

---

## .gitignore

Build artifacts are excluded from version control:

```
*.aux  *.log  *.out  *.synctex.gz  *.toc  *.fdb_latexmk  *.fls
build/
```

Only `.tex` source files and final `.pdf` outputs are committed.

---

## Author

**Felipe Ramires Terrazas** — Senior Data & BI Analyst  
[LinkedIn](https://www.linkedin.com/in/felipe-ramires-terrazas/) · [Website](https://feliperamiresterrazas.github.io/professionalwebsite/) · [felipe.agro.terrazas@gmail.com](mailto:felipe.agro.terrazas@gmail.com)
