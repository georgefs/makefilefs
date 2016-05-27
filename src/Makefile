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


## include all plugin if need
include base.mf pgsql/pgsql.mf redis/redis.mf virtualenv/virtualenv.mf

DATABASE_URL=postgres://$(PGUSER):$(PGPASSWORD)@$(PGHOST):$(PGPORT)
REDIS_URL=redis://$(REDIS_HOST):$(REDIS_PORT)

env::
	@echo DATABASE_URL=$(DATABASE_URL)
	@echo REDIS_URL=$(REDIS_URL)
	@echo DJANGO_SETTINGS_MODULE=op.settings.local
