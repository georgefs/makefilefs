PLUGINS_HOME=$(HOME)/.mf/plugins/
INC=$(PLUGINS_HOME)

plugin_path=$(PLUGINS_HOME)$(1)
MFDB=https://raw.githubusercontent.com/georgefs/makefilefs/master/src/

## plugin downloader
%.mf:
	@echo download plugin $@
	@mkdir -p `dirname $(call plugin_path,$@)` && \
	@curl $(MFDB)$@ > $(call plugin_path,$@)
	


## include all plugin if need
include base.mf pgsql/pgsql.mf

## setup custom variable in this
