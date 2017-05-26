# Maintainer: Harry ten Berge <htenberge@gmail.com>

pkgname=ropieee
pkgver=20170526
pkgrel=1
arch=(any)
url="https://github.com/RoPieee/"
license=('MIT')
depends=('usleep')
install=${pkgname}.install



package() {
echo "package"

   install -d "${pkgdir}/boot/RoPieee"
   install -d "${pkgdir}/opt/RoPieee/sbin"
   install -d "${pkgdir}/opt/RoPieee/conf"
   install -d "${pkgdir}/opt/RoPieee/lib"
   install -d "${pkgdir}/etc/systemd/system"

   install -m0755 "../ropieee/bootstrap"                            "${pkgdir}/boot/RoPieee"
   install -m0755 "../ropieee/control_led"                          "${pkgdir}/boot/RoPieee"
   install -m0755 "../ropieee/check_ntp_offset"                     "${pkgdir}/boot/RoPieee"

   install -m0644 "../ropieee/99-blacklist.conf"                    "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/alsa-base.conf"                       "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/fstab"                                "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/journald.conf"                        "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/ropieee.conf"                         "${pkgdir}/opt/RoPieee/conf"
   install -m0644 "../ropieee/sshd_config"                          "${pkgdir}/opt/RoPieee/conf"

   install -m0755 "../ropieee/run-updates"                          "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../ropieee/configure"                            "${pkgdir}/opt/RoPieee/sbin"
   install -m0755 "../ropieee/reboot"                               "${pkgdir}/opt/RoPieee/sbin"

   install -m0755 "../ropieee/lib/disable_usb_audio"                "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/enable_usb_audio"                 "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/install_roonbridge"               "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/touchscreen_on"                   "${pkgdir}/opt/RoPieee/lib"
   install -m0755 "../ropieee/lib/touchscreen_off"                  "${pkgdir}/opt/RoPieee/lib"

   install -m0644 "../ropieee/systemd/ropieee1-bootstrap.service"   "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee1-update.service"      "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee1-update.timer"        "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee1-reboot.service"      "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ropieee1-led.service"         "${pkgdir}/etc/systemd/system"

   # overruling some default services
   install -m0644 "../ropieee/systemd/ntpd.service"                 "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/systemd/ntpdate.service"              "${pkgdir}/etc/systemd/system"
   install -m0644 "../ropieee/rescue.service"                       "${pkgdir}/etc/systemd/system"
}

