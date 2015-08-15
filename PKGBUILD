# Maintainer:  TDY <tdy@archlinux.info>
# Contributor: Nathan Owe <ndowens04 at gmail>

pkgname=crip
pkgver=3.9
pkgrel=2
pkgdesc="A terminal-based ripper/encoder/tagger tool for creating Ogg Vorbis/FLAC/MP3 files"
arch=('any')
url="http://bach.dynet.com/crip/"
license=('GPL')
depends=('cddb_get' 'cdparanoia' 'flac' 'perl' 'sox' 'vorbisgain' 'vorbis-tools')
install=crip.install
source=(http://bach.dynet.com/crip/src/$pkgname-$pkgver.tar.gz)
md5sums=('dcb5b9d034c100987301276a2973f74d')

package() {
  cd "$srcdir/$pkgname-$pkgver"

  #install -Dm644 CDDB_get.pm "$pkgdir/usr/share/perl5/vendor_perl/CDDB_get.pm"
  install -Dm755 $pkgname "$pkgdir/usr/share/$pkgname/$pkgname"
  install -cm644 criprc_example "$pkgdir/usr/share/$pkgname/criprc_example"
  install -cm644 editfilenames "$pkgdir/usr/share/$pkgname/editfilenames"
  install -cm644 editcomment "$pkgdir/usr/share/$pkgname/editcomment"

  install -dm755 "$pkgdir/usr/bin"
  ln -sf /usr/share/$pkgname/$pkgname "$pkgdir/usr/bin/$pkgname"
}

# vim:set ts=2 sw=2 et:
