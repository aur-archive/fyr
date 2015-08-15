# Maintainer: ninian <mcfadzean.org.uk ta linux>

pkgname=fyr
pkgver=4.1.0
pkgrel=2
pkgdesc="Manages menus of application launchers, either executables or desktop files. Also opens files and URIs with launchers, desktop files, or applications associated by MIME-type."
arch=('any')
url="http://appstogo.mcfadzean.org.uk/linux.html#fyr"
license=('MIT')
depends=('bash' 'dmenu' 'libnotify' 'file')
optdepends=('perl-file-mimeinfo: for better MIME-type determination' 'gxmessage: for previewing application file')
install=$pkgname.install
source=("http://appstogo.mcfadzean.org.uk/dl/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('27e704d95e85ad9297e157eb10213b7b')

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 $pkgname               "$pkgdir/usr/bin/$pkgname"
  install -Dm644 $pkgname.png           "$pkgdir/usr/share/pixmaps/$pkgname.png"
  install -Dm644 $pkgname.desktop       "$pkgdir/usr/share/applications/$pkgname.desktop"
  install -Dm644 $pkgname-exec.desktop  "$pkgdir/usr/share/applications/$pkgname-exec.desktop"
  install -Dm644 LICENSE                "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -Dm644 config                 "$pkgdir/usr/share/doc/$pkgname/config"
  install -Dm644 README                 "$pkgdir/usr/share/doc/$pkgname/README"
  install -Dm644 CHANGELOG              "$pkgdir/usr/share/doc/$pkgname/CHANGELOG"
  install -Dm644 dudo                   "$pkgdir/usr/share/doc/$pkgname/dudo"
  install -Dm644 xdg-open               "$pkgdir/usr/share/doc/$pkgname/xdg-open"
  msg "Copy sample configuration file /usr/share/doc/$pkgname/config and customize per user"
}
