PLUGINS_HOME=$(HOME)/.mf/plugins/
INC=$(PLUGINS_HOME)

MFDB=https://raw.githubusercontent.com/georgefs/makefilefs/master/src/

help::
	@echo main help

%.mf:
	@echo download plugin $@
	mkdir -p `dirname /usr/local/include/$@` && \
	curl $(MFDB)$@ > /usr/local/include/$@

clean_plugin:
	rm `find /usr/local/include/**/*.mf` `find /usr/local/include/*.mf`

include configure
include $(PLUGINS)
