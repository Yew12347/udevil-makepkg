pkgname=udevil-git
pkgver=0.4.4
pkgrel=1
arch=('x86_64')
license=('GPL3')
depends=('udev' 'glib2')
makedepends=('git' 'intltool' 'gettext')

source=("$pkgname::git+https://github.com/Yew12347/udevil-arch.git")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  chmod +x ./configure
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" install
}
