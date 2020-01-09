CURDIR=$(shell pwd)
PACKAGE_VERSION :=
PACKAGE_DIR :=
PACKAGE_CONF :=

first_rule: all

all: build

build:
	$(MAKE) -C $(CURDIR)/PACKAGE/astyle      first_rule

clean:
	rm -Rf $(CURDIR)/BIN/; \
	rm -Rf $(CURDIR)/TARGET;
	
config_rule:

install_rule install:

clean_rule distclean clean:

uninstall_rule uninstall:

