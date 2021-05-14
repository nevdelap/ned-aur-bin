# Maintainer: Nev Delap <nevdelap at gmail dot com>
pkgname="ned-bin"
pkgver="1.2.9"
pkgrel=1
pkgdesc="Like grep but with a powerful replace, unlike sed, it's not only line oriented."
arch=("x86_64")
url="https://github.com/nevdelap/ned"
license=("GPL3")
makedepends=()
source=("$pkgname-$pkgver.tar.gz::https://github.com/nevdelap/ned/releases/download/release.$pkgver/ned.64-bit.musl.linux.tar.gz")
md5sums=('4e4b1f1bd1d2a9b84589f17eb2e82d95')

build() {
	tar xf ned-bin-1.2.9.tar.gz
}

check() {
	test -f ned && test -f ned.1.gz
}

package() {
	install -Dm755 ned "$pkgdir/usr/bin/ned" && \
	install -Dm 0644 ned.1.gz "$pkgdir/usr/share/man/man1/ned.1.gz"
}
