# Maintainer: yarob-0
pkgname=st
pkgrel=1
pkgver=0.8.5
pkgdesc="A fully patched sucless simple terminal"
arch=('any')
url="https://github.com/yarob-0/st"
license=('MIT')
makedepends=('make')
source=("git+${url}.git#branch=main")
md5sums=('SKIP')
validpgpkeys=()

build() {
	cd "$pkgname"
	make
}

pkgver() {
	cd "${pkgname%}"
	printf "0.8.5.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$pkgname"
	make DESTDIR="$pkgdir/" install
}
