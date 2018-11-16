.PHONY: all html pdf pages clean deepclean draft set-draft

ASCIIDOCTOR = $(shell command -v asciidoctor)
ifeq ($(ASCIIDOCTOR),)
GEMS = env
ASCIIDOCTOR = $(GEMS)/bin/asciidoctor
endif
DOCS_DIR = ../docs
PDF_FILE = $(DOCS_DIR)/nf-hack18.pdf
SOLUTIONS_DIR = solutions
CHEATSHEET_HTML = $(DOCS_DIR)/cheatsheet.html
CHEATSHEET_PDF = $(DOCS_DIR)/cheatsheet.pdf
STYLESHEETS_DIR = css
ASSETS_DIR = assets
DOCS = index.adoc cloud.adoc training.adoc handson.adoc
DOCS_HTML = $(DOCS:%.adoc=$(DOCS_DIR)/%.html)
CHEATSHEET = cheatsheet.adoc
SOLUTIONS = $(wildcard $(SOLUTIONS_DIR)/*.adoc)
SOLUTIONS_HTML = $(SOLUTIONS:%.adoc=$(DOCS_DIR)/%.html)
PDF = pdf
PDF_STYLE = crg
ATTRS = -a allow-uri-read

all: html
draft: set-draft html 	
set-draft:
	$(eval ATTRS += -a draft)

html: setup $(DOCS_HTML) $(CHEATSHEET_HTML) $(SOLUTIONS_HTML)
$(DOCS_HTML): $(DOCS_DIR)/%.html: %.adoc *.adoc
	@GEM_HOME=$(GEMS) $(ASCIIDOCTOR) $< $(ATTRS) -o $@
	@echo == Written file $@

$(CHEATSHEET_HTML): $(CHEATSHEET) *.adoc
	@GEM_HOME=$(GEMS) $(ASCIIDOCTOR) $(CHEATSHEET) -o $(CHEATSHEET_HTML)
	@echo == Written file $(CHEATSHEET_HTML)

$(SOLUTIONS_HTML): ATTRS = -a nofooter -a linkcss -a stylesdir=../css -a stylesheet=crg.css -a hide-uri-scheme -a icons=font -a source-highlighter=highlight.js -a highlightjs-theme=github
$(SOLUTIONS_HTML): $(DOCS_DIR)/%.html: %.adoc solutions/*.adoc
	@GEM_HOME=$(GEMS) $(ASCIIDOCTOR) $< $(ATTRS) -o $@
	@echo == Written file $@

pdf: setup $(PDF_FILE) $(CHEATSHEET_PDF) *.adoc
$(PDF_FILE): $(DOCS)
	@GEM_HOME=$(GEMS) $(ASCIIDOCTOR)-pdf $(DOCS) -a pdf-stylesdir=$(PDF)/style -a pdf-style=$(PDF_STYLE) -a pdf-fontsdir=$(PDF)/font
	@echo == Written file $(PDF_FILE)

$(CHEATSHEET_PDF): $(CHEATSHEET)
	@GEM_HOME=$(GEMS) $(ASCIIDOCTOR)-pdf $(CHEATSHEET) -a pdf-stylesdir=$(PDF)/style -a pdf-style=$(PDF_STYLE) -a pdf-fontsdir=$(PDF)/font
	@echo == Written file $(CHEATSHEET_PDF)

setup: $(ASCIIDOCTOR)

$(GEMS)/bin/asciidoctor: $(GEMS)
	@GEM_HOME=$(GEMS) $(GEMS)/bin/bundle --path=$(GEMS) --binstubs=$(GEMS)/bin

$(GEMS): $(GEMS)/bin/bundle
$(GEMS)/bin/bundle:
	@GEM_HOME=$(GEMS) gem install bundler

pages: html
	@echo == Updating github pages
	@git ci -m "Update docs" ../docs
	@git push

clean:
	rm -f $(DOCS_HTML) $(CHEATSHEET_HTML) $(PDF_FILE) $(CHEATSHEET_PDF) $(DEPLOY_LIST) $(SOLUTIONS_HTML)

deepclean: clean
	rm -rf $(GEMS) bin .bundle
