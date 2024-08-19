# https://gitlab.archlinux.org/archlinux/packaging/packages/nsxiv/-/blob/main/PKGBUILD

pkgname=nsxiv
pkgver=32_g0ddf4944
pkgrel=1
pkgdesc='Neo (or New or Not) Simple (or Small or Suckless) X Image Viewer'
arch=('x86_64')
license=('GPL-2.0-or-later')
url='https://nsxiv.codeberg.page/'

depends=(
  'glibc'
  'imlib2' 'libx11'                 # core dependencies
  'libxft' 'fontconfig' 'freetype2' # status bar
  'libexif'                         # display exif images
  'hicolor-icon-theme'              # make icon
)

build() {
  cd "$startdir"
  make HAVE_INOTIFY=1 HAVE_LIBFONT=1 HAVE_LIBEXIF=1
}

package() {
  cd "$startdir"
  sudo make PREFIX=/usr/local install
}
