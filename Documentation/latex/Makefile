# Definitions of macros
PDFNAME = GroundSegment

# Default target
all: $(PDFNAME).pdf

# Target to build the PDF
$(PDFNAME).pdf: main.tex
	pdflatex $< --job-name=$(PDFNAME)

# Target for additional runs of pdflatex to resolve references
$(PDFNAME).pdf: main.aux
	pdflatex main.tex --job-name=$(PDFNAME)

# Target to generate the aux file
main.aux: main.tex
	pdflatex $< --job-name=$(PDFNAME)

# Target to clean auxiliary files
clean:
	@echo " *** DELETING ALL LaTeX COMPILATION FILES ***"
	@/bin/rm -f *.aux *.log *.synctex.gz *.toc *.dvi *.out */*.aux

# Target to remove the generated PDF
rmpdf:
	@echo " *** DELETING THE FOLLOWING PDF --> $(PDFNAME).pdf ***"
	@/bin/rm -f $(PDFNAME).pdf