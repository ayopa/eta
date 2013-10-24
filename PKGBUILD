pkgname=eta
pkgver=1
pkgrel=1
pkgdesc="Agora build system"
arch=('i686' 'x86_64')
url="https"
license=('LGPL')
depends=('systemd')
makedepends=('git' 'gtk-doc')
source=("eta-build")
md5sums=('SKIP')

package() {
    install -D -m755 ${srcdir}/eta-build ${pkgdir}/usr/bin/eta-build
}
