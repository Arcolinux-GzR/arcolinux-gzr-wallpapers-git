# Maintainer: Erik Dubois <erik.dubois@gmail.com>
# GzR-Maintainer: John Brewer <nytesblood@gmail.com>
pkgname=arcolinux-gzr-wallpapers-git
_pkgname=arcolinux-gzr-wallpapers
_destname="/usr/share/"
_licensedir="/usr/share/arcolinux/licenses/"
pkgver=6.7
pkgrel=1
pkgdesc="Wallpapers for Arco-GzR"
arch=('any')
url="https://github.com/Arcolinux-GzR/arcolinux-gzr-wallpapers"
license=('GPL3')
makedepends=('git')
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${_pkgname}::"git+https://github.com/Arcolinux-GzR/${_pkgname}.git")
sha256sums=('SKIP')
package() {
	rm -f "${srcdir}/${_pkgname}/"README.md
	rm -f "${srcdir}/${_pkgname}/"git-v*
	mkdir -p "${pkgdir}${_destname}"
	mkdir -p "${pkgdir}${_licensedir}${_pkgname}"
	mv "${srcdir}/${_pkgname}/"LICENSE "${pkgdir}${_licensedir}${_pkgname}/LICENSE"
	cp -r "${srcdir}/${_pkgname}/"* "${pkgdir}${_destname}"
}
