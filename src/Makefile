V=20131125

PREFIX = /usr/local

install:
	install -dm755 $(DESTDIR)$(PREFIX)/share/pacman/keyrings/
	install -m0644 bbqlinux{.gpg,-trusted,-revoked} $(DESTDIR)$(PREFIX)/share/pacman/keyrings/

uninstall:
	rm -f $(DESTDIR)$(PREFIX)/share/pacman/keyrings/bbqlinux{.gpg,-trusted,-revoked}
	rmdir -p --ignore-fail-on-non-empty $(DESTDIR)$(PREFIX)/share/pacman/keyrings/

dist:
	git archive --format=tar --prefix=bbqlinux-keyring-$(V)/ $(V) | gzip -9 > bbqlinux-keyring-$(V).tar.gz
	gpg --detach-sign --use-agent bbqlinux-keyring-$(V).tar.gz

.PHONY: install uninstall dist
