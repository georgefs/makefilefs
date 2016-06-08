MFDB?=https://raw.githubusercontent.com/georgefs/makefilefs/master/src/
MFPATH?=/usr/local/include/

help::
	@echo main help

%.mf:
	@echo download plugin $@
	mkdir -p `dirname $(MFPATH)$@` && \
	curl $(MFDB)$@ > $(MFPATH)$@

clean_plugin:
	rm `find /usr/local/include/**/*.mf` `find /usr/local/include/*.mf`


MFCONF?=configure

include base.mf
include $(MFCONF)
include $(PLUGINS)

