# Maintainer: iyamnabeen 
# gmail:  <iym.nabeen@gmail.com>
# github: <github.com/iyamnabeen>

pkgname=metis-slstatus
pkgver=1.3
pkgrel=5
pkgdesc="slstatus for metis-os"
url="https://github.com/metis-os/metis-slstatus"
arch=('any')
license=('GPL3')
options=(zipman)
depends=('libx11' 'libxinerama' 'libxft' 'alsa-utils' 
)
conflicts=('slstatus')
provides=("${pkgname}")
options=(!strip !emptydirs)
install="${pkgname}.install"

prepare() {
	cp -af ../source/. ${srcdir}
}

build() {
  cd "$srcdir"
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11 FREETYPEINC=/usr/include/freetype2
}

package() {
  cd "$srcdir"
  make PREFIX=/usr DESTDIR="$pkgdir" install

}
