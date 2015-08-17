# Maintainer: xerc <aur[at]xerc.de>
# Contributor: Nathan Owe <ndowens.aur[at]gmail.com>

pkgname=toast
pkgver=1.484
pkgrel=2

pkgdesc="A simple, self-contained tool for managing software packages."
url="http://www.toastball.net/toast/"
license=('GPL')
arch=('any')

depends=('sh' 'perl')
optdepends=('wget')

source=(http://www.toastball.net/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('b66e07cd2839177cb644455cc42be3ca')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
