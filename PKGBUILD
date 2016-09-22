pkgname=pwgen
pkgver=2.07
pkgrel=1
pkgdesc='Password generator for creating easily memorable passwords'
arch=('x86_64')
url='http://sourceforge.net/projects/pwgen/'
license=('GPL')
depends=('glibc')
source=("http://downloads.sourceforge.net/sourceforge/pwgen/$pkgname-$pkgver.tar.gz")
sha256sums=('eb74593f58296c21c71cd07933e070492e9222b79cedf81d1a02ce09c0e11556')

prepare() {
  cd "$pkgname-$pkgver"
  autoconf
}

build() {
  cd "$pkgname-$pkgver"
  ./configure --prefix=/usr --mandir=/usr/share/man
  make
}

package() {
  make -C "$pkgname-$pkgver" DESTDIR="$pkgdir" install
} 
