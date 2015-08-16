# Maintainer:   MayKiller <imaykiller+aur at gmail dot com>
# Contributor:  fresh24 <pascher dot christian at gmail dot com>
#               Veeti Paananen <veeti.paananen@rojekti.fi>

pkgname=gtk-theme-elementary-for-3-14
pkgver=r444
pkgrel=1
pkgdesc="Development branch of the elementary GTK theme for GNOME 3.14 and later."
arch=('i686' 'x86_64')
url="https://code.launchpad.net/~elementary-design/egtk/3-14"
license=('GPL2')
depends=('gtk-engine-murrine' 'gtk-engine-unico')
optdepends=('elementary-icons')
makedepends=('bzr')
conflicts=('elementary-gtk-theme' 'gtk-theme-elementary' 'gtk-theme-elementary-bzr')

_bzrmod='3-14'
source=('bzr+lp:~elementary-design/egtk/3-14')
md5sums=('SKIP')

package() {
    cd ${_bzrmod}

    mkdir -p ${pkgdir}/usr/share/themes/elementary/
    cp -r gtk-2.0 ${pkgdir}/usr/share/themes/elementary/
    cp -r gtk-3.0 ${pkgdir}/usr/share/themes/elementary/
    cp -r metacity-1 ${pkgdir}/usr/share/themes/elementary/

    find ${pkgdir}/usr/share/themes/elementary/ -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/themes/elementary/ -type d -exec chmod 755 {} \;

    install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
