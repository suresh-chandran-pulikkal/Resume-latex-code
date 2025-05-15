markdown
# LaTeX Resume Compiler

Generate a professional PDF resume from LaTeX source on openSUSE Linux.

## Prerequisites
- openSUSE (Leap or Tumbleweed)
- Basic LaTeX installation

## Quick Start

1. Install required packages:
```bash
sudo zypper install texlive-scheme-full texlive-xetex
```
Compile your resume:
```bash
pdflatex my-cv-in-latex-code.tex
pdflatex my-cv-in-latex-code.tex  # Run twice for proper references
```
Your PDF will be generated as my-cv-in-latex-code.pdf

Advanced Options
Using XeLaTeX (recommended for font support)
```bash
xelatex my-cv-in-latex-code.tex
xelatex my-cv-in-latex-code.tex
```
Clean Build (remove temporary files)
```bash
rm -f *.aux *.log *.out *.toc
```
Automation
For frequent compilation, create a compile.sh script:

```bash
#!/bin/bash
xelatex my-cv-in-latex-code.tex
xelatex my-cv-in-latex-code.tex
rm -f *.aux *.log *.out
```
Make it executable:

```bash
chmod +x compile.sh
./compile.sh
```
Troubleshooting
Missing fonts: Install additional packages:

```bash
sudo zypper install texlive-fontsextra texlive-fontconfig
```
Missing templates: Install common LaTeX packages:

```bash
sudo zypper install texlive-latex-extra texlive-latex-recommended
```
Recommended Workflow
Edit your .tex file

Run the compiler

Check the PDF output

Commit changes:

```bash
git add my-cv-in-latex-code.tex
git commit -m "Updated resume content"
git push
```
License
This project is licensed under the MIT License - see the LICENSE file for details.
