TARGET=paper
all: pdf

pdf:
	GS_OPTIONS=-dPDFSETTINGS=/prepress rubber -f --pdf -Wrefs -Wmisc $(TARGET)

clean:
	rm -f *.aux *.log *.out *.bbl *.blg *.brf *~ *.bak $(TARGET).pdf $(TARGET).ps *.toc *.lot *.lof *.bcf *.run.xml

cleanall: clean
	rm -f $(TARGET).pdf

ps: pdf
	GS_OPTIONS=-dPDFSETTINGS=/prepress pdftops -level1 $(TARGET).pdf
