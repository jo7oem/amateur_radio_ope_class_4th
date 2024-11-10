PWD = $(shell pwd)
OUTPUT_DIR=${PWD}/out

.PHONY: build
build: ${OUTPUT_DIR}/無線工学基礎.pdf
	@echo Building

${OUTPUT_DIR}/無線工学基礎.pdf: 無線工学基礎.tex
	mkdir -p out
	lualatex -file-line-error -interaction=nonstopmode -synctex=1 -output-format=pdf -output-directory=$(dir $@) $(notdir $<)

無線工学基礎.tex: $(wildcard tex/*)
	touch $@

.PHONY: clean
clean:
	rm -rf ${OUTPUT_DIR}