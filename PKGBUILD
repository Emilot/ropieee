# Maintainer: Harry ten Berge <htenberge@gmail.com>

pkgname=ropieee
pkgver=2
pkgrel=7
arch=(any)
url="http://www.kernel.org/"
license=('MIT')
install=${pkgname}.install



package() {
echo "package"

   install -d "${pkgdir}/boot/RoPieee"

   install -m0644 "../RoPieee/99-blacklist.conf"                    "${pkgdir}/boot/RoPieee"
   install -m0755 "../RoPieee/SETUP"                                "${pkgdir}/boot/RoPieee"
   install -m0644 "../RoPieee/alsa-base.conf"                       "${pkgdir}/boot/RoPieee"
   install -m0755 "../RoPieee/bootstrap"                            "${pkgdir}/boot/RoPieee"
   install -m0644 "../RoPieee/fstab"                                "${pkgdir}/boot/RoPieee"
   install -m0644 "../RoPieee/journald.conf"                        "${pkgdir}/boot/RoPieee"
   install -m0755 "../RoPieee/roonbridge-installer-linuxarmv7hf.sh" "${pkgdir}/boot/RoPieee"
   install -m0644 "../RoPieee/ropieee.conf"                         "${pkgdir}/boot/RoPieee"
   install -m0644 "../RoPieee/sshd_config"                          "${pkgdir}/boot/RoPieee"
   install -m0755 "../RoPieee/run-updates"                          "${pkgdir}/boot/RoPieee"
}


