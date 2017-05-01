# Maintainer: Harry ten Berge <htenberge@gmail.com>

pkgname=ropieee
pkgver=5
pkgrel=1
arch=(any)
url="https://github.com/RoPieee/"
license=('MIT')
install=${pkgname}.install



package() {
echo "package"

   install -d "${pkgdir}/boot/RoPieee"
   install -d "${pkgdir}/opt/RoPieee/sbin"
   install -d "${pkgdir}/opt/RoPieee/conf"
   install -d "${pkgdir}/opt/RoPieee/lib"

   install -m0755 "../ropieee/SETUP"                                "${pkgdir}/boot/RoPieee"
   install -m0755 "../ropieee/bootstrap"                            "${pkgdir}/boot/RoPieee"

   install -m0644 "../ropieee/99-blacklist.conf"                    "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/alsa-base.conf"                       "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/fstab"                                "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/journald.conf"                        "${pkgdir}/opt/RoPieee/conf"
   install -m0755 "../ropieee/roonbridge-installer-linuxarmv7hf.sh" "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/ropieee.conf"                         "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/rescue.service"                       "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/sshd_config"                          "${pkgdir}/opt/RoPieee/conf"

   install -m0755 "../ropieee/run-updates"                          "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../ropieee/configure"                            "${pkgdir}/opt/RoPieee/sbin"

   install -m0755 "../ropieee/lib/*"                                "${pkgdir}/opt/RoPieee/lib"
}

