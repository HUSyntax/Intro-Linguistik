#STYLE-PATH= ${HOME}/.LaTex/
STYLE-PATH= ${HOME}/Library/tex/texmf/latex/


SOURCE= $(wildcard *.tex)

# grundkurs-handout.tex\
# 	00-Organisatorisches-include.tex \
#         01a-sprache-sprachwissenschaft-include.tex\
#         01b-sprache-sprachwissenschaft-include.tex\
#         02-phonetik-include.tex\
# 	03a-phonologie-include.tex\
# 	03b-phonologie-include.tex\
# 	04a-graphematik-include.tex\
# 	05a-wortbildung-include.tex\
# 	05b-flexion-include.tex\
# 	06a-syntax-stefan-include.tex\
# 	06b-xbar-simple-include.tex\
# 	06c-syntax-ip-include.tex\
# 	06-syntax-ha2.tex\
# 	07-semantik-stefan-include.tex\
# 	08-pragmatik-stefan-include.tex



check: check-grundkurs-handout-2x2.pdf

%.pdf: %.tex $(SOURCE) 
	xelatex $*
	bibtex $*
	xelatex $* 
	bibtex $*
	xelatex $* 

# 03bPhonologie-handout.dvi: $(SOURCE2)
# 	latex 03bPhonologie-handout
# 	latex 03bPhonologie-handout
# 	bibtex 03bPhonologie-handout
# 	latex 03bPhonologie-handout 
# 	bibtex 03bPhonologie-handout
# 	latex 03bPhonologie-handout 

# 03bPhonologie-slides.dvi: $(SOURCE2)
# 	latex 03bPhonologie-slides
# 	latex 03bPhonologie-slides
# 	bibtex 03bPhonologie-slides
# 	latex 03bPhonologie-slides 
# 	bibtex 03bPhonologie-slides
# 	latex 03bPhonologie-slides 




silben: 03b-phonologie-handout-2x2.pdf

silben-slides: 03b-phonologie-slides.pdf
silben-handout: 03b-phonologie-handout.pdf

semantik-handout: 07-semantik-handout.pdf

slides: grundkurs-slides.pdf
handout: grundkurs-handout.pdf

ma-handout: ma-uebung-handout.pdf


o-public: grundkurs-handout.pdf dp-tp-handout.pdf 01-sprache-sprachwissenschaft-handout.pdf 02-phonetik-handout.pdf 03a-phonologie-handout.pdf 03b-phonologie-handout.pdf 04a-graphematik-handout.pdf 05-morphologie-handout.pdf 06-syntax-handout.pdf
	scp -p $? hpsg.hu-berlin.de:/home/stefan/public_html/PS/



clean:
	find . -name \*\.bak -exec \rm {} \;
	find . -name \*~ -exec \rm {} \;
	rm -f *.bak *.toc *.bbl *.blg *~ *.log *.aux *.*pk *.cut *.tmp *.out *.nav *.snm


realclean: clean
	rm -f *.dvi *.ps *.pdf


