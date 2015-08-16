# Contributor: Andrea Scarpino <andrea@archlinux.org>
# Contributor: Pierre Schmitz <pierre@archlinux.de>

pkgname=kopete-cryptography
pkgver=1.3.0
_kdever=4.3.3
pkgrel=5
pkgdesc="Kopete plugin which encrypts and signs messages using OpenPGP"
arch=('i686' 'x86_64')
url='http://www.kde.org'
license=('GPL')
depends=('kdenetwork-kopete' 'kdepim-libkdepim')
makedepends=('pkgconfig' 'cmake' 'automoc4')
options=('docs')
source=("http://download.kde.org/stable/${_kdever}/src/extragear/${pkgname}-${pkgver}-kde${_kdever}.tar.bz2")
md5sums=('609f72a0884941bbefcd331de7c9f939')

build() {
	cd $srcdir
	mkdir build
	cd build
	cmake ../${pkgname}-${pkgver}-kde${_kdever} \
		-DCMAKE_BUILD_TYPE=Release \
		-DCMAKE_INSTALL_PREFIX=/usr
	make || return 1
	make DESTDIR=$pkgdir install || return 1
}
