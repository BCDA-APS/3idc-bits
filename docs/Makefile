# Minimal Sphinx Makefile.
#
# Targets:
#   html      build HTML into build/html
#   clean     remove build/ and the autoapi output under source/api/
#   linkcheck check external links
#   help      list available targets

SPHINXOPTS    ?=
SPHINXBUILD   ?= sphinx-build
SOURCEDIR     = source
BUILDDIR      = build

.PHONY: help clean Makefile

help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

clean:
	rm -rf "$(BUILDDIR)" "$(SOURCEDIR)/api"

# Catch-all: forward unknown targets to sphinx-build's -M mode.
# Do NOT list 'html', 'linkcheck', etc. in .PHONY -- doing so would
# block this catch-all from matching them.
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
