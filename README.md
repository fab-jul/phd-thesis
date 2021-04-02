<div align="center">
  <img src='src/cover/cover_with_text.jpg' width="50%"/>
  <a href='https://www.research-collection.ethz.ch/bitstream/handle/20.500.11850/476480/thesis_nightlyfinal_version_pdf.pdf?sequence=1&isAllowed=y'
     style='font-size:200%;'>
    PDF Link
  </a>
</div>


# PhD Thesis

This repo contains my PhD thesis. The LaTeX is based on [this template](http://pletscher.org/blog/2013/03/11/thesis.html), but I modified classicthesis.sty somewhat to have (imo) nicer chapter headings. I also replaced Palatino with Times, as
all figures use Times and I think Times' math looks somewhat cleaner. I ordered the books at [lulu.com](lulu.com), who offer a nice template to design your cover.

### Notes:
- To build the thesis, use `make` inside `src` (`cd src && make`)
- Template uses the "Crown Quarto size", that can be used at [lulu.com](lulu.com), see `preamle.sty`. If you need a different size, change this early!
- There is a `forprint` boolean in preamble.sty that influences how the PDF is 
created, which can be set there as well.
    - When we print, we want to rotate big figures such that they cause a reader
      of the book to rotate the book. Also, we do not want to add the cover and
      backcover as this is done in the web GUI of lulu.
    - When we don't print, we want to rotate the page for the PDF such that a reader
      can scroll through.

### How to convert papers into thesis chapters

1. First copy the whole paper incl. appendix.
2. Remove vspaces etc.
3. Run in vim, where you replace PREFIX with whatever you want the chapter prefix to be:
```
%s/\\label{/\\label{PREFIX:/g | %s/\\ref{/\\ref{PREFIX:/g | %s/\\eqref{/\\eqref{PREFIX:/g
```
4. At the end, to include the Appendices, use

```
\begin{subappendices} \section*{Appendices}  \end{subappendices} 
```

