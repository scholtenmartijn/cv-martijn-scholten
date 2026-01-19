# My CV

This repository is where I maintain my CV in LaTeX. It tells the story of my journey: from writing code as a full stack developer, to architecting cloud platforms, leading a Kubernetes practice across Europe, and eventually starting my own freelance business.

I keep it in Git because version control for a CV just makes sense. Every big role, every big project and every big skill I use day-to-day is tracked.

## Structure

```
cv.tex              # Main file
sections/
├── header.tex      # Contact info
├── profile.tex     # About me
├── skills.tex      # Technical skills
├── experience.tex  # Work history
├── education.tex   # Education & certs
└── projects.tex    # Side projects
```

## Setup

Copy the example secrets file and add your phone number:

```bash
cp secrets.tex.example secrets.tex
```

This keeps personal contact info out of version control.

## Building

You'll need a LaTeX distribution.

macOS:
```bash
brew install --cask mactex
```

Linux (Debian/Ubuntu):
```bash
sudo apt install texlive-full
```

Windows: [Here is a link](https://en.wikipedia.org/wiki/List_of_Linux_distributions)

Then compile:

```bash
pdflatex cv.tex
```

Or use latexmk:

```bash
latexmk -pdf cv.tex
```
