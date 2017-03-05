SUBDIRS= po src tests
ACLOCAL_AMFLAGS=-I m4
EXTRA_DIST=.build-aux/config.rpath
EXTRA_CLEAN=.build-aux ABOUT-NLS Makefile Makefile.in aclocal.m4 autom4te.cache \
			config.h config.h.in* config.log config.status configure m4 stamp-h1 \
			intl po/Makefile po/Makefile.in po/Makefile.in.in tests/Makefile \
		        tests/Makefile.in src/Makefile src/Makefile.in src/.deps \
			po/Makevars.template po/Rules-quot po/boldquot.sed \
			po/en@boldquot.header po/en@quot.header po/insert-header.sin \
			po/quot.sed po/remove-potcdate.sin

.PHONY: update-pot update-po
update-pot:
	@make -C ${PO_DIR} update-pot

update-po:
	@make -C ${PO_DIR} update-po

.PHONY: check-syntax
check-syntax:
	gcc -o nul ${AM_CFLAGS} -S ${CHK_SOURCES}

.PHONY: clean-all
clean-all: clean
	@rm -f *~
	@for i in ${SUBDIRS}; do \
		rm -f $$i/*~ ; \
	done
	@for i in ${EXTRA_CLEAN}; do \
		rm -fr $$i; \
	done
