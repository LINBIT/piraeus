PREFIX=
SRC=$(wildcard *.yaml)
DST=$(addprefix ../deploy/$(PREFIX),$(SRC))

all: $(DST)

../deploy/$(PREFIX)%: % Makefile funcs.lib.yml config.yml
	ytt -f config.yml -f funcs.lib.yml -f $< > $@
