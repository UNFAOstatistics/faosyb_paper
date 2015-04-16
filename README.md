# Introduction

I created source files for three documents, for a proper academic paper, for a presentation slides and for notes.

To see them *rendered* click the links from below:

- [theory_paper.pdf](https://rawgithub.com/digieast/paperx/master/theory_paper.pdf)
- [slides.html](https://rawgithub.com/digieast/paperx/master/slides.html)

## Processing the source files

To set up your software environment look at: [https://github.com/digieast/digicoffee/blob/master/methods_tools.md](https://github.com/digieast/digicoffee/blob/master/methods_tools.md)

### Commands

**This has been tested in using pandoc 1.13.2 version in Windows 7 and Ubuntu linux 12.04**

Use following scripts to convert slides into desired format

For converting the **faosyb_paper.md**

- **pdf**: `pandoc -r markdown+simple_tables+table_captions+yaml_metadata_block -s -S --latex-engine=pdflatex --template=faosyb.pdf.template --filter pandoc-citeproc --toc --number-section --toc-depth=2 faosyb_paper.md -o faosyb_paper.pdf`
- **docx**: `pandoc --toc --number-section faosyb_paper.md -o faosyb_paper.docx`
- **odt**: `pandoc --toc --number-section faosyb_paper.md -o faosyb_paper.odt`


For converting the **slides.md**

- **reveal.js html**: `pandoc -t revealjs -s slides.md -o slides.html -V revealjs-url=http://lab.hakim.se/reveal-js -V theme=simple -V transition=fade`
- **pdf**: `pandoc -t beamer slides.md -o slides.pdf`


