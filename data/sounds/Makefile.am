
public_sounds = \
    bell.ogg \
    loud-bell.ogg

EXTRA_DIST = \
    $(public_sounds)

install-sounds:
	for sound in $(public_sounds); do \
		mkdir -p $(DESTDIR)$(pkgdatadir)/sounds; \
		$(INSTALL_DATA) $(srcdir)/$$sound $(DESTDIR)$(pkgdatadir)/sounds/$$sound; \
	done

uninstall-sounds:
	for sound in $(public_sounds); do \
		rm -f $(DESTDIR)$(pkgdatadir)/sounds/$$sound; \
	done

install-data-local: install-sounds

uninstall-local: uninstall-sounds
