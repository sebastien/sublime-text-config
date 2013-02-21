# NOTE: plutil can be installed via:  sudo apt-get install libplist-utils
SOURCES_JSON=$(wildcard *.json)
PRODUCT_PLIST=$(SOURCES_JSON:%.json=../%)
PLIST_CONVERT=./plist-convert

all: $(PRODUCT_PLIST)
	
dev:
	ffkit-reloader . make

../%: %.json
	@$(PLIST_CONVERT) $< $@

# EOF
