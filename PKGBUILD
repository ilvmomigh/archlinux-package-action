pkgname=proycon-wayout
pkgver=0.1.5
pkgrel=1
pkgdesc='Output simple text to a Wayland desktop widget'
arch=('x86_64')
url='https://git.sr.ht/~proycon/wayout'
license=('GPL-3.0-or-later')
depends=('cairo' 'pango' 'wayland')
makedepends=('meson' 'ninja' 'scdoc' 'wayland-protocols')
source=("https://git.sr.ht/~proycon/wayout/archive/${pkgver}.tar.gz")
sha256sums=('SKIP')

build() {
    CFLAGS="${CFLAGS} -Wno-error=unused-result"
    meson build "${srcdir}/wayout-${pkgver}" \
        --prefix=/usr \
        --buildtype=release
    ninja -C build
}

package() {
     DESTDIR="$pkgdir" ninja -C build install
}
