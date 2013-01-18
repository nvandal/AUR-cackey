pkgname=cackey
pkgver=0.6.8
pkgrel=1
pkgdesc="Goverment Smartcard PKCS#11 Provider"
arch=('i686' 'x86_64')
url="https://software.forge.mil/sf/frs/do/listReleases/projects.community_cac/frs.cackey"
license=('unkown')
depends=('pcsclite')
makedepends=('git' 'perl')
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=('cackey-0.6.8.tar.gz')
md5sums=('ceab45f9d1c80ee0ffdbc4e45e553d0e')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    ./configure --prefix=/usr
    make
}

check() {
    cd "$srcdir/$pkgname-$pkgver"
    make -k test
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
