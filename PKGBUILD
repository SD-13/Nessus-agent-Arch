# Maintainer: noraj <printf %s 'YWxleGFuZHJlLnphbm5pQGV1cm9wZS5jb20='|base64 -d>
# Contributor: neale

pkgname=nessus-agent
_pkgname=nessus_agent
pkgver=10.7.3
pkgrel=1
pkgdesc="Nessus vulnerability scanner agent"
arch=('x86_64')
depends=('gnupg')
makedepends=('inetutils')
license=('custom')
options=(!strip debug)
url="https://www.tenable.com/downloads/nessus-agents"
install="$pkgname.install"
source=("~/Downloads/NessusAgent-10.8.0-fc38.x86_64.rpm"        LICENSE)

package() {
  mkdir -p "$pkgdir/etc/ld.so.conf.d" "$pkgdir/usr/share" "$pkgdir/opt/$pkgname" \
           "$pkgdir/usr/lib"

  cp -a usr/lib "$pkgdir/usr"

  # path to libraries
  echo /opt/${_pkgname}/lib > "$pkgdir/etc/ld.so.conf.d/nessus.conf"

  # main files
  cp -a opt/${_pkgname}/{bin,com,etc,lib,sbin,var} "$pkgdir/opt/$pkgname"

  # license
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

