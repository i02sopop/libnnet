AM_CFLAGS = -O3
AUTOMAKE_OPTIONS = std-options subdir-objects
lib_LIBRARIES = libnnet.a

libnnet_adir = $(PROJ_DIR)
libnnet_a_SHORTNAME = lnnet
libnnet_a_CFLAGS = -I$(INCLUDE_DIR) -DLOCALEDIR=\"$(localedir)\"
# libnnet_a_LDADD = $(LIBMATH) $(LIBINTL)
# libnnet_a_LDFLAG =
libnnet_a_SOURCES  = libnnet.c
include_HEADERS  = $(INCLUDE_DIR)/libnnet.h
include_HEADERS += $(INCLUDE_DIR)/gettext.h

.PHONY: check-syntax
check-syntax:
	gcc -o nul ${AM_CFLAGS} ${libnnet_CFLAGS} -S ${CHK_SOURCES}
