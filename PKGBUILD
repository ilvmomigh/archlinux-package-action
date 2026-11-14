pkgname=ld-icons-rs
pkgver=0.1.0 # set to upstream version (or use -git, see note below)
pkgrel=1
pkgdesc="Lightweight Wayland desktop-icons service for wlroots-based compositors"
arch=('x86_64' 'aarch64')
url="https://github.com/iHarryPotter178/ld-icons-rs"
license=('GPL-3.0-or-later')
depends=()
makedepends=('rust' 'cargo')
source=("https://github.com/iHarryPotter178/ld-icons-rs/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('SKIP') # run makepkg -g and replace after first download

build() {
  cd "$srcdir/ld-icons-rs-${pkgver}"
  cargo build --release --locked
}

package() {
  cd "$srcdir/ld-icons-rs-${pkgver}"
  install -Dm755 target/release/ld-icons-rs "$pkgdir/usr/bin/ld-icons-rs"
}
