# Maintainer: Vitalij Berdinskih <vitalij_r2@outlook.com>

pkgname=swayshot 
pkgver=2.7.3
pkgrel=5
pkgdesc="Sway screenshots: screen, window or region. Also it uploads them to 0x0.st."
arch=("any")
url="https://github.com/vitalijr2/swayshot"
license=('GPL3')
depends=('sway' 'xdg-user-dirs' 'grim' 'slurp' 'jq')
optdepends=('wl-clipboard: copy the full path to clipboard'
	'xsel: copy the full path to clipboard'
	'xclip: copy the full path to clipboard'
	'curl: upload a screenshot to x0.at'
	'libnotify: show message with path or URL')
conflicts=('swaygrab-helper')
backup=(etc/sway/config.d/swayshot.conf)
source=("https://github.com/vitalijr2/$pkgname/archive/refs/tags/$pkgver.tar.gz")
md5sums=('2434abe6b62780e4466226db3de35b99')
sha256sums=('a9cd5b4b9741fd10c350d905c8e0a0449637c3f322febcdf09f7000c2aeba1f2')

package() {
	cd "$srcdir"/$pkgname-$pkgver

	install -d "$pkgdir"/etc/sway/config.d
	install -m 644 $pkgname.conf "$pkgdir"/etc/sway/config.d
	install -d "$pkgdir"/usr/bin
	install -m 755 $pkgname.sh "$pkgdir"/usr/bin/$pkgname
}
