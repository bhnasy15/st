# Maintainer: yarob-0
pkgname=st
pkgrel=1
pkgver=r25.8f4faf1
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
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$pkgname"
	make DESTDIR="$pkgdir/" install
}
