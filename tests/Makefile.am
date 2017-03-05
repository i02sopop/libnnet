TESTS = check_libnnet
check_PROGRAMS = check_libnnet
check_libnnet_SOURCES = test.c
check_libnnet_CFLAGS = -I$(INCLUDE_DIR) -DLOCALEDIR=\"$(localedir)\" $(CHECK_CFLAGS)
check_libnnet_LDADD = $(LIBMATH) $(LIBINTL) $(CHECK_LIBS)

