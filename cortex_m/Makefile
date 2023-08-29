all: patch

# Path to `svd`/`svdtools`
SVDTOOLS ?= svdtools

YAMLS := $(wildcard *.yaml)
PATCHED_SVDS := $(patsubst %.yaml, %.svd.patched, $(YAMLS))

%.svd.patched: %.yaml %.svd
	$(SVDTOOLS) patch $<

patch: $(PATCHED_SVDS)

clean:
	rm -f $(PATCHED_SVDS)
