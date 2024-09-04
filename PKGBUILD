# Maintainer: Vitalij Berdinskih <vitalij_r2@outlook.com>

pkgname=swayshot 
pkgver=2.7.4
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
sha256sums=('84a0b6881ab687bcde4eb3b567c1d664b5aaf9391df9f6903581ee70d5c4bcd7')

package() {
	cd "$srcdir"/$pkgname-$pkgver

	install -d "$pkgdir"/etc/sway/config.d
	install -m 644 $pkgname.conf "$pkgdir"/etc/sway/config.d
	install -d "$pkgdir"/usr/bin
	install -m 755 $pkgname.sh "$pkgdir"/usr/bin/$pkgname
}
