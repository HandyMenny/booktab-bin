# Maintainer: HandyMenny <handymenny[at]outlook[dot]com>
pkgname=booktab-bin
s_pkgname=booktab
pkgver=1.8
pkgrel=3
pkgdesc="BooktabZ book reader"
arch=('x86_64')
depends=('gstreamer0.10-base-plugins')
install="${pkgname}.install"
license=('custom:"Copyright: 2017 duDAT Srl"')
url="https://booktab.it/"
source=("https://booktab.it/setup-z/BooktabZSetup-16.04.deb")
sha256sums=('SKIP')

package() {
	tar -zxf data.tar.gz -C "${pkgdir}"	
	sed -e 9a'Categories=Viewer;Literature;Education' ${pkgdir}/usr/share/applications/${s_pkgname}.desktop > ${pkgdir}/usr/share/applications/${pkgname}.desktop
	rm ${pkgdir}/usr/share/applications/{${s_pkgname},${s_pkgname}z}.desktop
	chmod 755 ${pkgdir}/usr/{,bin,share/{,applications}}
}
