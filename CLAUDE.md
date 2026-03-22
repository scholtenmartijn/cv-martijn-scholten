# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A LaTeX CV for Martijn Scholten. The main file is `cv.tex`, which inputs section files from `sections/` and a gitignored `secrets.tex` for private contact info (phone number).

## Building

Requires a LaTeX distribution (`texlive-full` on Linux, `mactex` on macOS).

```bash
pdflatex cv.tex
```

Or with auto-rebuild:
```bash
latexmk -pdf cv.tex
```

## Secrets

`secrets.tex` is gitignored. Copy from `secrets.tex.example` to set up:
```bash
cp secrets.tex.example secrets.tex
```

It defines `\phonenumber` — never commit real contact details.

## Structure

- `cv.tex` — Main document: packages, colors, custom commands (`\cvsection`, `\cventry`, `\skilltag`), and section includes
- `sections/` — One file per CV section: header, profile, skills, experience, education, projects
- `secrets.tex` — Private data (gitignored), provides `\phonenumber` command

## Custom LaTeX Commands

Defined in `cv.tex`, used throughout sections:

- `\cvsection{Title}` — Section heading with horizontal rule
- `\cventry{Role}{Date}{Company}{Location}` — Work experience entry
- `\skilltag{Skill}` — Rounded tag pill for skills

## Git

Do not use git commands at all
