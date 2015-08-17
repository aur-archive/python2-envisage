# Maintainer: Andrzej Giniewicz <gginiu@gmail.com>
pkgname=python2-envisage
pkgver=4.2.0
_githubtag=a326011
pkgrel=1
pkgdesc="Extensible Application Framework"
arch=('any')
url="https://github.com/enthought/envisage"
license=('BSD')
depends=('python2-apptools' 'python2-traits')
makedepends=('python2-distribute')
conflicts=('python2-envisage-git')
options=(!emptydirs)

source=("https://github.com/enthought/envisage/tarball/${pkgver}")
md5sums=('65a2a31be206abc8ce8f6afaaf4b9234')

build() {
  cd "$srcdir/enthought-envisage-${_githubtag}"

  python2 setup.py build
}

package() {
  cd "$srcdir/enthought-envisage-${_githubtag}"

  python2 setup.py install --root="$pkgdir"/ --optimize=1

  install -D "LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

