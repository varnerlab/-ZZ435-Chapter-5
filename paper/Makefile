TEX = chapter5
LATEX = pdflatex -shell-escape -interaction=nonstopmode

.PHONY: all clean

all: $(TEX).pdf

$(TEX).pdf: $(TEX).tex Reference.bib
	$(LATEX) $(TEX)
	bibtex $(TEX)
	$(LATEX) $(TEX)
	$(LATEX) $(TEX)

clean:
	rm -f $(TEX).aux $(TEX).bbl $(TEX).blg $(TEX).log $(TEX).out $(TEX).pdf $(TEX).synctex.gz
	rm -rf _minted-$(TEX)
