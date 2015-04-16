# Introduction

A demo of using markdown with version control for writing academic papers

source is here:

- <https://raw.githubusercontent.com/muuankarski/faosyb_paper/master/faosyb_paper.md>

To see different formats *rendered* click the links from below:

## Paper

- pdf: <https://github.com/muuankarski/faosyb_paper/raw/master/faosyb_paper.pdf>
- html: <http://htmlpreview.github.io/?https://raw.githubusercontent.com/muuankarski/faosyb_paper/master/faosyb_paper.html>
- Word: <https://github.com/muuankarski/faosyb_paper/raw/master/faosyb_paper.docx>
- Libreoffice: <https://github.com/muuankarski/faosyb_paper/raw/master/faosyb_paper.odt>

## Slides

- html: <http://htmlpreview.github.io/?https://raw.githubusercontent.com/muuankarski/faosyb_paper/master/slides.html>

## Processing the source files

To set up your software environment look at: [https://github.com/digieast/digicoffee/blob/master/methods_tools.md](https://github.com/digieast/digicoffee/blob/master/methods_tools.md)

### Commands

**This has been tested in using pandoc 1.13.2 version in Windows 7 and Ubuntu linux 12.04**

Use following scripts to convert slides into desired format

For converting the **faosyb_paper.md**

- **pdf**: `pandoc -r markdown+simple_tables+table_captions+yaml_metadata_block -s -S --latex-engine=pdflatex --template=faosyb.pdf.template --filter pandoc-citeproc --toc --number-section --toc-depth=2 faosyb_paper.md -o faosyb_paper.pdf`
- **html**: `pandoc -r markdown+simple_tables+table_captions+yaml_metadata_block -w html -s -S --template=faosyb.html.template -H faosyb.css --filter pandoc-citeproc --number-section --toc faosyb_paper.md -o faosyb_paper.html`
- **docx**: `pandoc --toc --number-section faosyb_paper.md -o faosyb_paper.docx`
- **odt**: `pandoc --toc --number-section faosyb_paper.md -o faosyb_paper.odt`


For converting the **slides.md**

- **reveal.js html**: `pandoc -t revealjs -s slides.md -o slides.html -V revealjs-url=http://lab.hakim.se/reveal-js -V theme=simple -V transition=fade`
- **pdf**: `pandoc -t beamer slides.md -o slides.pdf`


