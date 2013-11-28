# $Id$
# Maintainer: Daniel Hillenbrand <codeworkx [at] bbqlinux [dot] org>

pkgname=bbqlinux-keyring
pkgver=20131125
pkgrel=1
pkgdesc='BBQLinux PGP keyring'
arch=('any')
url='https://github.com/bbqlinux/bbqlinux-keyring'
license=('GPL')
install="${pkgname}.install"

package() {
	cd "${srcdir}"
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
