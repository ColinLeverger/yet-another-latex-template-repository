all: clean build clean

allfast: buildfast

fastloop:
	while true; do make buildfast; done

buildfast:
	pdflatex -synctex=1 -interaction=nonstopmode report.tex && evince report.pdf

loop:
	while true; do make clean all;	done

build:
	pdflatex -synctex=1 -interaction=nonstopmode report.tex && bibtex *.aux && pdflatex -synctex=1 -interaction=nonstopmode report.tex && pdflatex -synctex=1 -interaction=nonstopmode report.tex && evince report.pdf

clean:
	find . -regextype posix-extended -regex ".*\.(log|bbl|blg|aux|idx|ind|lof|lot|out|toc|acn|acr|alg|glg|glo|gls|ist|bar|bak|gz)" -exec rm {} \;
