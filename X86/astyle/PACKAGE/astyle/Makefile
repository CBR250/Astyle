first_rule: all

all: build install

PACKAGE_NAME := astyle_3.1_linux
PACKAGE_DIR  := astyle
INSTALL_DIR  := $(CURDIR)/../../BIN/
TARGET_DIR   := $(CURDIR)/../../TARGET

# Configuration
PACKAGE_CONF := \
    --prefix=$(CURDIR)/../../OBJ/ \

config_rule:
	if [ ! -d $(TARGET_DIR) ]; then \
	   mkdir $(TARGET_DIR)/; \
	   mkdir $(INSTALL_DIR); \
	fi
	if [ -d $(TARGET_DIR)/$(PACKAGE_DIR) ]; then \
	       echo "Folder existed"; \
	else \
	       tar xvf $(CURDIR)/$(PACKAGE_NAME).tar.gz -C $(TARGET_DIR)/; \
	fi

build_lib: config_rule
	cd $(TARGET_DIR)/$(PACKAGE_DIR)/build/gcc  \

build: build_lib
	$(MAKE) -C $(TARGET_DIR)/$(PACKAGE_DIR)/build/gcc all

install:
	@if [ -d $(INSTDIR) ]; \
	then \
		cp -Rf $(TARGET_DIR)/$(PACKAGE_DIR)/build/gcc/bin/*  $(INSTALL_DIR); \
		echo “Installed in $(INSTALL_DIR)“;\
	else \
		echo “Sorry, $(INSTDIR) does not exist”;\
	fi

clean_rule:

uninstall_rule:
