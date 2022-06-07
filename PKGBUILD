# Maintainer: yarob-0
pkgname=st
pkgrel=1
pkgver=0.8.5
pkgdesc="A fully patched sucless simple terminal"
arch=('x86_64' 'i686')
url="https://github.com/yarob-0/st"
privides=('st')
conflicts=('st')
license=('MIT')
makedepends=('make' 'git')
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
