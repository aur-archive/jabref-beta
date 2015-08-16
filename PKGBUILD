# forked from 'jabref' package
# Maintainer: Alexey Stukalov <astukalov@gmail.com>
# Contributor: Allan McRae <allan@archlinux.org>
# Contributor: Christian Storm <Christian.Storm@gmx.de>

pkgname=jabref-beta
_pkgname=jabref
pkgver=2.10b3
pkgrel=1
pkgdesc="GUI frontend for BibTeX, written in Java. Beta series"
arch=('any')
url="http://jabref.sourceforge.net/"
license=('GPL')
depends=('java-runtime')
conflicts=('jabref')
source=(http://downloads.sourceforge.net/${_pkgname}/JabRef-${pkgver}.jar
        jabref.sh
        jabref.desktop)
md5sums=('2d2f9462dfcc4474ccecc33678e1bb50'
         'f8d196651863fe9d961d3f7ecda06936'
         '496d2094ee194a5568baee7af5b70fa2')

build() {
  cd ${srcdir}
  install -Dm755 JabRef-${pkgver}.jar ${pkgdir}/usr/share/java/${_pkgname}/JabRef-${pkgver}.jar
  install -Dm755 ${_pkgname}.sh ${pkgdir}/usr/bin/${_pkgname}
  sed -i "s/VERSION/${pkgver}/" ${pkgdir}/usr/bin/${_pkgname}
  install -Dm644 ${_pkgname}.desktop ${pkgdir}/usr/share/applications/${_pkgname}.desktop
  install -Dm644 images/JabRef-icon-48.png ${pkgdir}/usr/share/pixmaps/${_pkgname}.png
}
