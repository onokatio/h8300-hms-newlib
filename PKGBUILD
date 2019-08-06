# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=h8300-hms-newlib
pkgver=1.19.0
pkgrel=1
pkgdesc="h8300 hms newlib libc"
arch=('x86_64')
url=""
license=('GPL')
groups=()
depends=('gcc-h8300-hms-nolibc')
makedepends=()
install=
source=("https://sourceware.org/pub/newlib/newlib-$pkgver.tar.gz")
md5sums=(SKIP)

build() {
	cd $srcdir/newlib-$pkgver
	export CFLAGS=""
	./configure --target h8300-hitachi-coff --prefix=/usr
	make
}
package() {
	cd $srcdir/newlib-$pkgver
	make DESTDIR="$pkgdir" install
}
