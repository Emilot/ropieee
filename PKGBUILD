# Maintainer: Harry ten Berge <htenberge@gmail.com>

pkgname=ropieee
pkgver=3
pkgrel=4
arch=(any)
url="http://www.kernel.org/"
license=('MIT')
install=${pkgname}.install



package() {
echo "package"

   install -d "${pkgdir}/boot/RoPieee"
   install -d "${pkgdir}/opt/RoPieee/sbin"
   install -d "${pkgdir}/opt/RoPieee/conf"

   install -m0755 "../RoPieee/SETUP"                                "${pkgdir}/boot/RoPieee"
   install -m0755 "../RoPieee/bootstrap"                            "${pkgdir}/boot/RoPieee"

   install -m0644 "../RoPieee/99-blacklist.conf"                    "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../RoPieee/alsa-base.conf"                       "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../RoPieee/fstab"                                "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../RoPieee/journald.conf"                        "${pkgdir}/opt/RoPieee/conf"
   install -m0755 "../RoPieee/roonbridge-installer-linuxarmv7hf.sh" "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../RoPieee/ropieee.conf"                         "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../RoPieee/rescue.service"                       "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../RoPieee/sshd_config"                          "${pkgdir}/opt/RoPieee/conf"

   install -m0755 "../RoPieee/run-updates"                          "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../RoPieee/configure"                            "${pkgdir}/opt/RoPieee/sbin"
}

