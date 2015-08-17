# Contributor: Andrea Scarpino <andrea@archlinux.org>

pkgname=phonon-xine
pkgver=4.4.4
pkgrel=1
arch=('i686' 'x86_64')
url="http://phonon.kde.org"
pkgdesc="Phonon Xine backend"
license=('LGPL')
depends=('xine-lib')
makedepends=('cmake' 'automoc4' 'phonon')
provides=('phonon-backend')
source=("http://download.kde.org/stable/phonon/phonon-backend-xine/${pkgver}/src/phonon-backend-xine-${pkgver}.tar.bz2")
md5sums=('b127104e67538e573adeed3b2fb3bf55')

build() {
  cd ${srcdir}
  mkdir build
  cd build
  cmake ../phonon-backend-xine-${pkgver} \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd ${srcdir}/build
  make DESTDIR=${pkgdir} install
}
