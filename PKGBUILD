# Maintainer: iyamnabeen <iym.nabeen@gmail.com>

pkgname=metis-slstatus
_pkgname=metis-slstatus
pkgver=r543.8de15fb
pkgrel=2
pkgdesc='A status monitor for @metis-os'
arch=('i686' 'x86_64')
url='https://github,com/metis-os/metis-slstatus'
depends=('libx11' 'alsa-lib')
makedepends=('git')
source=("git+https://github.com/metis-os/metis-slstatus")
md5sums=(SKIP)

build() {
  cd "${_pkgname}"
  make X11INC='/usr/include/X11' X11LIB='/usr/lib/X11'
}

package() {
  cd "${_pkgname}"
  make DESTDIR="${pkgdir}" PREFIX='/usr/' install

  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${_pkgname}/LICENSE"
}
