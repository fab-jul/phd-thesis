.PHONY: all

all:		thesis.pdf

thesis.pdf:	thesis.tex force
			latexmk -pdf $<
			cp thesis.pdf thesis_out/thesis_nightly$(TAG).pdf

force:		;


.PHONY: clean

clean:
			latexmk -C
			rm -f *.auxlock *.snm *.nav *.out *.fdb_latexmk *.vrb *.table *.gnuplot *-blx.bib *.mtc* *.maf *.bbl *.run.xml

