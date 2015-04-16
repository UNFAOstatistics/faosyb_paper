# Introduction

I created source files for three documents, for a proper academic paper, for a presentation slides and for notes.

To see them *rendered* click the links from below:

- [theory_paper.pdf](https://rawgithub.com/digieast/paperx/master/theory_paper.pdf)
- [slides.html](https://rawgithub.com/digieast/paperx/master/slides.html)

## Processing the source files

To set up your software environment look at: [https://github.com/digieast/digicoffee/blob/master/methods_tools.md](https://github.com/digieast/digicoffee/blob/master/methods_tools.md)

### Commands

**This has been tested in using pandoc 1.12.3 version in Windows 7 and Ubuntu linux 12.04**

Use following scripts to convert slides into desired format

For converting the **theory_paper.md**

- **pdf**: `pandoc --filter pandoc-citeproc theory_paper.md -o theory_paper.pdf --toc --number-sections`
- **docx**: `pandoc --filter pandoc-citeproc theory_paper.md -o theory_paper.docx --toc --number-sections`

For converting the **slides.md**

- **reveal.js html**: `pandoc -t revealjs -s slides.md -o slides.html -V revealjs-url=http://lab.hakim.se/reveal-js -V theme=simple -V transition=fade`
- **pdf**: `pandoc -t beamer slides.md -o slides.pdf`


