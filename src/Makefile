include ../../../system/include.mk

include ../vsn.mk
VSN=$(ERESYE_VSN)

MODULES=eresye	\
	eresye_agenda	\
	eresye_ontology	\
	eresye_ontology_resolver	\
	eresye_tree_list

EBIN_FILES=$(MODULES:%=../ebin/%.$(EMULATOR))
ERLC_FLAGS+=-I../../ -I../include +debug_info

#
# Targets
#

all: $(EBIN_FILES) 

debug:
	$(MAKE) ERLC_FLAGS+="$(ERLC_FLAGS) +debug_info -Ddebug"

clean:
	rm -f $(EBIN_FILES)
