# Technical Context: Tools, Setup, and LaTeX Conventions

**Last Updated:** 2026-01-12

## Technology Stack

### LaTeX Environment
- **Template**: ACM `acmart` class version 1.90+ (already in repository)
- **Document Class**: `sigconf` (conference format)
- **Compiler**: pdflatex (standard for ACM submissions)
- **Bibliography**: BibTeX with ACM-Reference-Format.bst

### Required Files (Already Present)
- `acmart.cls` - ACM article template class
- `ACM-Reference-Format.bst` - ACM bibliography style
- `acmart.pdf` / `acmguide.pdf` - Template documentation
- `sample-*.tex` - ACM template examples

### File Organization
```
fose2026/
├── main.tex                 # Main document
├── sections/               # Section files
│   ├── 01_introduction.tex
│   ├── 02_background.tex
│   ├── 03_survey.tex
│   ├── 04_breakdown.tex
│   ├── 05_principles.tex
│   ├── 06_implications.tex
│   ├── 07_limitations.tex
│   └── 08_conclusion.tex
├── bibliography.bib        # Main references
├── software.bib           # Software/tool references
├── figures/               # Figures directory (create as needed)
├── data/                  # Survey data (XLSX, PPTX)
└── acmart.cls            # ACM template
```

## Development Environment Setup

### LaTeX Distribution
- **macOS**: MacTeX (full TeX Live distribution)
- **Verification**: `pdflatex --version`
- **Package Manager**: tlmgr for TeX Live packages

### Recommended Editors
- **VS Code** with LaTeX Workshop extension (already in use)
- **Overleaf** for collaborative editing (if needed)
- **TeXShop** (macOS native)

### Build System
```bash
# Standard build
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex

# Or use latexmk for automated builds
latexmk -pdf main.tex
```

### VS Code LaTeX Workshop Configuration
```json
{
  "latex-workshop.latex.recipes": [
    {
      "name": "pdflatex → bibtex → pdflatex × 2",
      "tools": ["pdflatex", "bibtex", "pdflatex", "pdflatex"]
    }
  ]
}
```

## ACM Template Configuration

### Document Class Options
```latex
\documentclass[sigconf, anonymous, review]{acmart}
```

**Options:**
- `sigconf` - Conference format
- `anonymous` - Anonymous submission (hides author info)
- `review` - Review mode (line numbers, etc.)

### Required Preamble Elements
```latex
% Copyright block (deferred until acceptance)
\setcopyright{none}

% CCS Concepts (add before submission)
\begin{CCSXML}
<ccs2012>
...
</ccs2012>
\end{CCSXML}
\ccsdesc[500]{Software and its engineering~Software creation and management}

% Keywords
\keywords{knowledge accumulation, research artifacts, software engineering}
```

## Code Patterns and Conventions

### Section Include Pattern
```latex
% main.tex
\begin{document}
\maketitle

\input{sections/01_introduction}
\input{sections/02_background}
\input{sections/03_survey}
\input{sections/04_breakdown}
\input{sections/05_principles}
\input{sections/06_implications}
\input{sections/07_limitations}
\input{sections/08_conclusion}

\bibliographystyle{ACM-Reference-Format}
\bibliography{bibliography,software}
\end{document}
```

### Figure Pattern
```latex
\begin{figure}[t]
  \centering
  \includegraphics[width=\columnwidth]{figures/survey-demographics}
  \caption{FOSE pre-survey respondent demographics showing high experience levels and productivity.}
  \label{fig:survey-demographics}
\end{figure}
```

### Table Pattern
```latex
\begin{table}[t]
  \caption{Survey respondent characteristics}
  \label{tab:survey-stats}
  \begin{tabular}{lrr}
    \toprule
    Characteristic & Count & Percentage \\
    \midrule
    10+ years experience & XX & XX\% \\
    Multiple submissions & XX & XX\% \\
    Global distribution & XX & XX\% \\
    \bottomrule
  \end{tabular}
\end{table}
```

### Citation Patterns
```latex
% Inline citation
\citet{author2024} argue that...

% Parenthetical citation
Knowledge graphs have been applied to science \citep{author2024, other2023}.

% Multiple citations
Several efforts address this \citep{author1, author2, author3}.
```

### Section Structure Pattern
```latex
\section{Section Title}
\label{sec:section-label}

Opening paragraph establishing section purpose...

\subsection{Subsection Title}
\label{sec:subsection-label}

Content with proper paragraph structure...
```

## Bibliography Management

### BibTeX Entry Patterns

**Conference Paper:**
```bibtex
@inproceedings{key2024,
  author = {Author, First and Author, Second},
  title = {Paper Title},
  booktitle = {Proceedings of the Conference},
  year = {2024},
  pages = {1--10},
  doi = {10.1145/xxxxx}
}
```

**Journal Article:**
```bibtex
@article{key2024,
  author = {Author, First},
  title = {Article Title},
  journal = {Journal Name},
  volume = {42},
  number = {3},
  pages = {100--120},
  year = {2024},
  doi = {10.xxxx/yyyy}
}
```

**Tool/Software:**
```bibtex
@misc{tool2024,
  author = {Developer, Name},
  title = {Tool Name},
  howpublished = {\url{https://example.com}},
  year = {2024},
  note = {Accessed: 2024-01-12}
}
```

### Bibliography Organization
- `bibliography.bib` - Academic papers and main references
- `software.bib` - Tools, platforms, and software systems
- Both included via `\bibliography{bibliography,software}`

## Common Issues and Debugging

### Compilation Errors

**Missing references:**
- **Symptom**: "??" in place of citations or figures
- **Solution**: Run bibtex, then pdflatex twice more

**Undefined control sequence:**
- **Symptom**: `! Undefined control sequence`
- **Solution**: Check for typos in LaTeX commands, ensure packages loaded

**Figure/table placement:**
- **Symptom**: Figures appear far from reference point
- **Solution**: Use placement specifiers `[t]` (top), `[h]` (here), `[b]` (bottom)
- **Note**: LaTeX optimizes placement; use `\FloatBarrier` if needed

**Bibliography not appearing:**
- **Symptom**: Empty bibliography or missing entries
- **Solution**: Ensure bibtex step run, check .bib file syntax

### ACM Template Issues

**Anonymous submission:**
- Ensure `anonymous` option in `\documentclass`
- Check that `\author{}` blocks don't leak info

**CCS concepts:**
- Use ACM Computing Classification Tool: https://dl.acm.org/ccs
- Generate XML, paste into preamble

**Rights management:**
- For initial submission: `\setcopyright{none}`
- Update after acceptance per ACM instructions

### Build Automation

**Using latexmk:**
```bash
# Clean build
latexmk -pdf -interaction=nonstopmode main.tex

# Continuous preview
latexmk -pdf -pvc main.tex

# Clean auxiliary files
latexmk -c
```

## Survey Data Processing

### Data Files
- `icse_2026_fose_pre-survey_completed_raw_data.xlsx` - Raw survey responses
- `icse_2026_fose_pre-survey_basic_data.pptx` - Summary slides

### Analysis Tools
- **Excel/Numbers**: For basic descriptive statistics
- **Python/Pandas**: For more complex analysis (if needed)
- **R**: Alternative for statistical analysis

### Data Extraction Pattern
1. Open XLSX in spreadsheet software
2. Extract demographic summaries (experience, productivity, location)
3. Identify representative quotes (if IRB-approved and anonymized)
4. Create summary tables or figures
5. Document statistics in Section 3

### Data Privacy
- Ensure survey data usage complies with IRB/ethics approval
- Anonymize any quotes or examples
- Report only aggregate statistics unless consent obtained

## Version Control

### Git Workflow
```bash
# Create feature branch for sections
git checkout -b draft/section-03-survey

# Commit regularly with descriptive messages
git commit -m "Draft survey synthesis section"

# Merge to master when section complete
git checkout master
git merge draft/section-03-survey
```

### .gitignore Recommendations
```
# LaTeX auxiliary files
*.aux
*.log
*.out
*.toc
*.bbl
*.blg
*.synctex.gz
*.fdb_latexmk
*.fls

# macOS
.DS_Store

# Editor
.vscode/
*.swp
```

## Submission Checklist

### Pre-Submission Validation
- [ ] Compiles without errors: `pdflatex main.tex`
- [ ] Bibliography complete: All citations resolved
- [ ] Figures/tables numbered and captioned
- [ ] CCS concepts added
- [ ] Anonymous submission verified
- [ ] Within page limits (check conference CFP)
- [ ] PDF/A compliance (if required)

### Submission Package
- [ ] `main.pdf` - Final compiled PDF
- [ ] `main.tex` and `sections/*.tex` - LaTeX sources
- [ ] `bibliography.bib`, `software.bib` - Bibliography files
- [ ] `figures/*` - All figures
- [ ] `acmart.cls` and support files

## Resources and Documentation

### ACM Template
- **Documentation**: `acmguide.pdf` (in repository)
- **Online Guide**: https://www.acm.org/publications/proceedings-template
- **CCS Tool**: https://dl.acm.org/ccs

### LaTeX References
- **Overleaf Guides**: https://www.overleaf.com/learn
- **CTAN**: https://ctan.org (package documentation)
- **TeX StackExchange**: https://tex.stackexchange.com

### Conference Information
- **ICSE 2026**: Check conference website for CFP and deadlines
- **FOSE Track**: Specific requirements and evaluation criteria

---

**Remember:** Keep builds clean and frequent, commit regularly, and validate formatting early to avoid last-minute issues.
