pkgname=cambonos-installer
pkgver=0.2.3
pkgrel=2
pkgdesc="CambonOS live system installer"
arch=('any')
url="https://github.com/CambonOS/cambonos-installer"
license=('GPL-3.0-only')
depends=('arch-install-scripts' 'bash' 'coreutils' 'curl' 'dialog' 'dosfstools'
         'e2fsprogs' 'gawk' 'networkmanager' 'pacman' 'parted' 'pciutils' 'reflector'
         'systemd' 'util-linux')

package() {
  local version_file="$pkgdir/usr/share/cambonos-installer/version"

  install -Dm644 "$startdir/LICENSE" \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  install -Dm755 "$startdir/files/cambonos-installer" \
    "$pkgdir/usr/bin/cambonos-installer"
  install -d "$pkgdir/usr/share/cambonos-installer"
  printf '%s-%s\n' "$pkgver" "$pkgrel" > "$version_file"
}