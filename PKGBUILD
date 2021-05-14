# Maintainer: Nev Delap <nevdelap at gmail dot com>
pkgname="ned-bin"
pkgver="1.3.3"
pkgrel=1
pkgdesc="Like grep but with a powerful replace, unlike sed, it's not only line oriented."
arch=("x86_64")
url="https://github.com/nevdelap/ned"
license=("GPL3")
makedepends=()
source=(
	"https://github.com/nevdelap/ned/releases/download/release.$pkgver/ned.64-bit.musl.linux.gz"
	"https://github.com/nevdelap/ned/releases/download/release.$pkgver/ned.1.gz"
)
md5sums=('6823b1880bb8b03fb41e962acd075d85'
         'f15b49bea15473e0c503ae9bc3ce1994')

build() {
	mv ned.64-bit.musl.linux ned
}

check() {
	test -f ned && test -f ned.1.gz
}

package() {
	install -Dm755 ned "$pkgdir/usr/bin/ned" && \
	install -Dm 0644 ned.1.gz "$pkgdir/usr/share/man/man1/ned.1.gz"
}
