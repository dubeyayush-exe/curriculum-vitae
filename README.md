# Ayush Dubey - Curriculum Vitae

[![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat&logo=latex&logoColor=white)](https://www.latex-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Professional CV/Resume built with LaTeX, showcasing experience in AI/ML, research, and software development.

## 📄 About

This repository contains my professional CV, detailing my academic background, professional experience, research publications, projects, and technical skills in the field of Computer Science with specialization in Artificial Intelligence and Machine Learning.

## 🎓 Highlights

- **Education**: B.E. in Computer Science (AI & ML) from Chandigarh University
- **Current Role**: Research & Development Intern at DRDO
- **Previous Experience**: Machine Learning Intern at Patanjali Ayurveda Pvt. Ltd.
- **Research**: Published paper on Heart Failure Prediction using ANN at ICETET-SIP 25
- **Technical Skills**: Python, TensorFlow, PyTorch, OpenCV, Spring Boot, AWS

## 🚀 Quick Start

### Prerequisites

To compile this CV, you need:
- A LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- Required LaTeX packages (see dependencies below)

### Compilation

#### Using `pdflatex`:
```bash
pdflatex cv.tex
biber cv
pdflatex cv.tex
pdflatex cv.tex
```

#### Using `xelatex` (recommended for custom fonts):
```bash
xelatex cv.tex
biber cv
xelatex cv.tex
xelatex cv.tex
```

#### Using Overleaf:
1. Upload `cv.tex` to [Overleaf](https://www.overleaf.com/)
2. Click "Recompile" to generate the PDF

## 📦 Dependencies

The following LaTeX packages are required:

- `fontawesome5` - For social media icons
- `xcolor` - For color support
- `hyperref` - For clickable links
- `tabularx` - For advanced table formatting
- `titlesec` - For custom section formatting
- `biblatex` - For bibliography management
- `enumitem` - For customized lists
- `geometry` - For page layout customization

Most LaTeX distributions include these packages by default.

## 🔧 Customization

### Updating Personal Information

Edit the header section in `cv.tex`:

```latex
\begin{tabularx}{\linewidth}{@{} C @{}}
\Huge{Your Name} \\[7.5pt]
\href{https://github.com/username}{GitHub} \ $|$ \ 
\href{https://linkedin.com/in/username}{LinkedIn} \ $|$ \ 
...
\end{tabularx}
```

### Adding New Sections

The CV uses custom environments for job entries:

**Short job entry** (no bullet points):
```latex
\begin{jobshort}{Position Title}{Date Range}
Description text here
\end{jobshort}
```

**Long job entry** (with bullet points):
```latex
\begin{joblong}{Position Title}{Date Range}
\item First achievement or responsibility
\item Second achievement or responsibility
\end{joblong}
```

### Modifying Colors

Change link colors by editing:
```latex
\definecolor{linkcolour}{rgb}{0,0.2,0.6}
```

## 📊 Structure

```
.
├── cv.tex              # Main CV LaTeX file
├── citations.bib       # Bibliography file (if needed)
└── README.md          # This file
```

## 🤖 Auto-Compilation with GitHub Actions

You can set up automatic PDF generation using GitHub Actions:

1. Create `.github/workflows/compile-latex.yml`:

```yaml
name: Build LaTeX CV
on: [push]

jobs:
  build_latex:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      
      - name: Compile LaTeX
        uses: xu-cheng/latex-action@v2
        with:
          root_file: cv.tex
      
      - name: Upload PDF
        uses: actions/upload-artifact@v3
        with:
          name: CV-PDF
          path: cv.pdf
```

2. Push to GitHub - PDF will be generated automatically on each commit

## 📱 Online Profiles

- **GitHub**: [dubeyayush-exe](https://github.com/dubeyayush-exe)
- **LinkedIn**: [Ayush Dubey](https://www.linkedin.com/in/ayush-dubey-b445a123a)
- **Portfolio**: [dubeyayush-exe.github.io](https://github.com/dubeyayush-exe/dubeyayush-exe.github.io)
- **Medium**: [@ayushdubey421](https://medium.com/@ayushdubey421)
- **Email**: ayushdubey421@gmail.com

## 📝 License

This project is licensed under the MIT License - see the LICENSE section in `cv.tex` for details.

Original template by [Jitin Nair](https://github.com/jitinnair1).

## 🙏 Acknowledgments

- Template inspired by various LaTeX CV templates
- Built with support from the LaTeX community
- Special thanks to Chandigarh University, DRDO, and Patanjali Ayurveda for professional opportunities

## 📧 Contact

For any queries or suggestions, feel free to reach out via:
- Email: ayushdubey421@gmail.com
- LinkedIn: [Ayush Dubey](https://www.linkedin.com/in/ayush-dubey-b445a123a)

---

**Last Updated**: October 2025

⭐ If you find this CV template helpful, consider giving it a star!