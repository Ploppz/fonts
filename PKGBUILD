pkgname=uushi-font
pkgver=1.0
pkgrel=1
pkgdesc="A font made by phallus the features extra unicode characters."
pkgurl="https://github.com/phallus/fonts"
arch=('any')
depends=('fontconfig' 'xorg-font-utils')
source=("git+https://github.com/phallus/fonts.git")
md5sums=('SKIP')
install="$pkgname.install"

build() {
	bdftopcf -o "$srcdir/uushi.pcf" "$srcdir/fonts/uushi.bdf"
}

package() {
  install -d "$pkgdir/usr/share/fonts/misc"
  cp -dpr --no-preserve=ownership "$srcdir/uushi.pcf" "$pkgdir/usr/share/fonts/misc/"
}
