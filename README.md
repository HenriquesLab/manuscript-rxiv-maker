# Rxiv-Maker: Official Paper & Comprehensive Example

> 📚 **Dual Purpose Repository**: This repository serves two important roles:
> 1. **Official Published Paper & Preprint** - Published in *Journal of Cell Science* ([10.1242/jcs.265183](https://doi.org/10.1242/jcs.265183)), preprint at [arXiv:2508.00836](https://arxiv.org/abs/2508.00836)
> 2. **Comprehensive Working Example** - A complete demonstration of all rxiv-maker features
>
> Clone it instantly with: `rxiv get-rxiv-preprint`

This repository contains the source code for the official rxiv-maker paper, published in *Journal of Cell Science* (DOI: [10.1242/jcs.265183](https://doi.org/10.1242/jcs.265183)) and deposited as preprint [arXiv:2508.00836](https://arxiv.org/abs/2508.00836). This preprint both explains what rxiv-maker is and serves as an extensive demonstration of how scientific preprints can be written using [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker), a framework for writing scientific manuscripts in Markdown with automated figure generation.

## 📑 Quick Navigation

- [What's Inside](#-whats-inside) - Demonstrations and features
- [Getting Started](#-getting-started) - Prerequisites and building
- [Repository Structure](#-repository-structure) - File organization
- [Live Figure Generation](#-live-figure-generation) - Dynamic data features
- [Citation Features](#-citation-features) - Citation styles and DOI resolution
- [Ecosystem](#-rxiv-maker-ecosystem) - Related repositories
- [Citation](#-citation) - How to cite

<details>
<summary><b>🔍 Learning Paths</b> (click to expand)</summary>

**New to rxiv-maker?**
1. Start with [rxiv-maker Installation](https://github.com/HenriquesLab/rxiv-maker#installation)
2. Read the [Getting Started Guide](https://rxiv-maker.henriqueslab.org/getting-started/first-manuscript/)
3. Clone this repository: `rxiv get-rxiv-preprint`
4. Build the PDF: `rxiv pdf MANUSCRIPT/`
5. Explore the source files to see how features work

**Want to learn specific features?**
- **Figures**: Check `MANUSCRIPT/FIGURES/` for Python/R examples
- **Citations**: See `01_MAIN.md` for citation syntax examples
- **Data Integration**: Look at `{{py:exec}}` blocks in `01_MAIN.md`
- **Configuration**: Study `00_CONFIG.yml` for metadata setup

</details>

## 📚 What's Inside

This preprint demonstrates rxiv-maker's capabilities while documenting the framework itself:

| Feature | Location | Example |
|---------|----------|---------|
| **Self-documenting preprint** | `01_MAIN.md` | Explains rxiv-maker while using it |
| **Live data integration** | `{{py:exec}}` blocks | Current arXiv statistics |
| **Automated figures** | `FIGURES/*.py` | Publication-ready plots from data |
| **Supplementary info** | `02_SUPPLEMENTARY_INFO.md` | Additional technical details |
| **Configuration** | `00_CONFIG.yml` | Metadata and settings |
| **Analysis modules** | `src/py/` | Reusable data processing code |
| **Bibliography** | `03_REFERENCES.bib` | BibTeX references |

<details>
<summary><b>📖 Learning by Example - What Each File Teaches</b></summary>

**Core Manuscript Files:**
- `00_CONFIG.yml` - Learn: Metadata, author configuration, citation styles
- `01_MAIN.md` - Learn: Scientific markdown, cross-references, Python integration
- `02_SUPPLEMENTARY_INFO.md` - Learn: Supplementary content organization
- `03_REFERENCES.bib` - Learn: BibTeX citation management

**Figure Generation:**
- `FIGURES/Figure__*.mmd` - Learn: System diagrams, workflow illustrations
- `FIGURES/SFigure__*.py` - Learn: Data visualization, live arXiv statistics
- `FIGURES/SFigure__*.R` - Learn: R-based statistical plots

**Code Organization:**
- `src/py/` - Learn: Reusable analysis modules
- Python imports in markdown - Learn: How to integrate analysis code

</details>

## 🚀 Getting Started

### Prerequisites

1. Install [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker):
   
   See the [Official Installation Guide](https://github.com/HenriquesLab/rxiv-maker#installation) for your platform (macOS, Linux, Windows).

2. Ensure you have a LaTeX distribution installed (the installation guide covers this).

### Building the Preprint

```bash
# Clone this repository
git clone https://github.com/HenriquesLab/manuscript-rxiv-maker.git
cd manuscript-rxiv-maker

# Generate the PDF
rxiv pdf MANUSCRIPT/
```

This will:
1. Execute all Python scripts to fetch current arXiv data and generate statistics
2. Create all figures from source data and scripts
3. Process the Markdown content with embedded dynamic values
4. Generate the complete preprint PDF in `MANUSCRIPT/output/`

### Other Commands

```bash
# Build the preprint PDF
rxiv pdf MANUSCRIPT/

# Generate figures only
rxiv figures MANUSCRIPT/

# Validate preprint structure
rxiv validate MANUSCRIPT/

# Clean generated files
rxiv clean MANUSCRIPT/

# Export to Word format
rxiv docx MANUSCRIPT/
```

<details>
<summary><b>🎓 Educational Use - Command Explanations</b></summary>

**Why these commands are useful for learning:**

- `rxiv pdf` - See the complete workflow from markdown to publication PDF
- `rxiv figures` - Understand how figure generation works independently
- `rxiv validate` - Learn what makes a valid rxiv-maker manuscript
- `rxiv clean` - Understand what gets generated vs. what's source

**Try these learning exercises:**
1. Run `rxiv clean` then `rxiv pdf MANUSCRIPT/` to see the full build process
2. Modify a figure script in `FIGURES/` and run `rxiv figures MANUSCRIPT/`
3. Change citation style in `00_CONFIG.yml` and rebuild
4. Add a new citation to `03_REFERENCES.bib` and reference it in `01_MAIN.md`

</details>

## 📁 Repository Structure

```
MANUSCRIPT/
├── 00_CONFIG.yml              # Preprint configuration and metadata
├── 01_MAIN.md                 # Main preprint content
├── 02_SUPPLEMENTARY_INFO.md   # Supplementary information
├── FIGURES/                   # Figure generation scripts
│   ├── Figure__*.py          # Main figure scripts (system diagrams, workflows)
│   └── SFigure__*.py         # Supplementary figure scripts (arXiv data visualizations)
├── DATA/                     # Live data files (arXiv statistics, etc.)
├── src/                      # Source code and utilities for the preprint
│   └── py/                   # Python modules for data processing and analysis
└── output/                   # Generated preprint PDF and LaTeX files
```

## 🎨 Live Figure Generation

The preprint includes figures that are generated from real, current data:

- **arXiv growth analysis**: Live plots of preprint submission trends using current arXiv statistics
- **System diagrams**: Technical illustrations of the rxiv-maker architecture and workflow
- **Data visualization**: Professional plots using matplotlib and seaborn with real scientific data
- **Self-updating content**: Figures and statistics that refresh with the latest data when rebuilt
- **Publication quality**: High-resolution outputs ready for academic publication

## 📚 Citation Features

This manuscript demonstrates rxiv-maker's flexible citation management:

### Multiple Citation Styles
Switch between numbered `[1, 2]` and author-date `(Smith, 2024)` formats:
```yaml
# In 00_CONFIG.yml
citation_style: "numbered"      # [1, 2, 3] (default)
citation_style: "author-date"   # (Smith, 2024; Jones, 2023)
```

### Inline DOI Resolution
Paste DOIs directly in markdown - rxiv-maker automatically:
- Fetches metadata from CrossRef/DataCite
- Generates BibTeX entries
- Replaces DOIs with citation keys

```yaml
# In 00_CONFIG.yml
enable_inline_doi_resolution: true
```

**Example workflow:**
```markdown
Recent advances 10.1038/nature12373 enable new techniques.
```
Auto-converts to:
```markdown
Recent advances @smith2024 enable new techniques.
```

With complete BibTeX entry generated automatically!

### Learn More
- **[Citations Tutorial](https://rxiv-maker.henriqueslab.org/getting-started/citations-tutorial/)** - Hands-on practice
- **[Complete Guide](https://rxiv-maker.henriqueslab.org/guides/citations-and-references/)** - Comprehensive reference

## 🔗 Rxiv-Maker Ecosystem

### Core Components
- **🛠️ Main Framework**: [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker) - The core tool for converting Markdown to publication-ready PDFs
- **🐳 Docker Support**: [docker-rxiv-maker](https://github.com/HenriquesLab/docker-rxiv-maker) - Containerized execution with pre-configured environment
- **💻 VS Code Extension**: [vscode-rxiv-maker](https://github.com/HenriquesLab/vscode-rxiv-maker) - IDE integration with syntax highlighting and validation
- **🌐 Official Website**: [rxiv-maker.henriqueslab.org](https://rxiv-maker.henriqueslab.org) - Documentation, guides, and tutorials
- **📄 This Repository**: Contains the official paper (JCS doi:10.1242/jcs.265183, arXiv:2508.00836) and comprehensive usage example

### Documentation & Resources
- **Getting Started**: [Installation Guide](https://rxiv-maker.henriqueslab.org/getting-started/installation/)
- **First Manuscript**: [Tutorial](https://rxiv-maker.henriqueslab.org/getting-started/first-manuscript/)
- **User Guides**: [Complete Documentation](https://rxiv-maker.henriqueslab.org/guides/)
- **Google Colab**: [Try Online](https://colab.research.google.com/github/HenriquesLab/rxiv-maker/blob/main/notebooks/rxiv_maker_colab.ipynb)
- **GitHub Actions**: [CI/CD Guide](https://github.com/HenriquesLab/rxiv-maker/blob/main/docs/github-actions-guide.md)

## 📖 Citation

If you use rxiv-maker or reference this preprint, please cite:

```bibtex
@article{saraiva_2025_rxivmaker,
  title={Rxiv-Maker: An automated template engine for streamlined scientific publications},
  author={Bruno M. Saraiva and Rita Carlota and António D. Brito and Iván Hidalgo-Cenalmor and Guillaume Jacquemet and Ricardo Henriques},
  journal={Journal of Cell Science},
  year={2026},
  doi={10.1242/jcs.265183},
  url={https://doi.org/10.1242/jcs.265183}
}
```

## 📄 License

This preprint is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

## 🤝 Contributing

Found an issue or want to improve this preprint? Please open an issue or pull request on the [main rxiv-maker repository](https://github.com/HenriquesLab/rxiv-maker/issues).

---

**Note**: This repository contains the official rxiv-maker preprint (arXiv:2508.00836) which both documents the framework and serves as a comprehensive example of scientific writing with rxiv-maker. The source code demonstrates reproducible manuscript preparation with live data integration.