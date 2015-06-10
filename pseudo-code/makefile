FILENAME = makeHicuts
TEX = $(FILENAME).tex
DVI = $(FILENAME).dvi
PDF = $(FILENAME).pdf


all:
	make tex
#	make pbibtex
	make tex
	make dvipdf

distclean: clean
	make clean

clean: 
	rm *.aux *.dvi *.ilg *.ind *.log *.out *.toc *~

tex:
	platex $(TEX)

pbibtex:
	pbibtex $(FILENAME)
dvipdf:
	dvipdfmx $(DVI)

%.pdf: %.dvi
	dvipdfmx $<
