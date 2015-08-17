#Contributor: Dominik Fuchs <dominik.fuchs@wur.nl>

pkgname=ranalyticflow
pkgver=2.1.0
pkgrel=1
pkgdesc="Statistical analysis flowchart software, based on R"
url="http://www.ef-prime.com/products/ranalyticflow_en/"
license=(custom)
arch=('any')
depends=('r' 'java-runtime' 'r-rjava')
optdepends=()
install="$pkgname.install"
source=(http://download.ef-prime.com/ranalyticflow/$pkgver/bin/RAnalyticFlow_Linux_$pkgver.tar.gz
	ranalyticflow.png
	ranalyticflow.desktop)
md5sums=('ab78fb85fbf2fa240f01a724da5be91e'
         '2b5b1defcdcc8403068c4f7758f109da'
         '6d0d32000cec5e2ef650924483db4e65')

package() {
  cd $srcdir
  mkdir -p $pkgdir/usr/share/applications $pkgdir/usr/share/pixmaps $pkgdir/opt $pkgdir/usr/bin
  install -D -m644 ranalyticflow.png $pkgdir/usr/share/pixmaps
  install -D -m644 ranalyticflow.desktop $pkgdir/usr/share/applications
  cp -R RAnalyticFlow_${pkgver} $pkgdir/opt/ranalyticflow
  install -D -m644 $srcdir/RAnalyticFlow_${pkgver}/license.txt $pkgdir/usr/share/licenses/${pkgname}/License.txt
#  ln -sf /opt/ranalyticflow/rflow $pkgdir/usr/bin/rflow
}
