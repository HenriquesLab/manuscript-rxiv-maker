# Rxiv-Maker: Official Preprint & Comprehensive Example

> 📚 **Dual Purpose Repository**: This repository serves two important roles:
> 1. **Official Published Preprint** - The rxiv-maker paper published as [arXiv:2508.00836](https://arxiv.org/abs/2508.00836)
> 2. **Comprehensive Working Example** - A complete demonstration of all rxiv-maker features
>
> Clone it instantly with: `rxiv get-rxiv-preprint`

This repository contains the official rxiv-maker preprint published as [arXiv:2508.00836](https://arxiv.org/abs/2508.00836). This preprint both explains what rxiv-maker is and serves as an extensive demonstration of how scientific preprints can be written using [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker), a framework for writing scientific manuscripts in Markdown with automated figure generation.

## 📚 What's Inside

This preprint demonstrates rxiv-maker's capabilities while documenting the framework itself:

- **Self-documenting preprint**: The content in `01_MAIN.md` explains rxiv-maker while being written with it
- **Live data integration**: Python scripts that pull current arXiv statistics and inject them into the text
- **Automated figure generation**: Python scripts in `FIGURES/` that generate publication-ready plots from real data
- **Supplementary information**: Additional technical details in `02_SUPPLEMENTARY_INFO.md`
- **Complete workflow**: Configuration in `00_CONFIG.yml`, data processing modules in `src/py/`, and BibTeX references
- **Reproducible science**: Every figure and statistic is generated from source data and code

## 🚀 Getting Started

### Prerequisites

1. Install [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker):
   ```bash
   pipx install rxiv-maker
   ```

2. Ensure you have a LaTeX distribution installed (see [rxiv-maker installation guide](https://github.com/HenriquesLab/rxiv-maker#installation))

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
# Generate figures only
rxiv figures MANUSCRIPT/

# Validate preprint structure
rxiv validate MANUSCRIPT/

# Clean generated files
rxiv clean MANUSCRIPT/
```

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

- **ArXiv growth analysis**: Live plots of preprint submission trends using current arXiv statistics
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
- **[10-Minute Tutorial](https://rxiv-maker.henriqueslab.org/getting-started/citations-tutorial/)** - Hands-on practice
- **[Complete Guide](https://rxiv-maker.henriqueslab.org/guides/citations-and-references/)** - Comprehensive reference

## 🔗 Rxiv-Maker Ecosystem

### Core Components
- **🛠️ Main Framework**: [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker) - The core tool for converting Markdown to publication-ready PDFs
- **🐳 Docker Support**: [docker-rxiv-maker](https://github.com/HenriquesLab/docker-rxiv-maker) - Containerized execution with pre-configured environment
- **💻 VS Code Extension**: [vscode-rxiv-maker](https://github.com/HenriquesLab/vscode-rxiv-maker) - IDE integration with syntax highlighting and validation
- **🌐 Official Website**: [rxiv-maker.henriqueslab.org](https://rxiv-maker.henriqueslab.org) - Documentation, guides, and tutorials
- **📄 This Repository**: Contains the official preprint (arXiv:2508.00836) and comprehensive usage example

### Documentation & Resources
- **Getting Started**: [Installation Guide](https://rxiv-maker.henriqueslab.org/getting-started/installation/)
- **First Manuscript**: [Tutorial](https://rxiv-maker.henriqueslab.org/getting-started/first-manuscript/)
- **User Guides**: [Complete Documentation](https://rxiv-maker.henriqueslab.org/guides/)
- **Google Colab**: [Try Online](https://colab.research.google.com/github/HenriquesLab/rxiv-maker/blob/main/notebooks/rxiv_maker_colab.ipynb)
- **GitHub Actions**: [CI/CD Guide](https://github.com/HenriquesLab/rxiv-maker/blob/main/docs/github-actions-guide.md)

## 📖 Citation

If you use rxiv-maker or reference this preprint, please cite:

```bibtex
@misc{saraiva_2025_rxivmaker,
  title={Rxiv-Maker: an automated template engine for streamlined scientific publications},
  author={Bruno M. Saraiva and António D. Brito and Guillaume Jaquemet and Ricardo Henriques},
  year={2025},
  eprint={2508.00836},
  archivePrefix={arXiv},
  url={https://arxiv.org/abs/2508.00836}
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