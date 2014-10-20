R = viewdep-paper
STY = TexInputs/IEEEtran.cls
FIG = images/*.pdf images/*.eps images/*.tex

pdf: $(R).pdf

$(R).bbl: $(R).bib
	pdflatex $(R)
	bibtex $(R)
	pdflatex $(R)

$(R).pdf: *.tex $(STY) $(FIG) $(R).bbl
	pdflatex $(R)
	pdflatex $(R)

clean:
	rm -f $(R).log $(R).aux $(R).bbl $(R).blg $(R).out
