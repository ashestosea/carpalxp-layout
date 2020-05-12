# Maintainer: Damian Geerdes <damian.geerdes@tutanota.com>
pkgname=carpalxp-layout
pkgver=r2.3834801
pkgrel=1
pkgdesc="Carpalx keyboard layout merged with the Programmer parts of Programmer Dvorak"
arch=(any)
url="https://github.com/chronotab/carpalxp-layout"
source=("git+$url.git")
license=(GPL3)
makedepends=(git)
md5sums=('SKIP')

pkgver() {
	cd "$pkgname"
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd "$srcdir/$pkgname"
	gzip -c carpalxp.map > carpalxp.map.gz
	install -Dm 644 carpalxp.map.gz "$pkgdir/usr/share/kbd/keymaps/i386/carpalx/carpalxp.map.gz"
	install -Dm 644 carpalxp "$pkgdir/usr/share/X11/xkb/symbols/carpalxp"
}
