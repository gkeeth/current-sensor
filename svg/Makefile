NAMES   := frontpanel backpanel frontpanel_36A
SOURCES := $(addsuffix .svg, $(NAMES))
TARGETS := $(addsuffix .kicad_mod, $(NAMES))

.PHONY: all

all: $(TARGETS)

%.kicad_mod: %.svg
	svg2mod -i $< -p 0.05
# frontpanel: frontpanel.svg
# 	svg2mod -i frontpanel.svg -p 0.1 --center
# backpanel: backpanel.svg
# 	svg2mod -i frontpanel.svg -p 0.1 --center
