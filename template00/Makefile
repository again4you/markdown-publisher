BOOK = test

$(BOOK).pdf: 
	pandoc -S --toc -H build/pdf.tex -o test.pdf \
		page/01-chapter1.markdown \
		page/01-chapter2.markdown

clean:
	rm $(BOOK).pdf
