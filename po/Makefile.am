PROJ_NAME=libnnet
LANGUAGES=es en

.PHONY: update-pot update-po new-lang all
update-pot:
	@xgettext -L C -j $(SOURCE_DIR)/*.c $(INCLUDE_DIR)/*.h -o $(PROJ_NAME).pot

update-po:
	@for i in ${LANGUAGES}; do \
		msgmerge -U -i ${PO_DIR}/$$i.po ${PO_DIR}/$(PROJ_NAME).pot; \
	done

new-lang:
	@for i in ${NEW_LANG}; do \
		msginit -i ${PO_DIR}/$(PROJ_NAME).pot -o ${PO_DIR}/$$i.po; \
	done

all:
	@make update-pot
	@make update-po
