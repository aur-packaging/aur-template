# Maintainer: <Name of maintainer> <email>

pkgname=name-of-package
pkgver=v0.1.0
pkgrel=1
pkgdesc="Some description"

arch=("any") #or x86_64 or any architectures that might support
url="https://github.com/user/package"
depends=("dependencies", "dependencies2")

provides=("${pkgname}")
conflicts=("${pkgname}")

license=('MIT')
md5sums=("SKIP") #or md5sums of provides
source("${url}/releases/download/v${_pkgver/${pkgname}_x86_64.tar.gz}" "${pkgname}")

package() {
	cd "${pkgname%-git}"
	install -Dm755 "${srcdir}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
	install -D -t "$pkgdir/usr/bin" "$srcdir/${pkgname}"
}

