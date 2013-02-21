# NOTE: plutil can be installed via:  sudo apt-get install libplist-utils
SOURCES_JSON=$(wildcard *.json)
SOURCES_THEME=$(wildcard *.theme)
PRODUCT_PLIST=$(SOURCES_JSON:%.json=../%) $(SOURCES_THEME:%.theme=../%.tmTheme)
PLIST_CONVERT=../bin/plist-convert
THEME_CONVERT=../bin/theme-convert

all: $(PRODUCT_PLIST)

dev:
	ffkit-reloader . make

../%: %.json
	@$(PLIST_CONVERT) $< $@

../%.tmTheme: %.theme
	@$(THEME_CONVERT) $< $@

# EOF
