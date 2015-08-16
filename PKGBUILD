# Maintainer:  Nyarcel  <nyarcel AT SPAMFREE gmail DOT com>
#
# PKGBUILD revision: 2014-03-17

pkgname=libsocketcan
pkgver=0.0.9
pkgrel=1
pkgdesc='Allows you to control some basic functions in SocketCAN from userspace'
arch=('i686' 'x86_64')
url="http://www.pengutronix.de/software/$pkgname/download/"
license=('LGPLv2')
source_url=$url
source=("$source_url/$pkgname-$pkgver.tar.bz2")
md5sums=('cd92766be40d98b5cb08366b71ea4663')

build() {
	cd "$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
