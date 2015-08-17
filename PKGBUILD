# Maintainer: Madura A <madura.x86@gmail.com>
# If you use PulseAudio change CONFIG+=Alsa to CONFIG+=PulseAudio
# or if you use some other audio server you can try CONFIG+=Ao

pkgname=vrok-git
pkgver=20140227
pkgrel=1
pkgdesc="A light weight audio player (Edit PKGBUILD to build for PulseAudio, builds for Alsa by default)"
arch=('i686' 'x86_64')
url="http://0xdeafc0de.wordpress.com/vrok/"
license=('GPL')
groups=()
depends=('mpg123' 'flac' 'ffmpeg>=2.1.1' 'libogg' 'qt4' 'curl')
makedepends=('git')
optdepends=()
provides=('vrok')
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(git://github.com/manushanga/vrok.git)
noextract=()
md5sums=('SKIP')

build() {
  cd "$srcdir/vrok"
  ## change below if you use PulseAudio
  qmake-qt4 CONFIG+=Alsa CONFIG+=RELEASE
  make
}

package() {
  cd "$srcdir/vrok"
  mkdir -p $pkgdir/usr/bin
  mkdir -p $pkgdir/usr/share/vrok
  mkdir -p $pkgdir/usr/share/applications
  cp vrok $pkgdir/usr/bin/vrok
  cp res/vrok.png $pkgdir/usr/share/vrok/
  cp vrok.desktop $pkgdir/usr/share/applications
}
