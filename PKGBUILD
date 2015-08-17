# Maintainer: xylosper <darklin20@gmail.com>

pkgname=('okular-backend-mupdf')
pkgver=0.0.5
pkgrel=1
pkgdesc="MuPDF-based backend for Okular"
arch=('i686' 'x86_64')
license=('GPL')
depends=('kdegraphics-okular' 'openjpeg2' 'mupdf')
makedepends=('gcc' 'automoc4' 'cmake')
url='https://github.com/xylosper/okular-backend-mupdf'
source=("$url/archive/v$pkgver.tar.gz")
md5sums=('SKIP')

build() {
    cd $srcdir/$pkgname-$pkgver
    rm -rf build
    mkdir build && cd build
    cmake -DCMAKE_INSTALL_PREFIX:PATH=$pkgdir/usr .. && make -j$(nproc)
}

package() {
    cd $srcdir/$pkgname-$pkgver/build
    make install
}
