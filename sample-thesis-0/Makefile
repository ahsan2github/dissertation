LATEXBIN = lualatex

BIBTEX = bibtex

STYFILES =  amssymbols.sty \
	amssymb.sty \
	bibnames.sty \
	citesort.sty \
	coloralias.sty \
	diagram.sty \
	dissertationapproval.sty \
	lamsarrow.sty \
	mythesis.sty \
	rgb.sty \
	tgrind.sty \
	uuthesis-2016-h.sty \
	uuthesis-chapterbib.sty \
	uuthesis-color-headings.sty \
	uuthesis-index.sty

TEXMAIN = sample-thesis-0.tex
TEXFILES = intro.tex chap1.tex chap2.tex chap3.tex conclusion.tex appa.tex
OUTPUTFILE = ahsan_thesis.pdf

all: $(OUTPUTFILE)


$(OUTPUTFILE): $(TEXMAIN) $(TEXFILES) $(STYFILES)
	$(LATEXBIN) -jobname=$@ $<
	$(BIBTEX) intro
	$(BIBTEX) chap1
	$(BIBTEX) chap2
	$(BIBTEX) chap3
	$(LATEXBIN) -jobname=$@ $<
	$(LATEXBIN) -jobname=$@ $<
	
clean:
	rm -fr $(OUTPUTFILE) *.log *.aux *.lof *.lot
