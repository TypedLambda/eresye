include ../../../system/include.mk

include ../vsn.mk
VSN=$(ERESYE_VSN)

MODULES=auto	\
	cannibals	\
	journal_sample	\
	phil	\
	prodcons	\
	relatives	\
	sample	\
	sieve	\
	wine_sample

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
