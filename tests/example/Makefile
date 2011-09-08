.PHONY : all clean tex pdf view

w2b = ../../code/wiki2beamer

all: tex pdf

tex: example.tex

pdf: example.pdf example-pygments.pdf

view: example.pdf
	evince example.pdf

example.tex: example.txt Makefile $(w2b)
	$(w2b) $< -o $@

example-pygments.tex: example.txt Makefile $(w2b)
	$(w2b) $< -o $@ -c pygments

%.pdf: %.tex Makefile
	pdflatex $<

clean:
	rm example.aux example.log example.nav example.out example.pdf example.snm example.tex example.toc example.vrb example-pygments.*
