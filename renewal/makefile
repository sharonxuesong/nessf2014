FILE = proposal
REF = references
TEX = latex
BIBTEX = bibtex
DVIPDF = dvipdf

.PHONY: all clean

all: $(FILE).dvi $(FILE).pdf

$(FILE).dvi : $(FILE).tex makefile references.bib
	$(TEX) $(FILE)
	$(BIBTEX) $(FILE)
	$(TEX) $(FILE)
	$(TEX) $(FILE)

$(FILE).pdf : $(FILE).dvi
	$(DVIPDF) $(FILE).dvi
	open $(FILE).pdf &
	cp $(FILE).pdf /astro/grads/xxw131/Dropbox/Public/nessf2015.pdf

clean :
#	\rm *Notes.bib
	\rm *.aux
	\rm *.bbl
	\rm *.log
	\rm *.blg
	\rm *.dvi
#	\rm *.out
