# Example Manuscript for Rxiv-Maker

This repository contains a complete example manuscript demonstrating the capabilities of [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker), a tool for writing scientific preprints in Markdown with automated figure generation.

## 📚 What's Inside

This manuscript showcases:

- **Markdown-based writing**: Clean, readable scientific content in `01_MAIN.md`
- **Automated figure generation**: Python scripts in `FIGURES/` that generate publication-ready plots
- **Supplementary information**: Additional content in `02_SUPPLEMENTARY_INFO.md`
- **Configuration**: Manuscript settings in `00_CONFIG.yml`
- **Data processing**: Python modules in `src/py/` for data analysis
- **Citations and references**: BibTeX integration for academic citations

## 🚀 Getting Started

### Prerequisites

1. Install [rxiv-maker](https://github.com/HenriquesLab/rxiv-maker):
   ```bash
   pipx install rxiv-maker
   ```

2. Ensure you have a LaTeX distribution installed (see [rxiv-maker installation guide](https://github.com/HenriquesLab/rxiv-maker#installation))

### Building the Manuscript

```bash
# Clone this repository
git clone https://github.com/HenriquesLab/manuscript-rxiv-maker.git
cd manuscript-rxiv-maker

# Generate the PDF
rxiv pdf MANUSCRIPT/
```

This will:
1. Execute all Python figure generation scripts
2. Process the Markdown content
3. Generate a publication-ready PDF in `MANUSCRIPT/output/`

### Other Commands

```bash
# Generate figures only
rxiv figures MANUSCRIPT/

# Validate manuscript structure
rxiv validate MANUSCRIPT/

# Clean generated files
rxiv clean MANUSCRIPT/
```

## 📁 Repository Structure

```
MANUSCRIPT/
├── 00_CONFIG.yml              # Manuscript configuration
├── 01_MAIN.md                 # Main manuscript content
├── 02_SUPPLEMENTARY_INFO.md   # Supplementary information
├── FIGURES/                   # Figure generation scripts
│   ├── Figure__*.py          # Main figure scripts
│   └── SFigure__*.py         # Supplementary figure scripts
├── DATA/                     # Data files
├── src/                      # Source code and utilities
│   └── py/                   # Python modules
└── output/                   # Generated files (created during build)
```

## 🎨 Figure Generation

The manuscript includes several example figures that demonstrate:

- **Data visualization**: Plots using matplotlib and seaborn
- **Statistical analysis**: Data processing and visualization
- **Dynamic content**: Figures that update based on current data
- **Publication quality**: High-resolution outputs suitable for journals

## 🔗 Learn More

- **Main Project**: [rxiv-maker on GitHub](https://github.com/HenriquesLab/rxiv-maker)
- **Documentation**: [Rxiv-Maker Guide](https://github.com/HenriquesLab/rxiv-maker#documentation)
- **Paper**: [arXiv:2508.00836](https://arxiv.org/abs/2508.00836)

## 📄 License

This example manuscript is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

## 🤝 Contributing

Found an issue or want to improve the example? Please open an issue or pull request on the [main rxiv-maker repository](https://github.com/HenriquesLab/rxiv-maker/issues).

---

**Note**: This is an example manuscript designed to showcase rxiv-maker's features. The content serves as a demonstration and template for creating your own scientific manuscripts.