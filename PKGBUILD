# Maintainer: Thomas Bosley <tbosley@limbofps.net>
pkgname=pacgraph
pkgver=20240320
pkgrel=1
pkgdesc="Draws a graph of installed packages to PNG/SVG/GUI/console.  Good for finding bloat."
arch=('any')
url="https://github.com/keenerd/pacgraph"
license=('GPL')
depends=('python')
makedepends=()
optdepends=('inkscape: png backend'
            'imagemagick: png backend'
            'tk: gui version')
source=(https://github.com/StuckInLimbo/pacgraph/releases/download/$pkgver/$pkgname.tar.gz)
md5sums=('277a4aaa027b63efbdfe50f251b5a83e')
sha256sums=('471cbba6eb9c8153f43e7d078d8dab38ecd67f8742307a969ae1c7ad1fa7b454')

package() {
  cd "$srcdir"
  install -D -m 0755 pacgraph    "$pkgdir/usr/bin/pacgraph"
  install -D -m 0755 pacgraph-tk "$pkgdir/usr/bin/pacgraph-tk"
  install -Dm644     $pkgname.1  "$pkgdir/usr/share/man/man1/$pkgname.1"
}