pkgname='bootsplash-theme-bgrt'
pkgver=0.2
pkgrel=1
pkgdesc="BGRT bootsplash theme"
url="https://github.com/t1meshift/bootsplash-theme-bgrt"
arch=('x86_64')
license=('GPL')

optdepends=('bootsplash-systemd: for bootsplash functionality')
makedepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-bgrt.sh'
	'bootsplash-bgrt.initcpio_install'
	'spinner.gif')

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP')

prepare() {
  echo "Checking for BGRT..."
  if [ ! -f "/sys/firmware/acpi/bgrt/version" ]
  then
    echo "BGRT not found, aborting..."
    exit 1
  fi
}

build() {
  cd "$srcdir"
  sh ./bootsplash-bgrt.sh
}

package() {
  cd "$srcdir"
  install -Dm644 "$srcdir/bootsplash-bgrt" "$pkgdir/usr/lib/firmware/bootsplash-themes/bgrt/bootsplash"
  install -Dm644 "$srcdir/bootsplash-bgrt.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-bgrt"
} 
