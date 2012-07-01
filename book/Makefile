# Makefile for the book

PAPERBACK=paperback
TEX=xelatex
BIB=./make_bibtex.sh
MIDX=makeindex


# Build the PDF for the paperback
paperback : ${PAPERBACK}.tex
	${TEX} ${PAPERBACK};true
	${BIB};true	
	${TEX} ${PAPERBACK};true
	${TEX} ${PAPERBACK};true
	${MIDX} ${PAPERBACK};true
	${TEX} ${PAPERBACK};true
	${TEX} ${PAPERBACK};true
	grep -i "undefined" ${PAPERBACK}.log;true


# Delete all the guff and build matter
clean : 
	rm *.out *.bbl *.blg *.aux *.idx *.log *.toc *.ilg *.ind *.synctex.gz

# View the PDF on Linux
vl:
	acroread paperback.pdf

# View the PDF on Mac
vm:
	open -a Preview paperback.pdf
